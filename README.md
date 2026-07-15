# GPUs & LLMs Testing/Performance

## **Test 1**


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
```
Build a countdown timer web app in a SINGLE HTML file using vanilla HTML, CSS, and JavaScript. No frameworks, no external libraries, no separate files.

Features:

1. Input for minutes (1–120) and a Start button.
   - Reject invalid input (empty, non-numeric, out of range) by showing an error message in the page, do not use alert().
2. While running, show remaining time as MM:SS, updating every second.
3. Pause and Resume buttons (Pause only visible while running, Resume only while paused).
4. Reset button that stops the timer and clears the display back to the  initial state.
5. When the timer reaches 00:00, display "Time's up!" and flash the background color 3 times.

Rules:

- The timer must not drift: use a timestamp-based calculation, not just counting setInterval ticks.
- Starting a new timer while one is running must cancel the old one (no two intervals running at once).
- All code in one .html file, ready to open in a browser.

After the code, add a short section (3–5 bullet points) explaining how you evented timer drift and double intervals.
```

### Result:



|Modle|Context|Processing|Generating|Duration|Quality|Attempts|
|---|---|---|---|---|---|---|
|Ornith 1 9B|32k|1850 - 1550 t/s|47 - 43 t/s|< 1min|6|1|
|Gemma 4 12B|32k|1800 - 1300 t/s| 27 - 23 t/s|< 3min|8|1 / 2 to have the file creted|
|Gemma 4 26B A4B|32k|1290 - 1083 t/s|52 - 48 t/s|< 2min |9|1 for code / 2 to have the file created|
|Qwen 3.6 27B|10k|703 - 310 t/s|21 - 17 t/s|< 5min|5|2|
|Qwem 3.6 35B A3B|8k|1384 - 1198 t/s|67 - 63 t/s|x|x|x|
|GPT OSS 20B|32k|2068 - 1367 t/s|84 - 77 t/s|< 1min|2|1 for code / 2 with file creation|


[Watch on YT](https://youtu.be/Sz2oMTMLgm8)





