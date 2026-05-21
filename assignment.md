Assignment (architecture and design decisions):
Overview
This project implements a Meeting Preparation Assistant using Google AI Studio and Gemini models via Vertex AI. The system analyses meeting content and generates structured, actionable insights including summaries, risks, talking points, and next steps.
The solution demonstrates prompt engineering, structured outputs, user experience prototyping, and iterative refinement.

Architecture
The system consists of the following components:
•	LLM Layer: Gemini 3.1 Pro (Vertex AI)
•	Prompt Layer: Structured prompt enforcing JSON output
•	UX Layer: Stitch-generated interface screens
•	Development Environment: Google AI Studio Agent Builder
•	Version Control: GitHub repository

Design Decisions
Model Selection
Gemini 3.1 Pro (Preview) was selected due to its strong reasoning capabilities. This is particularly important for:
•	Identifying meaningful risks
•	Producing structured JSON outputs
•	Generating actionable next steps
Flash models were considered but not used, as they prioritise speed over reasoning quality.

Structured Output Design
A strict JSON schema was enforced to ensure:
•	Consistent output format
•	Ease of interpretation
•	Compatibility for potential downstream systems
This approach improves reliability compared to free-text outputs.

Prompt Constraints
Specific rules were added to control model behaviour:
•	Prevent hallucination
•	Ensure grounding in provided content
•	Maintain clarity and precision
These constraints significantly improved output quality.

Prompt Iterations
Iteration 1
The initial prompt used simple instructions to generate meeting insights.
Observations:
•	Output lacked structure
•	Risks were often generic
•	Some responses were inconsistent
This highlighted the need for stricter formatting and control.

Iteration 2
A structured JSON format was introduced along with grounding rules.
Improvements:
•	Output became consistent
•	Reduced hallucination
•	Clear separation of sections
However, outputs still lacked prioritisation and depth.

Iteration 3 (Final Version)
Additional constraints were introduced to improve output quality:
•	Risks include impact levels (High / Medium / Low)
•	Talking points are concise and stakeholder-focused
•	Next steps are actionable and include ownership
•	Output is fully structured and free from repetition
Outcome: The system now produces professional, structured, and actionable insights suitable for real-world use.

UX Design (Stitch)
Stitch was used to generate UI mockups for the Meeting Prep Assistant.
The interface includes:
•	File upload functionality
•	Insight generation button
•	Structured output sections (summary, risks, talking points, next steps)
Stitch enabled rapid prototyping of a clean and professional interface, although it is limited to static outputs.

Advantages:
•	Rapid prototyping
•	Clean, professional design output
•	No coding required

Limitations:
•	Limited customisation
•	Static outputs (PNG format only)
•	No interactive functionality

Testing Approach
Due to platform limitations, file upload functionality was not available within Agent Studio preview mode.
To overcome this, testing was conducted by pasting structured meeting notes directly into the input field.
This approach still enabled:
•	Validation of prompt behaviour
•	Testing of output structure
•	Demonstration of iteration improvements

Future Improvements
To productionise this system, the following enhancements are recommended:
•	Integration with document ingestion (PDF and slide parsing)
•	API deployment via Cloud Run
•	Persistent storage for meeting data
•	User authentication and session management
•	Feedback loop for continuous improvement

Conclusion
This project demonstrates the effectiveness of iterative prompt engineering in building structured AI applications. Through progressive refinement, the system evolved from producing basic outputs to generating professional, production-ready meeting insights.
The final solution highlights how structured prompts and appropriate model selection can deliver reliable and actionable outputs aligned with business needs.
