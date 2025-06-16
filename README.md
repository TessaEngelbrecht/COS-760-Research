# COS-760-Research: Detecting Machine-Generated Text in African Languages  
**David Roodt (u19264047), Tessa Engelbrecht (u22633601), Catherina Ackerman (u24076491)**  
*University of Pretoria*  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)  
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1B9FMRyw1Krc6ac3YrS8t80GY-4IyEXd6?usp=sharing)

---

## Table of Contents  
- [Project Overview](#project-overview)  
- [Installation](#installation)  
- [Data](#data)  
- [Methodology](#methodology)   
- [Contributing](#contributing)  
- [License](#license)   

---

## Project Overview  
This research addresses the critical gap in machine-generated text detection for **isiZulu** and **isiXhosa** – two major Southern Bantu languages spoken by over 19 million people. We develop a binary classifier using:  

- **Afro-XLM-R** for transfer learning  
- **Data augmentation** (back-translation, synonym replacement) 

---

## Installation  
### Local Setup  
git clone https://github.com/TessaEngelbrecht/COS-760-Research.git
cd code
pip install -r requirements.txt

### Google Colab  
Model and training: [![isiZulu Detection Notebook](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1B9FMRyw1Krc6ac3YrS8t80GY-4IyEXd6?usp=sharing)  
Data gathering: [![isiXhosa Detection Notebook](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1HWsO7WWTqdEdBYGmZkKdYwK1uM9x2EM2?usp=sharing)

---

## Data  
### Sources  
| Language   | Human Sources                              | Machine Generation Methods              |
|------------|--------------------------------------------|------------------------------------------|
| **isiZulu** | ZA isiZulu-Siswati News (10k+ articles)    | GPT-4/Gemini API prompts + MarianMT      |
| **isiXhosa**| MasakhaPOS (POS-tagged sentences)         | Template-based pattern synthesis         |

---

## Methodology   

**Key Components:**  
1. **Afro-XLM-R Encoder** pretrained on 17 African languages  
2. **Dual-Language Classifier** with shared parameters  
3. **Back-Translation Augmentation** (isiXhosa ↔ English → isiXhosa)  
---

## Contributing  
We welcome contributions! Please:  
1. Fork the repository  
2. Create a feature branch:  
git checkout -b feature/your-feature

3. Submit a **pull request** with:  
- Test cases for new features  
- Documentation updates  

---

## License  
This project is licensed under the **MIT License** - see [LICENSE](LICENSE) for details.  

---
