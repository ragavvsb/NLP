# Quick Start Guide

## Installation

```bash
# Install dependencies
pip install -r requirements.txt
```

## Training the Model

```bash
# Train the chatbot model
python train.py
```

This will create:
- `chatbot_model.h5` - The trained neural network
- `words.pkl` - Preprocessed vocabulary
- `classes.pkl` - Intent classes

## Running the Chatbot

### Web Interface (Recommended)

```bash
python app.py
```

Open browser: http://localhost:5000

### Command Line

```bash
python chat.py
```

Type messages and press Enter. Type 'quit' to exit.

## Customizing Responses

Edit `intents.json` to add new intents, then retrain:

```bash
python train.py
```
