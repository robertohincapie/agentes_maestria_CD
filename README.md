# agentes_maestria_CD
# Se debe tener instalado UV
curl -LsSf https://astral.sh/uv/install.sh | sh
uv --version

# Organización del repositorio para poder correr los agentes. 
uv init
uv venv

# add dependencies
uv add --pre langgraph langchain langchain-openai
uv add --pre langchain-anthropic
uv add "fastapi[standard]"

# add dev dependencies
uv add "langgraph-cli[inmem]" --dev
uv add ipykernel --dev
uv add grandalf --dev
uv add langchain-tavily

# run the agent
#uv run langgraph dev



# instalar el proyecto con la estructura apropiada
uv pip install -e .