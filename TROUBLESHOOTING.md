# Common Errors and Solutions

## Error 1: "No module named 'tensorflow'"
**Solution:**
```bash
pip install tensorflow
```

## Error 2: "No module named 'flask'"
**Solution:**
```bash
pip install flask
```

## Error 3: "No module named 'nltk'"
**Solution:**
```bash
pip install nltk
```

## Error 4: "FileNotFoundError: chatbot_model.h5"
**Cause:** You haven't trained the model yet.

**Solution:**
```bash
python train.py
```

## Error 5: "model.save() got an unexpected keyword argument"
**Fixed!** Updated train.py to use correct save method.

## Error 6: NLTK Download Errors
**Solution:** Run this in Python:
```python
import nltk
nltk.download('punkt')
nltk.download('wordnet')
nltk.download('omw-1.4')
```

## Error 7: "Port 5000 already in use"
**Solution:** Change port in app.py:
```python
app.run(debug=True, port=5001)  # Use different port
```

## Error 8: TensorFlow warnings
**Fixed!** Added verbose=0 to suppress prediction warnings.

---

## Quick Fix - Install Everything

Run these commands in order:

```bash
# 1. Install all dependencies
pip install flask nltk tensorflow numpy

# 2. Train the model
python train.py

# 3. Run the chatbot
python app.py
```

---

## Still Having Issues?

1. **Check Python version:** Should be Python 3.8 or higher
   ```bash
   python --version
   ```

2. **Upgrade pip:**
   ```bash
   python -m pip install --upgrade pip
   ```

3. **Install specific TensorFlow version:**
   ```bash
   pip install tensorflow==2.15.0
   ```

4. **Try running in a virtual environment:**
   ```bash
   python -m venv venv
   venv\Scripts\activate  # On Windows
   pip install -r requirements.txt
   ```
