# GPUs & LLMs Testing/Performance

## **Test 1: Countdown timer (mini) app on 5 local LLMs**

[Watch on YT](https://youtu.be/Sz2oMTMLgm8)

### Enviroment:
- Llama-cpp Vulkan [b9986](https://github.com/ggml-org/llama.cpp/releases/tag/b9986) (WebUI) 
- Windows 11
- CPU: Intel Core 265 Ultra
- RAM: DDR5 5600 96GB
- **GPU: Intel Arc Pro B70 (32GB)**
- Prompt type | Level: Coding | Low
- Prompt: Countdown Timer project
- Agent: [Opencode] (https://github.com/anomalyco/opencode)
- Command parameters: -np 1, -c 32000, -dev Vulkan1

### Prompt:
Check PROMPT-1.txt

### Result:


|Modle|Context|Processing|Generating|Duration|Quality|Attempts|
|---|---|---|---|---|---|---|
|Ornith 1 9B|32k|1850 - 1550 t/s|47 - 43 t/s|< 1min|6|1|
|Gemma 4 12B|32k|1800 - 1300 t/s| 27 - 23 t/s|< 3min|8|1 / 2 to have the file creted|
|Gemma 4 26B A4B|32k|1290 - 1083 t/s|52 - 48 t/s|< 2min |9|1 for code / 2 to have the file created|
|Qwen 3.6 27B|10k|703 - 310 t/s|21 - 17 t/s|< 5min|5|2|
|Qwem 3.6 35B A3B|8k|1384 - 1198 t/s|67 - 63 t/s|x|x|x|
|GPT OSS 20B|32k|2068 - 1367 t/s|84 - 77 t/s|< 1min|2|1 for code / 2 with file creation|


===


## **Test 2: GPU vs CPU | Café bussiness plan**

[Watch on YT](https://youtu.be/4HcVb9xai3E)

### Enviroment for GPU test:
- LM studio Vulkan 
- Windows 11
- **GPU: Intel Arc Pro B70 (32GB) + Nvidia RTX 5070 (12GB)**

### Enviroment for CPU test:
- LM studio CPU
- Windows 11
- **GPU: Intel Ultra 7 265**
- RAM: 96GB


### Prompt:
Check PROMPT-2.md

### Result:


|Test|Time for first token|PP|Generating|
|---|---|---|---|---|---|---|
|GPUs|6.45s|4612 t/s|31.58 t/s|
|Gemma 4 12B|49.76s|4546 t/s| 6.11 t/s|

===




