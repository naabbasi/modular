# modular getting started
magic init life --format mojoproject

magic run mojo hello.mojo
magic shell
mojo hello.mojo
mojo build hello.mojo

# magic tasks
magic task add hello mojo hello.mojo
magic run hello

magic task add hello-build mojo build hello.mojo
magic run hello-build

# add Python libraries
magic add --pypi "fastapi[standard]"
magic run python -m fastapi dev main.py

# Run llm models with max
1. magic global install max-pipelines
2. max-pipelines serve --huggingface-repo-id=deepseek-ai/DeepSeek-R1-Distill-Llama-8B \
--weight-path=lmstudio-community/DeepSeek-R1-Distill-Llama-8B-GGUF/DeepSeek-R1-Distill-Llama-8B-Q4_K_M.gguf