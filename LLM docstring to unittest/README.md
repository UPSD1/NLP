# **LLM-Based Unit Test Generation from Python Docstrings**  

This project fine-tunes large language models (LLMs) to generate Python unit tests directly from function **docstrings**. The models are evaluated for accuracy, robustness, and generalization, using custom datasets and mutation testing techniques.

---

## **Overview**  

### **Goal**  
Automate the creation of Python unit tests using LLMs, improving developer productivity and ensuring code reliability.

### **Key Features**  
1. **Fine-Tuned LLMs**: Models such as **LLaMA 3.0**, **CodeLLaMA**, and **GPT-3.5** were fine-tuned for test case generation.  
2. **Dataset Reconstruction**: Standardized test case lengths to ensure consistent model output.  
3. **Mutation Testing**: Gemini-generated mutations assess model robustness.  
4. **Evaluation Metrics**: Code validity, correctness, and accuracy are rigorously tested.  

---

## **Setup Instructions**  

### **Prerequisites**  
- Python 3.x  
- A Google account for running **Google Colab**  
- API keys for the following services:  
   - **OpenAI** (for GPT models)  
   - **Lamini** (for fine-tuning LLaMA models)  
   - **Gemini** (for code mutation generation)  

---

### **Steps to Run**  

1. **Open the Colab Notebook**  
   - Go to [Google Colab]([https://colab.research.google.com/](https://colab.research.google.com/drive/1V9_Mc1qwXkxoO3GYZzcQjF8EpfXL3Nk8?usp=sharing)).  

2. **Set API Keys**  
   Add your API keys to the notebook secrets using the following names:  
   - **OpenAI Key** → `openai_key`  
   - **Lamini Key** → `lamini.api_key`  
   - **Gemini Key** → `gemini_key`  

4. **Run All Cells**  
   - Navigate to the **Third Trial** section of the notebook.  
   - Select **"Runtime" → "Run all"**.  
   - The notebook will execute all cells sequentially, including dataset preparation, model fine-tuning, test generation, and evaluation.  

---

## **Results**  

### Fine-Tuned Model Performance  
| Metric           | Fine-Tuned | Fine-Tuned (Mutation) | Gemini  | GPT-3.5 |  
|------------------|------------|-----------------------|---------|---------|  
| **Code Validity**| 26 / 30    | 26 / 30              | 30 / 30 | 25 / 30 |  
| **Correctness**  | 10 / 26    | 7 / 26               | 14 / 30 | 10 / 25 |  
| **Accuracy**     | 38.46%     | 26.92%               | 46.67%  | 40.0%   |  

### Observations  
- Fine-tuned models struggled with mutation-induced code variations.  
- Gemini outperformed other models with **100% code validity** and higher correctness rates.  
- GPT-3.5 showed competitive performance but fell short of Gemini.  

---

## **Project Structure**  
- **CS_6158_ClassProject.ipynb**: Contains the Colab notebook for execution.  
- **README.md**: This file.
- 
---

## **Acknowledgements**  
This project leverages powerful tools and frameworks:  
- **OpenAI GPT**  
- **LLaMA & CodeLLaMA**  
- **Google Gemini**  
- **EvalPlus Dataset**  

---

## **License**  
This project is licensed under the MIT License.  

---

## **Contact**  
For questions or feedback, reach out via:  
- Email: daa238@cornell.edu

