# Dimension {0}

## Solution Approach

	  We approached the solution by first deeply understanding the custom Domain-Specific Language (DSL) syntax and semantics. Our initial plan involved fine-tuning a model specifically to handle DSL-to-VB.NET translation. To support this, we generated a robust dataset primarily focused on the Industrial Automation domain.  
	  
	  Our dataset creation process followed a structured path:  
	  	•	Base Cases Creation: Hand-crafted DSL programs and their accurate VB.NET equivalents.  
	  	•	Data Augmentation Techniques:  
	  	•	Token-level augmentation  
	  	•	Structural reordering  
	  	•	Noise injection  
	  	•	Negative sampling with non-DSL code (e.g., Python)  
	  
	  After producing ~300 high-quality pairs, we began fine-tuning several shortlisted models. However, due to performance limitations (mainly from insufficient data and time constraints), we pivoted to a prompt engineering approach instead of full model fine-tuning.  
	  
	  Ultimately, we adopted Google Gemini, which provided a powerful and accessible interface for accurate DSL-to-VB.NET conversion through prompt-based generation.  

## Implementation Details  

  	Technologies & Tools:  
	•	Python – dataset generation, augmentation scripts  
	•	Google Gemini 1.5 Pro – for DSL-to-VB.NET conversion  
	•	Git & GitHub – version control  
	•	DSL syntax rules – custom-designed for Honeywell-like control systems  
	Techniques Used:  
	•	Prompt engineering  
	•	Data augmentation (custom scripts)  
	•	Model evaluation  
	•	VB.NET syntax optimization  
 
## Execution Steps  

	1.	Clone the Repository   
`git clone https://github.com/Shreeganeshhere/Dimension-0-.git`  
`cd Dimension-0-/backend`  

	2. Run the gemini model  
`python3 gemini_model.py`  

 	3. Enter the Input  
	
 	4. Get your output  
  
## Dependencies  

	•	Python 3.8+  
	•	Google Gemini 1.5 Pro or Gemini Flash  
	•	Git  

## Expected Output

	The output is a clean, syntactically correct, and logically equivalent VB.NET version of the input DSL code. This output preserves control flow, function calls, and custom operations while optimizing for real-world execution. It is ready to be integrated into larger VB.NET projects and tested for correctness.  
 	For example, a BLOCK in DSL becomes a Sub, while CALL functions are mapped to standard VB.NET Sub or Function calls.
