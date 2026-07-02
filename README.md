---
language:
  - ps
language_bcp47:
  - ps-AF
license: cc-by-4.0
tags:
  - pashto
  - glossary
  - dedup
  - linguistics
  - ai
  - nlp
  - corpus
  - ipashto
  - yugen
  - talanda
  - multilingual
  - dataset
  - education
  - translation
  - semantic
  - tokenization
  - pashto-ai
  - pashto-llm
pretty_name: "iPashto Glossary Ddup Dataset"
size_categories:
  - 10k<n<50k
task_categories:
  - text-generation
  - translation
  - other
viewer: false
---

# 🦅 iPashto.ai Culturally Aligned Master Glossary (ddup)

Welcome to the official **iPashto.ai Master Glossary** dataset repo (`nassimjp/ipashto-glossary-ddup`). This is a highly specialized, clean, and deduplicated dictionary network covering **39 strategic domains** with **11,442 unique entries**. 

As verified in our deployment log (**Screenshot from 2026-07-02 22-33-31.png**), this dataset maps complex domain terminology and foreign personal names (English, Chinese, and Japanese) directly into culturally authentic, natural, and context-aware Pashto equivalents. It is specifically built to enhance the contextual reasoning and translation pipeline of Pashto LLMs (such as the Rawan series).

---

## 🗂️ Domain Mapping & Tags

### 🌾 Agriculture & Farming
*   `ddup_agriculture.json` — Fundamental botanical, soil, and general agricultural terms.
*   `ddup_agriculture_farming.json` — Functional terms for practical farming, tools, and methods.
*   `ddup_livestock_veterinary.json` — Animal husbandry, livestock management, and veterinary science.

### 🚗 Automotive & Logistics
*   `ddup_car_types_automotive.json` — Automotive engineering, vehicle components, and transportation terms.
*   `ddup_shipping_logistics.json` — Supply chain, freight, distribution, and global logistics terminology.

### 🍲 Food, Cooking & Grocery
*   `ddup_cooking.json` — Massive index of culinary techniques, recipes, and traditional cooking terms.
*   `ddup_food_items.json` — Specialized directory for prepared meals, ingredients, and dishes.
*   `ddup_grocery_supplies.json` — Raw ingredients, market provisions, and household supplies.
*   `ddup_beverages_drinks.json` — Classification of hot, cold, traditional, and commercial beverages.

### 💰 Finance & Economics
*   `ddup_finance_economics.json` — Micro/macroeconomics, macro-policies, and fiscal principles.
*   `ddup_finance_commerce.json` — Corporate trade, transactional commerce, and market dynamics.
*   `ddup_currencies_finance.json` — Global currency mapping and core financial transactions.

### ⚖️ Legal & Governance
*   `ddup_legal.json` — Statutory terms, contractual language, and legal frameworks.
*   `ddup_islamic_jurisprudence.json` — Islamic legal rulings (Fiqh), jurisprudential definitions, and ethical terminology.

### 🩺 Medical & Health
*   `ddup_medical.json` — Healthcare diagnostics, clinical anatomy, symptoms, and medical treatment frameworks.

### ➗ Mathematics & Statistics
*   `ddup_mathematics.json` — Algebraic, geometric, statistical, and advanced computational mathematical terminology.

### ⚛️ Physics & Pure Sciences
*   `ddup_physics_chemistry.json` — Combined operational terms for structural physics and chemical elements.
*   `ddup_pure_sciences.json` — Theoretical science concepts, research terminology, and natural sciences.

### 🧠 Psychology & Behavior
*   `ddup_psychology_behavior.json` — Cognitive behavior, psychological analysis, and human mental framework terms.

### 💻 Technology & SEO
*   `ddup_tech_glossary.json` — IT infrastructure, hardware/software design, and Artificial Intelligence terminology.
*   `ddup_seo_education.json` — Digital marketing architectures, SEO optimization, and modern educational methodologies.

### ✈️ Travel & Tourism
*   `ddup_travel_tourism.json` — Hospitality structures, geographical navigation, and travel logistics.
*   `ddup_countries_capitals.json` — Accurate geopolitical localization for countries and world capitals.
*   `ddup_geography_continents.json` — Physical geography, terrain attributes, and global continental regions.

### 🛒 Shopping & Marketplaces
*   `ddup_bazar_marketplace.json` — Traditional trade structures, local bazaar colloquialisms, and negotiation terms.
*   `ddup_shopping_ecommerce.json` — Modern digital e-commerce flows, user checkout terms, and retail logistics.

### 🧵 Fashion & Tailoring
*   `ddup_tailoring_fashion.json` — Textile terminology, garments, local design patterns, and tailoring methodologies.

### 📖 Linguistics & Core Infrastructure
*   `ddup_linguistics_grammar.json` — Morphological syntax, lexical rules, and specialized grammar concepts.
*   `ddup_core.json` — High-priority foundational system tokens for structural alignment.
*   `ddup_common.json` — Highly frequent conversational connector phrases and basic vocabulary.

---

## 🧑‍🤝‍🧑 Cross-Cultural Persona Mapping (For SFT Datasets like TinyStories)
To replace dry, machine-translated western or eastern names with highly organic Pashto alternatives during dataset processing, use these mapped files:

*   **English:**
    *   `ddup_english_to_pashto_boys_names.json` (e.g., *John → خان*)
    *   `ddup_english_to_pashto_girls_names.json` (e.g., *Mary → زرغونه*)
*   **Chinese:**
    *   `ddup_chinese_to_pashto_boys_names.json` (Original Kanji keys mapped to Pashto male equivalents)
    *   `ddup_chinese_to_pashto_girls_names_meaning.json` (Original Kanji keys mapped to meaning-aligned Pashto female equivalents)
*   **Japanese:**
    *   `ddup_japanese_to_pashto_boys_names.json` (Original Kanji keys mapped to Pashto male equivalents)
    *   `ddup_japanese_to_pashto_women_names.json` (Original Kanji/Kana keys mapped to Pashto female equivalents)
*   **Mythology:**
    *   `ddup_fantasy_mythology.json` — Cultural alternatives for magical creatures, folklore entities, and fantasy arcs.

---

## 🛠️ Quick Usage via Hugging Face Datasets

You can parse any specific json file seamlessly into your Python NLP pipelines:

```python
import json
from huggingface_hub import hf_hub_download

# Example: Download and load the Japanese to Pashto Women Names glossary
file_path = hf_hub_download(
    repo_id="nassimjp/ipashto-glossary-ddup", 
    filename="data/ddup_japanese_to_pashto_women_names.json",
    repo_type="dataset"
)

with open(file_path, "r", encoding="utf-8") as f:
    glossary = json.load(f)

print(f"Loaded {len(glossary)} authentic mapping pairs!")

```

---

**Powered by iPashto.ai Development Framework** 🚀

```
## 🧩 د کارونې مثال
```python
from datasets import load_dataset
ds = load_dataset("nassimjp/ipashto-glossary-ddup")
print(ds)
```

## ✨ جوړونکی
**Nassim Nasibullah** — Founder of Spinzar Enterprises Inc. (Yūgen Kaisha), Japan  
Pashto AI Research & Development Division

## 📅 وروستی تازه‌والی
2026‑07‑02

---
```