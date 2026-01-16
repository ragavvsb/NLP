# AI Virtual Assistant for Customer Query Handling

This project implements an AI-powered virtual assistant using Natural Language Processing (NLP) and Deep Learning to handle customer queries intelligently.

## Features

- 🤖 **Intelligent Response System**: Uses Deep Learning to understand and respond to customer queries
- 💬 **Modern Web Interface**: Beautiful, responsive chat interface with real-time interactions
- 🎯 **Intent Recognition**: Accurately identifies user intent and provides relevant responses
- 🚀 **Easy to Use**: Simple setup and intuitive interface

## Project Structure

```
NLP/
├── app.py                 # Flask backend server
├── train.py              # Model training script
├── chat.py               # CLI chatbot interface
├── intents.json          # Training data (intents, patterns, responses)
├── requirements.txt      # Python dependencies
├── templates/
│   └── index.html       # Web interface
└── static/
    ├── style.css        # Styling
    └── script.js        # Frontend logic
```

## Installation

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Download NLTK data (done automatically during training):
```python
import nltk
nltk.download('punkt')
nltk.download('wordnet')
```

## Usage

### Step 1: Train the Model

Run the training script to create the chatbot model:

```bash
python train.py
```

This will:
- Process the intents from `intents.json`
- Train a neural network model
- Save the model as `chatbot_model.h5`
- Save preprocessed data (`words.pkl`, `classes.pkl`)

### Step 2: Run the Chatbot

**Option A: Web Interface (Recommended)**

```bash
python app.py
```

Then open your browser and navigate to: `http://localhost:5000`

**Option B: Command Line Interface**

```bash
python chat.py
```

Type your messages and press Enter. Type 'quit' to exit.

## Customization

### Adding New Intents

Edit `intents.json` to add new conversation patterns:

```json
{
  "tag": "your_intent_name",
  "patterns": ["example question 1", "example question 2"],
  "responses": ["response 1", "response 2"],
  "context": [""]
}
```

After modifying `intents.json`, retrain the model by running `python train.py`.

## Technologies Used

- **Python 3.x**
- **TensorFlow/Keras**: Deep Learning framework
- **NLTK**: Natural Language Processing
- **Flask**: Web framework
- **HTML/CSS/JavaScript**: Frontend interface

## Model Architecture

- Input Layer: Bag of words representation
- Hidden Layer 1: 128 neurons with ReLU activation
- Dropout: 50% (prevents overfitting)
- Hidden Layer 2: 64 neurons with ReLU activation
- Dropout: 50%
- Output Layer: Softmax activation (multi-class classification)

## License

This project is open source and available for educational purposes.
