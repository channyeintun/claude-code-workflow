# 🤖 Local AI Guide: Qwen3-Coder on M1 (8GB RAM)

Based on your system specs (**Apple M1, 8GB RAM**), here is how you can run **Qwen3-Coder**:

## 1. The Verdict
The **Qwen3-Coder** series is incredibly powerful, but its primary specialized models are quite large for an 8GB setup.

- **Qwen3-Coder:30b (The Flash Model)**: This is the smallest *dedicated* Coder version of Qwen3. It uses a "Mixture of Experts" (MoE) where only 3.3B parameters are active at once, but the full weights still take up ~19GB space. 
- **Can it run?** Technically yes via Ollama, but it will cause **severe disk swapping** on your 8GB machine. It will be slow.

## 2. Optimized Setup (Ollama)

For the best experience on your 8GB M1, I recommend these commands:

### Option A: The "Pure" Qwen3 Coder (Might be slow)
```bash
ollama run qwen3-coder:30b
```
*Try this first. If it takes more than 5 seconds to respond, your machine is swapping too much.*

### Option B: The "Lite" Qwen3 Experience (Recommended for Speed)
Use the **dense** version of Qwen3. While not "Coder" branded, the base Qwen3 family is extremely good at code.
```bash
ollama run qwen3:4b
```
*This will run instantly and smoothly on your machine.*

### Option C: The Reliable Pro (Best for daily coding)
If you need a dedicated "Coder" model that feels like it has zero lag:
```bash
ollama run qwen2.5-coder:3b
```

## 3. Free Local Coding: Claude Code + Ollama
You can now run **Claude Code** (the agentic CLI tool) for free using your local Ollama models!

### Setup
1. **Configure Claude Code**:
   Run this command once to point it to your local Ollama server:
   ```bash
   ollama launch claude --config
   ```
2. **Run it locally**:
   Launch it using your preferred local model:
   ```bash
   ollama launch claude --model qwen3-coder:30b
   ```

## 4. Integration with your New Setup
- **Ghostty**: Open Claude in one pane and `lazygit` in another. Claude will use your local M1 chip for intelligence, while Ghostty provides the beautiful blurred interface.
- **Neovim**: Use the `gen.nvim` plugin to interface with `qwen3-coder:30b` directly inside your editor.

---
> [!TIP]
> Since you have **8GB RAM**, remember to quit other memory-heavy apps when running Claude locally for the best agentic performance!
