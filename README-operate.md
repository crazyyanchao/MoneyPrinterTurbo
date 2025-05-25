
- 使用UV启动后端API

```shell
uv venv
uv pip install -r requirements.txt
python main.py
# DOCS: http://127.0.0.1:8080/docs 或者 http://127.0.0.1:8080/redoc
```

- 启动前端WEBUI

```shell
.\.venv\Scripts\activate
streamlit run ./webui/Main.py --browser.serverAddress="127.0.0.1" --server.enableCORS=True --browser.gatherUsageStats=False
# WEBUI: http://127.0.0.1:8501
```
