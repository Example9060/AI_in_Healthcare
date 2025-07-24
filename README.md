#  AI in Healthcare — Автоматизированный Пайплайн Сбора и Обработки Новостей

##  Цель проекта

Создать автоматизированный pipeline, который:

1. Собирает статьи из открытых источников по теме «AI in Healthcare»
2. Кластеризует статьи по темам с помощью тематического моделирования
3. Генерирует краткие резюме для каждого кластера
4. Формирует финальную мета-статью (5000–7000 слов), охватывающую все ключевые темы
5. Работает с использованием LangChain, Together.ai API и Python-библиотек

---

##  Архитектура проекта

```
ai-healthcare-pipeline/
├── README.md
├── requirements.txt
├── config.yaml
├── data/
│   ├── full_articles.csv
│   └── clustered_articles.csv
├── notebooks/
│   ├── collect.ipynb
│   └── afm_tz2.ipynb
└── output/
    ├── cluster_summaries.txt
    └── meta_article.txt
```

---

##  Как запустить

1. **Установить зависимости**  
   ```bash
   pip install -r requirements.txt
   ```

2. **Указать ключи API** в `config.yaml`

3. **Собрать статьи**
   ```bash
   python src/collect.py
   ```

4. **Кластеризовать и сгенерировать резюме**
   ```bash
   python src/cluster.py
   python src/summarize.py
   ```

5. **Собрать финальную мета-статью**
   ```bash
   python src/generate_meta.py
   ```

---

##  Используемые технологии

-  Python 3.11
-  GNews + newspaper3k + selenium
-  Together.ai API + LangChain
- SentenceTransformers + sklearn
-  Jupyter Notebooks(kaggle)

---

##  Вывод

Результаты:

- Краткие резюме: `output/cluster_summaries.txt`
- Мета-статья: `output/meta_article.txt`




