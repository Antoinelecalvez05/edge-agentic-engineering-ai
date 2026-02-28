# edge-agentic-engineering-ai
Overview
This repository documents the development of a private, locally hosted agentic AI system running on NVIDIA Jetson hardware.
The objective is not to build a conversational assistant, but a controlled reasoning system capable of generating structured outputs that can drive engineering software such as FreeCAD and LTspice.
The system is designed around strict separation between:
Model reasoning
Structured output generation
Validation and constraint enforcement
External tool execution
The architecture prioritizes reliability, determinism, and full data locality.

What Currently Works
Local inference using quantized instruction-tuned language models
Structured JSON output generation experiments
Comparison of lightweight vs larger instruction models under edge constraints
Middleware prototype for validating structured outputs before execution

In Progress
Lightweight web interface for local browser access
Stabilizing end-to-end execution from model output to FreeCAD / LTspice result
Improving structured output consistency under constrained prompting
Refining middleware validation logic

Design Philosophy
The language model never directly executes system commands.
It proposes structured actions in JSON format.
A middleware layer validates schema constraints and restricts execution to predefined functions.
External tools perform computation.
This separation reduces instability and improves safety under hardware constraints.

Current Status
This project is actively in development.
The inference layer and structured output testing are functional.
The full execution pipeline from user request → validated action → completed engineering result is currently being refined.
The focus remains on architectural discipline rather than conversational capability.
