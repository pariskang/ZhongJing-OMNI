# ZhongJing-OMNI: The First Multimodal Benchmark for Evaluating Traditional Chinese Medicine

**ZhongJing-OMNI** is the first multimodal benchmark dataset designed to evaluate Traditional Chinese Medicine (TCM) knowledge in large language models. This dataset provides a diverse array of questions and multimodal data, combining visual and textual information to assess the model’s ability to reason through complex TCM diagnostic and therapeutic scenarios. The unique combination of TCM textual knowledge with multimodal tongue diagnosis data sets a new standard for AI research in TCM.

### Key Multimodal Features:
- **Multiple-choice questions**: Encompassing core TCM concepts, syndromes, diagnostics, and herbal formulas.
- **Open-ended questions**: Focused on detailed diagnostic reasoning, treatment strategies, and explanation of TCM principles.
- **Case-based questions**: Real-world clinical cases that require in-depth analysis and comprehensive treatment approaches.
- **Multimodal tongue diagnosis Q&A**: High-resolution tongue images paired with corresponding diagnostic questions and expert answers, combining both visual and textual data to evaluate the model’s understanding of TCM tongue diagnosis.

This multimodal dataset allows AI systems to develop a deeper, more holistic understanding of TCM by integrating textual reasoning with visual diagnostic skills, making it a powerful resource for healthcare AI research.

## Dataset Structure

- `MCQ/`: Multiple-choice questions with answer keys.
- `OpenQA/`: Open-ended questions with detailed expert-verified answers.
- `CaseQA/`: Clinical case-based questions and answers.
- `TongueDiagnosis/`: High-quality tongue diagnosis images with paired Q&A for multimodal analysis.

## How to Use

### 1. Clone the repository:
```bash
git clone https://github.com/yourusername/ZhongJing-OMNI.git
#2. Load the dataset:
```
```python
import pandas as pd

# Load multiple-choice data
mcq_data = pd.read_csv('MCQ/questions.csv')

# Load open-ended Q&A
openqa_data = pd.read_csv('OpenQA/questions.csv')

# Load case-based Q&A
caseqa_data = pd.read_csv('CaseQA/questions.csv')

# Load tongue diagnosis Q&A (multimodal data)
tongue_data = pd.read_csv('TongueDiagnosis/tongue_questions.csv')
```
3. Multimodal Tongue Diagnosis Example:

```python
from PIL import Image

# Load and display an example tongue image for multimodal evaluation
img = Image.open('TongueDiagnosis/images/tongue001.png')
img.show()

# Load the corresponding Q&A
with open('TongueDiagnosis/questions/tongue001_question.txt', 'r') as file:
    question = file.read()
print(f"Question: {question}")

with open('TongueDiagnosis/answers/tongue001_answer.txt', 'r') as file:
    answer = file.read()
print(f"Answer: {answer}")
```

## Why Multimodal?
The ZhongJing-OMNI dataset introduces the first multimodal component for TCM, combining visual and textual data, which is crucial for understanding complex diagnostic features such as tongue color, shape, and coating. This allows models to:

- **Learn how to integrate visual diagnostic features with textual knowledge.
- **Perform joint reasoning over both modalities to reach accurate TCM diagnoses.
- **Support real-world clinical applications where visual and textual data are intertwined.

# Tongue Diagnosis Example: Qi Deficiency with Pale Tongue

![Qi Deficiency Pale Tongue](TongueDiagnosis/images/demo.png)

This image shows a pale, slightly swollen tongue with a thin white coating. These features are typical signs of Qi deficiency in Traditional Chinese Medicine.

This example represents an actual test result from our dataset using the Claude-3.5-Sonnet model. It demonstrates the model's capability to accurately identify and describe key features of tongue images used in Traditional Chinese Medicine diagnosis.

## Contact
For questions or collaboration, please contact at Email: ylkan21@m.fudan.edu.cn

Citation
If you use ZhongJing-OMNI in your research or project, please cite it as follows:

```
@dataset{zhongjing_omni_2024,
  title = {ZhongJing-OMNI: The First Multimodal Benchmark for Evaluating Traditional Chinese Medicine},
  author = {Kang, Yanlan},
  year = {2024},
  publisher = {GitHub},
  journal = {GitHub repository},
  url = {https://github.com/yourusername/ZhongJing-OMNI}
}
```
