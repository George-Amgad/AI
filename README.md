# Stable Diffusion Web Demo (Pollinations.ai)

## Overview
This simple web application demonstrates how to integrate Stable Diffusion image generation into a plain HTML page using the Pollinations.ai public API. No authentication, backend server, or external libraries are required.

## Features
- Text input for user prompts
- "Generate Image" button to request image creation
- Loading indicator to inform the user while the model processes the prompt
- Display of the generated image upon completion

## Usage
1. Open the `index.html` file in a web browser.
2. Enter a descriptive prompt into the text input field.
3. Click the **Generate Image** button.
4. View the message "Please wait while the AI generates the image…" during processing.
5. Observe the generated image displayed below the prompt.

## File Structure
```
project-root/
├── index.html   # Main HTML file with embedded JavaScript
└── README.md    # This documentation file
```

## index.html Structure
- `<input id="prompt">` – Accepts the user's text prompt.
- `<button id="generate">` – Triggers the image generation request.
- `<p id="loading">` – Displays a loading message during API calls.
- `<img id="output">` – Shows the returned image.
- `<script>` section – Contains JavaScript logic to call Pollinations.ai API.

## How It Works
1. The user enters a prompt and clicks **Generate Image**.
2. JavaScript constructs a URL of the form:
   ```
   https://image.pollinations.ai/prompt/{encoded_prompt}
   ```
3. A `fetch()` request is sent to Pollinations.ai.
4. The response is retrieved as a binary blob representing the image.
5. `URL.createObjectURL(blob)` generates a local URL for the image.
6. The `<img>` element’s `src` attribute is set to the object URL, displaying the image.

## Requirements
- A modern web browser with support for `fetch()` and `URL.createObjectURL()`.
- Internet access to reach the Pollinations.ai service.

## License
This project is provided under the MIT License. Pollinations.ai is open-source and free to use without authentication or tokens.

---

**End of Documentation**

