# Greek Mythology QA System

## English Description

A Persian language question-answering system about Greek mythology using few-shot learning and semantic similarity. The system answers questions about Greek gods and goddesses with concise responses (4-5 words maximum).

### Features

- **Few-Shot Learning**: Uses semantic similarity to select relevant examples
- **Persian Language Support**: Handles Persian text and questions
- **Concise Responses**: Provides short, focused answers (4-5 words max)
- **Greek Mythology Knowledge**: Covers 14 major Olympian gods and goddesses
- **Semantic Example Selection**: Uses Cohere embeddings for intelligent example selection

### System Components

1. **Knowledge Base**: JSON file containing information about 14 Greek gods
2. **Example Database**: 30 question-answer pairs for few-shot learning
3. **Semantic Selector**: ChromaDB with Cohere embeddings for example selection
4. **Language Model**: Cohere Command-R-Plus for answer generation

### Technical Implementation

- **Embeddings**: Cohere multilingual embeddings (`embed-multilingual-v3.0`)
- **Vector Store**: ChromaDB for semantic similarity search
- **LLM**: Cohere Command-R-Plus model
- **Framework**: LangChain for prompt engineering and chain management

### Gods Covered

Zeus, Hades, Poseidon, Hera, Demeter, Hestia, Ares, Hermes, Dionysus, Hephaestus, Apollo, Artemis, Aphrodite, Athena

---

## توضیحات فارسی

سیستم پرسش و پاسخ فارسی درباره اساطیر یونان با استفاده از یادگیری چند نمونه‌ای و شباهت معنایی. سیستم به سوالات درباره خدایان و الهه‌های یونانی با پاسخ‌های مختصر (حداکثر 4-5 کلمه) پاسخ می‌دهد.

### ویژگی‌ها

- **یادگیری چند نمونه‌ای**: استفاده از شباهت معنایی برای انتخاب نمونه‌های مرتبط
- **پشتیبانی از زبان فارسی**: پردازش متن و سوالات فارسی
- **پاسخ‌های مختصر**: ارائه پاسخ‌های کوتاه و متمرکز (حداکثر 4-5 کلمه)
- **دانش اساطیر یونان**: پوشش 14 خدای اصلی المپوس
- **انتخاب نمونه معنایی**: استفاده از embedding های Cohere برای انتخاب هوشمند نمونه‌ها

### اجزای سیستم

۱. **پایگاه دانش**: فایل JSON حاوی اطلاعات درباره 14 خدای یونانی
۲. **بانک نمونه‌ها**: 30 جفت سوال-جواب برای یادگیری چند نمونه‌ای
۳. **انتخابگر معنایی**: ChromaDB با embedding های Cohere برای انتخاب نمونه
۴. **مدل زبانی**: Cohere Command-R-Plus برای تولید پاسخ

### پیاده‌سازی فنی

- **Embeddings**: embedding چندزبانه Cohere (`embed-multilingual-v3.0`)
- **Vector Store**: ChromaDB برای جستجوی شباهت معنایی
- **LLM**: مدل Cohere Command-R-Plus
- **Framework**: LangChain برای مهندسی prompt و مدیریت زنجیره

### خدایان پوشش داده شده

زئوس، هادس، پوسوئیدون، هرا، دمتر، هستیا، آرس، هرمس، دیونیسوس، هفایستوس، آپولون، آرتمیس، آفرودیت، آتنا

## Installation

```bash
# Install required packages
pip install langchain-cohere
pip install langchain-chroma
pip install langchain-core
pip install pandas

# Set up Cohere API key
export COHERE_API_KEY="your_api_key_here"
```

## Usage

1. Run the main notebook (`main.ipynb`) or test notebook (`Quera_Test.ipynb`)
2. The system will load the gods database and create example embeddings
3. Ask questions about Greek mythology in Persian
4. Receive concise answers (4-5 words maximum)

### Example Questions

```
سوال: همسر زئوس چه کسی است؟
پاسخ: هرا

سوال: آتنا با چه حیوانی همراه است؟
پاسخ: جغد

سوال: هرمس خدای چه چیزهایی است؟
پاسخ: بدبختی، سفر، تجارت، زبان
```

## Project Structure

```
Greek-Mythology-QA-System/
├── main.ipynb              # Interactive Q&A system
├── Quera_Test.ipynb       # Automated testing system
├── gods.json              # Greek gods knowledge base
├── questions.csv          # Test questions dataset
├── .gitignore            # Git ignore file
└── README.md             # This file
```

## Features

- **Rate Limiting**: Built-in API rate limiting management
- **Error Handling**: Robust error handling for API calls
- **Batch Processing**: Efficient processing of multiple questions
- **Few-Shot Learning**: Dynamic example selection based on question similarity

## Author

**Mohammad Sadegh Seifi**

## License

This project is for educational purposes.
