## Reflection

This project demonstrated the importance of structured prompt engineering, iterative refinement, and model selection in building a practical AI application. Through three prompt iterations, the Meeting Prep Assistant evolved from producing basic outputs to delivering structured, actionable insights aligned with real-world business needs.

### Prompt Evolution

The development process began with an initial prompt (Iteration 1) that focused on generating meeting insights such as summaries, risks, and next steps. While the outputs were generally relevant, they were inconsistent in structure and often lacked clarity. The model produced free-form responses, with risks appearing vague and some information being loosely inferred. This highlighted the need for stronger constraints to guide output format and reliability.

In Iteration 2, a strict JSON output format was introduced alongside rules to prevent hallucination. This significantly improved consistency, as outputs were clearly segmented into defined categories such as summary, risks, talking points, and next steps. The structured format made the results easier to interpret and more suitable for downstream use. However, the outputs still lacked prioritisation and actionable detail.

Iteration 3 focused on improving the quality and usability of the outputs. Additional constraints were introduced, including assigning impact levels (High, Medium, Low) to risks, limiting talking points to concise stakeholder-ready statements, and ensuring next steps were actionable with ownership fields. These enhancements resulted in outputs that were significantly more structured, precise, and aligned with real-world business expectations.

### Model Selection Trade-offs

Model selection played a key role in determining output quality. Flash models were considered due to their speed, but they were not suitable for this use case as they lacked the reasoning depth required for identifying risks and generating structured insights.

Gemini 3.1 Pro (Preview) was selected due to its stronger reasoning capabilities. It performed better at interpreting meeting content, generating consistent structured outputs, and identifying meaningful risks and actions. The trade-off was slightly slower response times, but this was acceptable given the improved accuracy and reliability of the outputs.


### Use of Stitch for UX Design

Stitch was used to generate UI mockups for the Meeting Prep Assistant, enabling rapid prototyping without the need for front-end development. The generated interface included a file upload section, an insight generation button, and structured output areas for summaries, risks, talking points, and next steps.

The primary advantage of Stitch was speed and simplicity, allowing for quick generation of clean, professional UI designs. However, it had limitations, including limited customisation and lack of interactivity, as outputs are static images. Despite this, Stitch effectively demonstrated the intended user experience.


### Limitations and Challenges

A key limitation encountered was the absence of direct file upload functionality in the Agent Studio preview environment. This was addressed by simulating document input using pasted meeting content. While this did not fully replicate real-world usage, it allowed for effective testing of prompt behaviour and output structure.

Another challenge was ensuring that the model consistently adhered to structured output requirements. This was addressed through prompt refinement and the introduction of explicit formatting and behavioural constraints.


### Future Improvements

To productionise this system, several enhancements could be implemented:

- Integration with document ingestion pipelines (PDF and slide parsing)  
- Deployment as an API using Cloud Run  
- Persistent storage for meeting data and outputs  
- User authentication and session management  
- Feedback mechanisms to iteratively improve output quality  


### Conclusion

Overall, the project highlights how iterative prompt engineering can significantly improve the performance and reliability of AI systems. By progressively refining the prompt and enforcing structured outputs, the Meeting Prep Assistant evolved into a practical tool capable of generating meaningful and actionable meeting insights.

The combination of structured prompt design, appropriate model selection, and rapid UX prototyping demonstrates a scalable approach to building AI-powered applications in a business context.
