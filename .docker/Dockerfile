FROM mam10eks/roberta-sentiment-analysis:0.0.1-dev

RUN huggingface-cli download OnnoLander/XLMRoberta-comparative-questions \
    && python3 -c "from transformers import XLMRobertaForSequenceClassification, AutoTokenizer; AutoTokenizer.from_pretrained('xlm-roberta-large')"

ADD . /app