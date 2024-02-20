# Benchmarking LLMs 


The OpenVINO GenAI repository contains several examples that implement text generation tasks with LLMs. One highlight of
this repository is the [LLM Benchmarking tool](https://github.com/openvinotoolkit/openvino.genai/tree/master/llm_bench/python). The tool provides a unified approach to estimate performance for Large
Language Models. It is based on pipelines provided by Optimum-Intel and can be used to estimate performance for PyTorch
and OpenVINO™ models. 

## Prerequisites

**python -m venv openvino_env
**openvino_env\Scripts\activate

**pip install -r requirements.txt

Note: You can specify the installed openvino version through pip install
### e.g.
**pip install openvino==2023.3.0

## Commands to Test the Performance of one LLM
**python benchmark.py -m <model> -d <device> -r <report_csv> -f <framework> -p <prompt text> -n
<num_iters>
### e.g.
**python benchmark.py -m tiny-llama-1b-chat/INT8_compressed_weights -n 2  --report REPORT.csv
