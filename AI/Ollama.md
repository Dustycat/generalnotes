# Running Ollama

Option 1: Run with the windows app
Option 2: Run from command line. Model name: llama3
```
ollama run model_name
```
# Models

* **Best for Low-End Hardware:** `ollama run qwen2.5:1.5b` or `ollama run llama3.2` (3B).
* For reasoning, math, or coding, **deepseek-r1 (specifically 7B or 14B)** is highly recommended. 
* For a reliable general-purpose model, **Mistral (7B)** is also a top choice.

**Tips for Beginners:**

- **Hardware Check:** If you have 8GB-16GB RAM/VRAM, stick to 7B-14B models. If you have less, choose 1B-3B models.
- **Quantization:** Use the default, or look for `q4_k_m` or `q5_k_m` for the best balance of size and intelligence.
- **How to Run:** Open your terminal and type the `ollama run <model_name>` command (e.g., `ollama run qwen2.5`).

Recommended models for Nvidia 4060
* AI recommends: **[Llama 3 (8B)](https://www.google.com/search?q=Llama+3+%288B%29&oq=nvidia+geforce+rtx+4060%2C+which+ai+model+is+best&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIHCAEQIRigATIHCAIQIRigATIHCAMQIRigATIHCAQQIRigATIHCAUQIRigATIHCAYQIRirAjIHCAcQIRirAjIHCAgQIRiPAjIHCAkQIRiPAtIBCTE0MzkwajBqNKgCALACAA&sourceid=chrome&ie=UTF-8&mstk=AUtExfD7e--dboreIoPwk8DXhpx3nag3jd2QqyRJRpe7OEr9TN_kkk4c_ysdMuvuCrMPeh1wI5R1Gsoe5tQLmLEnqemOI5uIxV7ziU-yWnF-gegcqyQGazYG6yRZ7e8r7zwSQKD60koAE_qqoO14d6y_lBxorGWYNyQmp2376yiDTU8_NNA98gdp6FvpfqOlzwLb2RTJUkUPyoI9G4qtTtV8GevA0ASpSolXx5zDYvHinnTux0hVl0LIcfhZvs2BrAEpxlvG01Lnm1dltDEkoHolTM4b&csui=3&ved=2ahUKEwjmspqTrdmSAxXFOzQIHRsTCLYQgK4QegQIARAC)**, **[Mistral (7B)](https://www.google.com/search?q=Mistral+%287B%29&oq=nvidia+geforce+rtx+4060%2C+which+ai+model+is+best&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIHCAEQIRigATIHCAIQIRigATIHCAMQIRigATIHCAQQIRigATIHCAUQIRigATIHCAYQIRirAjIHCAcQIRirAjIHCAgQIRiPAjIHCAkQIRiPAtIBCTE0MzkwajBqNKgCALACAA&sourceid=chrome&ie=UTF-8&mstk=AUtExfD7e--dboreIoPwk8DXhpx3nag3jd2QqyRJRpe7OEr9TN_kkk4c_ysdMuvuCrMPeh1wI5R1Gsoe5tQLmLEnqemOI5uIxV7ziU-yWnF-gegcqyQGazYG6yRZ7e8r7zwSQKD60koAE_qqoO14d6y_lBxorGWYNyQmp2376yiDTU8_NNA98gdp6FvpfqOlzwLb2RTJUkUPyoI9G4qtTtV8GevA0ASpSolXx5zDYvHinnTux0hVl0LIcfhZvs2BrAEpxlvG01Lnm1dltDEkoHolTM4b&csui=3&ved=2ahUKEwjmspqTrdmSAxXFOzQIHRsTCLYQgK4QegQIARAD)**, and **[Stable Diffusion XL (SDXL) or Flux](https://www.google.com/search?q=Stable+Diffusion+XL+%28SDXL%29+or+Flux&oq=nvidia+geforce+rtx+4060%2C+which+ai+model+is+best&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIHCAEQIRigATIHCAIQIRigATIHCAMQIRigATIHCAQQIRigATIHCAUQIRigATIHCAYQIRirAjIHCAcQIRirAjIHCAgQIRiPAjIHCAkQIRiPAtIBCTE0MzkwajBqNKgCALACAA&sourceid=chrome&ie=UTF-8&mstk=AUtExfD7e--dboreIoPwk8DXhpx3nag3jd2QqyRJRpe7OEr9TN_kkk4c_ysdMuvuCrMPeh1wI5R1Gsoe5tQLmLEnqemOI5uIxV7ziU-yWnF-gegcqyQGazYG6yRZ7e8r7zwSQKD60koAE_qqoO14d6y_lBxorGWYNyQmp2376yiDTU8_NNA98gdp6FvpfqOlzwLb2RTJUkUPyoI9G4qtTtV8GevA0ASpSolXx5zDYvHinnTux0hVl0LIcfhZvs2BrAEpxlvG01Lnm1dltDEkoHolTM4b&csui=3&ved=2ahUKEwjmspqTrdmSAxXFOzQIHRsTCLYQgK4QegQIARAE)** (using GGUF/quantization)
* glm-4.7-flash (19GB) 32B model seems to hang for my graphics card. This makes sense because it ideally need 16-32 VRAM but the Nvidia 4060 is 8GB
* 

VS Code
* llama3 seems to be incompatible with roocode
* AI recommends qwen3:8b

Thomas
* Gemini3
* opus4.7
* perplexity

# Managing Models

Default model location
```
C:\Users\hewan\.ollama\models
```

To change the location, start the app in windows, and click settings on the right side. Note that putting the model on an SD drive will load slower

List models
```
ollama list
```

Remove models
```
ollama rm mode_name
```

# Server Location

```
http://localhost:11434
```

Port Number: 11434 (a play on the word "llama" in leetspeak)

API: http://localhost:11434/api

# Setting up AI with obsidian

Copilot plugin
* Setup: I haven't confirmed if this is really needed
```
export OLLAMA_ORIGINS="app://obsidian.md*"
```
* Go Copilot plugin settings
* 
# Questions

1. Can ollama access a URL?
	1. Possibly only in turbo (cloud?) mode
	2. Go to the ollama app->settings->Airplane mode to be completely offline?
2. Alternative to ollama is llama.cpp

# Summary of Ollama

1. Very easy to install and add local models on the fly. The server setup is also very easy. Thus allowing either a GUI (Graphical User Interface) or a CLI (Command Line Interface). The CLI runs faster but I feel more comfortable using the GUI.
2. With an Nvidia 4060 (8GB VRAM) running on a laptop, the best model for me is llama3. It's responsive and gives decent answers. I also tried qwen3:8b model and it takes longer to generate an answer.
3. 14b and above models are practically unusable. It takes forever to load the model and the modes takes forever to generate an answer.
4. I believe you need around a 32b model to interface reliably as a code assistant for VS code. That means I will need 2 to 4 Nvidia 4060 graphics card. 
5. My next step is to look into how ollama can integrate with Obsidian notes.