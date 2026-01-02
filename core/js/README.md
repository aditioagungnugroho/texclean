# textclean

A multi-language (Python, JavaScript) text cleaning library with CLI support.

## Features

- Trim leading/trailing whitespace
- Collapse multiple spaces
- Normalize newlines
- Remove zero-width Unicode chars
- Remove non-breaking spaces
- Preserve emojis
- Preserve language accents

## Usage

### JavaScript

```javascript
import { clean } from "textclean";

const text = "  Hello   World! \u200B ";
const cleaned = clean(text, {
  trim: true,
  collapseSpaces: true,
});

console.log(cleaned); // "Hello World!"
```

### Python

```python
from textclean import clean

text = "  Hello   World! \u200B "
cleaned = clean(text, options={
    "trim": True,
    "collapse_spaces": True
})

print(cleaned) # "Hello World!"
```

### CLI

```bash
# Process a file
textclean input.txt > output.txt

# Pipe from stdin
echo "  Hello   World!  " | textclean
```

## Structure

- `core/js`: JavaScript implementation and CLI
- `core/python`: Python implementation and CLI

## AI Assistance Disclaimer

This project was developed with assistance from AI/LLMs (including GitHub Copilot, ChatGPT, and related tools), supervised by humans who occasionally knew what they were doing.
