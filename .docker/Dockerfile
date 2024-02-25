#docker build -t registry.webis.de/code-research/tira/tira-user-salamander/comparative-questions:0.0.1 -f .docker/Dockerfile .
FROM mam10eks/roberta-sentiment-analysis:0.0.1-dev

RUN huggingface-cli download OnnoLander/XLMRoberta-comparative-questions \
    && python3 -c "from transformers import XLMRobertaForSequenceClassification, AutoTokenizer; AutoTokenizer.from_pretrained('xlm-roberta-large')"

RUN wget 'https://raw.githubusercontent.com/tira-io/ir-experiment-platform/main/tira-ir-starters/pyterrier/run-pyterrier-notebook.py' -O /run-notebook.py && \
	pip3 install runnb jupyter && \
	chmod +x /run-notebook.py

ADD . /app

RUN jupyter trust /app/code/*.ipynb

ENTRYPOINT [ "/run-notebook.py", "--input", "$inputDataset", "--output", "$outputDir", "--notebook", "/app/code/classify_comparative_queries.ipynb" ]

