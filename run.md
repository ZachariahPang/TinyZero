`docker pull drikster80/vllm-gh200-openai:v0.6.3`
`git clone git@github.com:ZachariahPang/TinyZero.git`
```
sudo docker run -it --rm \
    --gpus all \
    --ipc=host \
    -v $(pwd):/workspace \
    -w /workspace \
    --entrypoint bash \
    drikster80/vllm-gh200-openai:v0.6.3
```
Inside the container,
```
pip install -e .
pip install wandb
wandb login
```
```
python ./examples/data_preprocess/countdown.py --local_dir ./data
bash train-gh200.sh
```
