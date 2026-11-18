EmotionLens - Emotion Detection from Text
=========================================

FOLDER LAYOUT (must look like this)
  emotion_app\
    app.py
    index.html
    run.bat
    requirements.txt
    emotion_bert\        <- from emotion_bert.zip (Colab)
      config.json
      model.safetensors
      metrics.json
      tokenizer files...

STEP 1 - Train the model in Google Colab (only once, ~15 min)
  1. Go to colab.research.google.com > File > Upload notebook
  2. Pick Emotion_Detection_Colab_v2.ipynb
  3. Runtime > Change runtime type > T4 GPU > Save
  4. Runtime > Run all
  5. emotion_bert.zip downloads at the end (~390 MB)
     If it doesn't: Files pane (folder icon) > content > emotion_bert.zip > Download

STEP 2 - Put the model in place
  Extract emotion_bert.zip into this emotion_app folder.
  If you get emotion_app\content\emotion_bert, move emotion_bert up one level.

STEP 3 - Install (only once), in PowerShell inside this folder
  pip install torch --index-url https://download.pytorch.org/whl/cpu
  pip install -r requirements.txt

STEP 4 - Run
  Double-click run.bat
  (or in PowerShell: python app.py, then open http://127.0.0.1:5000)

STOP the server: press Ctrl + C in the window.
