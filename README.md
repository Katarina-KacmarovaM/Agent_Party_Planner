# Agent Party Planner 🎉

Get ready to throw the ultimate bash! This project shows off how to build a fun, multi-step AI agent using the awesome [smolagents](https://github.com/bigscience-workshop/smol-agents) framework.
From tasty menus and dazzling decorations to stylish dress codes and exciting activities – this agent’s got your party covered! Let’s celebrate smarter! 🥳
---

## Features

- Multi-step reasoning with smolagents
- Custom tools for menu, decorations, dress code, and activities
- Integration with Hugging Face Inference API
- Example of using `additional_authorized_imports` for safe Python imports inside the agent

---

## Installation

```sh
git clone https://github.com/Katarina-KacmarovaM/Agent_Party_Planner.git
cd Agent_Party_Planner
pip install -r requirements.txt
```

---

## Usage

1. Open `frame_smallagents.ipynb` in Jupyter or VS Code.
2. Run the notebook cells step by step.
3. Log in to Hugging Face when prompted.
4. Interact with the agent using natural language instructions.

**Example:**
```python
agent.run(
    "Prepare a menu for birthday party in summer season. "
    "Give also proper dress code in soft summer color palette for guests and decorations for the birthday party in summer season. "
    "Also suggest some activities for the birthday party in summer season."
)
```

---

## How to Use Additional Imports

By default, smolagents restricts Python imports for security.  
If your tool needs extra imports (like `datetime`), use the `additional_authorized_imports` parameter:

```python
agent = CodeAgent(
    tools=[suggest_menu],
    model=InferenceClientModel(),
    additional_authorized_imports=["numpy", "time", "datetime"]
)
```

---

## Project Structure

- `frame_smallagents.ipynb` — Main notebook with all code and examples
- `README.md` — Project documentation

---

## Requirements

- Python 3.8+
- `smolagents`
- `huggingface_hub`

---

## License

MIT License

---

## Acknowledgements

- [smolagents](https://github.com/bigscience-workshop/smol-agents)
- [Hugging Face](https://huggingface.co/)
