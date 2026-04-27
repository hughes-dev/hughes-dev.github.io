# Dylan — Software Engineer

Backend and systems-focused software engineer building distributed applications that integrate robotics, real-time processing, and AI-driven analysis. Experienced in designing and implementing multi-service systems that operate across devices under constraints such as offline environments and low-latency requirements.

---

# Projects

## Robotics-Based Facility Monitoring System

Backend and AI Pipeline  
Work Project, Proprietary Code

### Role

Primary backend engineer. Responsible for designing and building the server-side system, with additional contributions to mobile, robot-side systems, and cross-system integration.

### Overview

Built the backend for a robotics-based monitoring platform that performs automated patrols and analyzes conditions inside a correctional facility. A mobile robot navigates the environment, streams live camera feeds and captures inspection video, which is sent to a central server for processing.

The server ingests video data, runs automated analysis, and presents results to operators through a live dashboard. Analysis includes person detection, motion and activity recognition, face matching against a known registry, contraband detection, and vision-language model-based scene interpretation.

Operators can view live video streams, review analysis results, and receive real-time alerts across web and mobile interfaces.

The system runs across multiple machines within a local network and is designed to operate fully offline.

### System Context

- A central server responsible for coordination, data processing, and analysis
- One or more mobile robots that capture video and sensor data during patrols
- An edge compute device on each robot that runs custom software and communicates with the server
- Client devices including browser-based dashboards and mobile devices for monitoring and alerts

The backend system I built runs on the central server and coordinates communication and data flow across all components.

### System Flow

```
┌──────────────────────────────┐
│        Web / Mobile UI       │
│   Dashboard + Alerts View    │
└──────────────┬───────────────┘
               │
┌──────────────┴───────────────┐
│        Central Server        │
│   API + Worker + Database    │
└──────────────┬───────────────┘
               │
┌──────────────┴───────────────┐
│         Edge Device          │
│  Control, Execution, Streams │
└──────────────────────────────┘
```

### What I Built

- Designed and implemented the backend architecture for a multi-service robotics platform
- Designed and built the API layer for patrol coordination, media ingestion, and real-time communication
- Designed and implemented core data models and database schema using PostgreSQL
- Built an asynchronous video analysis pipeline integrating computer vision and LLM-based inference
- Implemented a PostgreSQL-based job queue and inter-service communication system
- Selected and integrated infrastructure components including PostgreSQL for persistence and MediaMTX for real-time streaming
- Developed real-time alerting and state synchronization using WebSockets across multiple clients
- Built a mobile-compatible dashboard and Android wrapper for real-time monitoring and alerts
- Contributed to early robot-side development, including initial implementation of vision-based window alignment using object detection

### Tech Stack

Python, FastAPI, PostgreSQL, OpenCV, YOLO, InsightFace, Ollama, WebSockets, WebRTC, MediaMTX

### Code Availability

Source code is not publicly available due to this being proprietary company work.

---

## Agent Console

Remote Interface for Local AI Agent

GitHub: `https://github.com/hughes-dev/agent-interface`

### Overview

Built a Slack-based interface for interacting with a locally running AI agent from any device. The system exposes a local Claude Code agent through Slack, allowing users to send text or voice messages remotely and receive responses directly in the chat.

The goal of this project is to enable continuous interaction with an agent while it performs work in the background, allowing tasks to be monitored, guided, and iterated on remotely.

### Current Functionality

- Routes messages from a configured Slack channel to a local Claude Code agent and returns responses in-channel
- Supports voice input by transcribing audio attachments before sending them to the agent
- Generates spoken responses and uploads them alongside text replies
- Handles long responses by uploading full output as a file with a short preview
- Provides basic user feedback during processing through message reactions

The system runs locally and communicates with Slack using a persistent WebSocket connection, with all processing handled on the host machine.

### Planned Expansion

- Add conversation memory across messages, replacing the current stateless interaction model
- Separate conversational interaction from task execution by introducing a manager agent that can coordinate background worker agents
- Enable concurrent agent interactions instead of serialized request handling
- Improve reliability with structured logging and error handling

### Tech Stack

Python, Slack API, Socket Mode, Claude Code SDK, Whisper.cpp, FFmpeg, Piper TTS, asyncio

---

## Physics Simulator

2D Gravitational Simulation

GitHub: `https://github.com/hughes-dev/PhysicsSimulators`

Developed a 2D physics simulation modeling gravitational interactions between objects, including orbital motion and black hole behavior. The focus of this project was implementing the underlying physics calculations and simulation logic.

This project demonstrates understanding of mathematical modeling, numerical simulation, and system behavior under continuous forces.

### Tech Stack

C#, WPF

---

# Skills

### Languages
Python, C#, SQL

### Backend and Systems
System Design, Distributed Systems, FastAPI, Flask, PostgreSQL, REST APIs, WebSockets

### AI and Data
Computer Vision, OpenCV, Object Detection (YOLO), LLM Integration, Inference Pipelines

### Streaming and Media
MediaMTX, RTSP, WebRTC

### Tools and Environment
Linux, Git

---
