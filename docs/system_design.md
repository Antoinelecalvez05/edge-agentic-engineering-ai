System Architecture Overview
Core Flow
User Request
→ Prompt Construction
→ Local LLM Inference
→ Structured JSON Output
→ Middleware Validation
→ Tool Adapter
→ Engineering Software Execution
→ Output Capture

Architecture Diagram
[ User Input ]
        ↓
[ Local LLM ]
        ↓
[ Structured JSON Output ]
        ↓
[ Middleware Validator ]
        ↓
[ Tool Adapter Layer ]
        ↓
[ FreeCAD / LTspice ]
        ↓
[ Result Returned ]

Design Constraints
No direct system command execution by the model
Only predefined tool functions are allowed
Required JSON schema enforced before execution
Full local processing (no external API dependency)

Model Considerations
Experiments have included:
Lightweight transformers (e.g., DistilGPT-2)
Larger instruction-tuned models (e.g., Mistral-7B Instruct, quantized)
The primary challenge observed was structured reliability, not linguistic fluency.
Under edge hardware constraints, model size directly impacts latency and memory usage
