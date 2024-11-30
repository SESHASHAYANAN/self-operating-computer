<h1 align="center">Self-Operating computer Using multimodal models Framework</h1>

<p align="center">
  <strong>A framework to enable multimodal models to operate a computer.</strong>
  <strong>Unlock hands-free computing: AI-powered voice control that bridges vision, language, and interaction across cutting-edge multimodal models.</strong>
</p>
<p align="center">
  Using the same inputs and outputs as a human operator, the model views the screen and decides on mouse and keyboard actions to reach an objective. 
</p>

## Key Features
- **Compatibility**: Designed for various multimodal models.
- **Integration**: Currently integrated with ** Gemini Pro Vision,GPT-4o, Claude 3 and LLaVa.**
- **Future Plans**: Support for additional models.
## Demo

https://github.com/OthersideAI/self-operating-computer/assets/42594239/9e8abc96-c76a-46fb-9b13-03678b3c67e0
## Run `Self-Computing`

1. **Install the project**
```
pip install self-operating-computer
```
2. **Run the project**
```
operate
```
 

3. **Give the Terminal app the required permissions**: As a last step, the Terminal app will ask for permission for "Screen Recording" and "Accessibility" in the "Security & Privacy" page of Mac's "System Preferences".
4. **Enter your OpenAI Key**:  If you need you change your key at a later point, run `vim .env` to open the `.env` and replace the old key.

## Using `operate` Modes

### Multimodal Models  `-m`
An additional model is now compatible with the Self Operating Computer Framework. Try Google's `gemini-pro-vision` by following the instructions below. 

Start `operate` with the Gemini model
```
operate -m gemini-pro-vision
```

**Enter your Google AI Studio API key when terminal prompts you for it** If you don't have one, you can obtain a key [here](https://makersuite.google.com/app/apikey) after setting up your Google AI Studio account. You may also need [authorize credentials for a desktop application](https://ai.google.dev/palm_docs/oauth_quickstart). It took me a bit of time to get it working.


### Optical Character Recognition Mode 'gemini-pro-vision'
The Self-Operating Computer Framework now integrates Optical Character Recognition (OCR) capabilities with the 'gemini-pro-vision' mode. This mode gives GPT-4 and and 'gemini-pro-visiona hash map of clickable elements by coordinates. GPT-4 and 'gemini-pro-vision can decide to `click` elements by text and then the code references the hash map to get the coordinates for that element 'gemini-pro-vision wanted to click. 

Based on recent tests, OCR performs better than `som` and vanilla 'gemini-pro-vision' and  'gemini-pro-vision' so we made it the default for the project. To use the OCR mode you can simply write: 

 `operate` or `operate -m gpt-4-with-ocr` will also work. 

### Set-of-Mark Prompting `-m gpt-4-with-som`
The Self-Operating Computer Framework now supports Set-of-Mark (SoM) Prompting with the `gpt-4-with-som` command. This new visual prompting method enhances the visual grounding capabilities of large multimodal models.

Learn more about SoM Prompting in the detailed arXiv paper: [here](https://arxiv.org/abs/2310.11441).

For this initial version, a simple YOLOv8 model is trained for button detection, and the `best.pt` file is included under `model/weights/`. Users are encouraged to swap in their `best.pt` file to evaluate performance improvements. If your model outperforms the existing one, please contribute by creating a pull request (PR).

Start `operate` with the SoM model

```

operate -m gemini-pro-vision
operate -m gpt-4-with-som
```

## Compatibility
- This project is compatible with Mac OS, Windows, and Linux (with X server installed).

## OpenAI Rate Limiting Note
The ```gpt-4o``` and  model is```gemini-pro-vision``` required. To unlock access to this model, your account needs to spend at least \$5 in API credits. 
