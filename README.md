# 🍽️ AI Recipe Vision Project

> **Multimodal AI pipeline that enriches food recipe and restaurant review datasets with LLM-generated image captions using IBM WatsonX and LLaMA Vision.**

---

## 📌 Overview

This project demonstrates how to process **multimodal data** (images + text) using Large Language Models (LLMs). A vision-capable LLaMA model is used to automatically generate descriptive captions for food images, which are then integrated into structured JSON datasets — augmenting both recipe data and user restaurant reviews.

The lab is part of the **IBM Generative AI / Agentic AI Professional Certificate** curriculum on Coursera (Skills Network).

---

## 🎯 Objectives

- Load structured food recipe and restaurant review JSON datasets containing image references
- Configure and use a **LLaMA-based vision LLM** via IBM WatsonX AI
- Design and validate prompts for multimodal image captioning
- Iterate over datasets and generate captions for all food and review images
- Augment and save the enriched JSON files for downstream AI applications

---

## 🗂️ Project Structure

```
AI-Recipe-Vision-Project/
│
├── M1L2_Process_Multimodal_Data_with_LLMs.ipynb   # Main Jupyter Notebook (lab)
├── Recipes.json                                    # Raw food recipe dataset (109 recipes)
├── Synthetic-User-Reviews.json                     # Raw restaurant user reviews dataset
├── augmented_food_recipe.json                      # Recipes enriched with image_description
├── augmented_user_review.json                      # Reviews enriched with image_captions
└── README.md                                       # Project documentation
```

---

## 📊 Datasets

### `Recipes.json`
A structured dataset containing **109 food recipes** across multiple cuisines.

| Field | Description |
|---|---|
| `id` | Unique recipe identifier |
| `name` | Recipe name (e.g., Classic Margherita Pizza) |
| `cuisine` | Cuisine type (Italian, Indian, Chinese, etc.) |
| `servings` | Number of servings |
| `prep_time` | Preparation time |
| `cook_time` | Cooking time |
| `total_time` | Total time |
| `ingredients` | List of ingredients |
| `directions` | Step-by-step cooking instructions |

### `Synthetic-User-Reviews.json`
Restaurant visit reviews with image URLs and ratings.

| Field | Description |
|---|---|
| `reviewId` | Unique review ID |
| `userId` | Reviewer identifier |
| `itemId` | Restaurant identifier |
| `title` | Review title |
| `text` | Full review text |
| `date` | Review date |
| `rating` | Star rating (out of 5) |
| `images` | List of image URLs |

### Augmented Outputs
| File | Added Field | Description |
|---|---|---|
| `augmented_food_recipe.json` | `image_description` | AI-generated visual description of the dish |
| `augmented_user_review.json` | `image_captions` | AI-generated captions for each review image |

---

## 🧠 Tech Stack

| Tool / Library | Purpose |
|---|---|
| **Python 3** | Core programming language |
| **IBM WatsonX AI** | LLM hosting and inference platform |
| **LLaMA Vision Model** | Multimodal image + text understanding |
| **NumPy** | Numerical operations and array handling |
| **Matplotlib** | Data visualization and image inspection |
| **Pillow (PIL)** | Image loading and preprocessing |
| **JSON** | Data parsing and augmented output saving |
| **Jupyter Notebook** | Interactive development environment |

---

## ⚙️ Setup & Installation

### Prerequisites
- Python 3.8+
- IBM WatsonX AI account with API credentials
- Jupyter Notebook or JupyterLab

### Install Dependencies

```bash
pip install numpy==2.3.4
pip install matplotlib==3.10.7
pip install ibm-watsonx-ai==1.4.7
pip install Pillow
```

### IBM WatsonX Credentials

Set up your credentials before running the notebook:

```python
from ibm_watsonx_ai import Credentials

credentials = Credentials(
    url="https://us-south.ml.cloud.ibm.com",
    api_key="YOUR_IBM_API_KEY"
)
```

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/Leelaissakattaota/AI-Recipe-Vision-Project.git
   cd AI-Recipe-Vision-Project
   ```

2. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook M1L2_Process_Multimodal_Data_with_LLMs.ipynb
   ```

3. **Run the notebook cells in order:**
   - Set up environment and install libraries
   - Fetch and explore the datasets
   - Configure the vision LLM (LLaMA via WatsonX)
   - Run Exercise 1: Caption food recipe images
   - Run Exercise 2: Caption restaurant review images
   - Save augmented JSON outputs

---

## 🔬 Workflow Summary

```
Raw JSON Data (Recipes + Reviews)
         │
         ▼
   Load & Explore Data
         │
         ▼
  Configure Vision LLM (LLaMA via WatsonX)
         │
         ▼
  Design & Validate Prompts
         │
         ▼
  Caption All Images (Batch Inference)
         │
         ▼
  Augment JSON with Captions
         │
         ▼
  Save Augmented Output Files
```

---

## 📋 Exercises

### Exercise 1 — Food Recipe Image Captioning
1. Load and explore `Recipes.json`
2. Define the vision LLM with LLaMA
3. Design and validate a food-specific caption prompt
4. Caption all recipe images and augment the dataset
5. Save as `augmented_food_recipe.json`

### Exercise 2 — Restaurant Review Image Captioning
1. Load and explore `Synthetic-User-Reviews.json`
2. Design a prompt incorporating user review context
3. Caption all review images using the vision LLM
4. Augment and save as `augmented_user_review.json`

---

## 💡 Sample Output

**Input Recipe:** Classic Margherita Pizza

**AI-Generated Image Description:**
> *"This image presents a delectable Classic Margherita Pizza, expertly crafted with fresh ingredients. The pizza is adorned with vibrant green basil leaves, adding color and fragrance. The crust boasts a golden-brown hue with subtle charred accents, while the melted mozzarella glistens with a creamy sheen. A rich tomato sauce serves as the base, providing a tangy and savory flavor profile..."*

---

## 📚 Course Context

This project is a hands-on lab from:
- **Course:** IBM Generative AI Professional Certificate
- **Module:** M1 — Processing Multimodal Data with LLMs
- **Lab:** M1L2 — Process Multimodal Data with LLMs
- **Platform:** Coursera / IBM Skills Network
- **Author:** Jianping (Mike) Ye

---

## 👤 Author

**Leela Issak Attota**
- 📍 Bengaluru, India
- 💼 AI/ML Enthusiast | Generative AI | Data Science
- 🔗 [GitHub](https://github.com/Leelaissakattaota)
- 🎓 IBM Data Science Professional Certificate | IBM Generative AI Professional Certificate

---

## 📄 License

This lab and its materials are © IBM Corporation. All rights reserved.
The implementation code in this repository is for educational and portfolio purposes.

---

*⭐ If you found this project helpful, consider giving it a star!*
