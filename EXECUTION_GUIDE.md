# 🚀 EXECUTION GUIDE - AI Chatbot

## Step-by-Step Instructions

### STEP 1: Install Dependencies

Open terminal in the NLP folder and run:

```bash
pip install flask nltk tensorflow numpy
```

**OR** use the requirements file:

```bash
pip install -r requirements.txt
```

---

### STEP 2: Train the Model

Run the training script:

```bash
python train.py
```

**What happens:**
- Downloads NLTK data automatically
- Processes intents.json
- Trains the neural network (takes 2-5 minutes)
- Creates 3 files:
  - `chatbot_model.h5`
  - `words.pkl`
  - `classes.pkl`

**Expected output:**
```
[nltk_data] Downloading package punkt...
[nltk_data] Downloading package wordnet...
Training data created
Epoch 1/200
...
Model created and saved
```

---

### STEP 3: Run the Chatbot

**Option A: Web Interface (Recommended)**

```bash
python app.py
```

Then open your browser and go to:
```
http://localhost:5000
```

**Option B: Command Line**

```bash
python chat.py
```

Type messages and press Enter. Type 'quit' to exit.

---

## Quick Commands Summary

```bash
# 1. Install
pip install -r requirements.txt

# 2. Train
python train.py

# 3. Run Web App
python app.py
# Then visit: http://localhost:5000

# OR Run CLI
python chat.py
```

---

## Troubleshooting

**Error: "No module named 'flask'"**
- Run: `pip install flask`

**Error: "No module named 'tensorflow'"**
- Run: `pip install tensorflow`

**Error: "Model not found"**
- You need to run `python train.py` first

**Training is slow**
- Normal! Training takes 2-5 minutes on most computers

---

## What to Expect

### After Training:
You'll see new files created:
- ✅ chatbot_model.h5 (the AI model)
- ✅ words.pkl (vocabulary)
- ✅ classes.pkl (intent categories)

### Web Interface:
- Beautiful purple/blue gradient design
- Chat bubbles for messages
- Typing indicators
- Quick action buttons

### Try These Messages:
- "Hello"
- "What services do you offer?"
- "How can you help me?"
- "Thank you"
- "Goodbye"
