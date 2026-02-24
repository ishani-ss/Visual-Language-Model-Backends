# Large Multimodal Model Research: Model Evaluation
This repository has been set up to contain research and experimentation on Large Multimodal Models. The specific focus is on how these models can be properly evaluated for optimal performance. 


## LMM Document Parsing Model Evaluation Research 
Evaluating LMMs for document parsing involves a combination of:
•	specialized benchmarks
•	quantitative metrics
•	qualitative human-in-the-loop (or AI-as-judge) assessments
These methods assess the LMM’s ability to extract and accurately structure information from visually rich documents. 


### Specialised Benchmarks and Datasets for Model Evaluation
•	OmniDocBench: Is a new benchmark with a high-quality and diverse dataset that covers nine document types (academic papers to exam papers) and is designed to address the limitations in current evaluation methods. 
•	CC-OCR: This is a comprehensive yet challenging benchmark that focuses on OCR-centric tasks in real-world scenarios, including multi-scene text reading and key information extraction. This is to reveal model limitations in text grounding and hallucination. 
•	OCRBench v2: This is an improved benchmark that evaluates model abilities like table parsing, chart parsing and formula recognition. It incorporates mathematical calculation and visual text understanding tasks.
•	LMMs-Eval: This is a unified and standardised multimodal evaluation suite that covers over 50 tasks. It offers a transparent and reproducible evaluation pipeline and a “Lite” version that is efficient enough to balance coverage and costs. 


### Quantitative Metrics for Model Evaluation
To measure model performance tailored to the parsing subtask, the following specialised metrics can be used: 
•	Normalized Edit Distance (NED): To evaluate general document parsing and formula recognition, to measure the difference between the model’s output and the ground truth. 
•	Tree Edit Distance-based Similarity (TEDS): A metric for table parsing that looks at the structural accuracy of the table extract. 
•	F1 Score: Used for key information extraction (KIE) tasks at a field level. 
•	Edit Distance/Levenshtein Distance: Used to evaluate the accuracy of the reading order of extracted elements. Sometimes this method incorporates penalty matrices for a comprehensive assessment. 
•	Eval-Trans and Eval-Pos: These metrics are used to evaluate text sequences and their positional accuracy. 


### Qualitative and Advanced Methods
•	LLM-as-a-Judge: This method involves a powerful language model (e.g. GPT-4) scoring the output of the LMM being evaluated against a ground truth or reference. This has specific prompts to ensure consistency and capture semantic equivalence. 
•	Human-in-the-Loop Scoring: Essential for nuanced tasks and complex scenarios where automated metrics might be too rigid or fail to capture “usefulness” or human preference (subjective quality aspects).
•	Zero-shot Evaluation Protocol: Assesses a model’s generalisation capacity without fine-tuning, using clear instructions and chain-of-though prompting to evaluate model performance on unseen tasks. 

### Best Practice
To ensure reliable and robust model performance across a variety of applications, model evaluation should combine the aforementioned methods. This ensures a comprehensive understanding of an LMM's strengths and weaknesses in document parsing.

