🧠 Spoken Grammar Scoring System using Whisper & LanguageTool
This project evaluates the grammar quality of spoken English from audio files by transcribing them using OpenAI's Whisper model and analyzing the grammar of the transcription using LanguageTool.

🔧 Technologies Used
🗣️ Whisper by OpenAI — for speech-to-text transcription.

📚 LanguageTool — for grammar checking.

📦 Google Colab (Python) — for environment setup and execution.

🐍 Python Libraries: pandas, tqdm, zipfile, os

📁 Dataset Structure
The dataset zip file contains:

train.csv: List of training audio filenames with grammar scores.

test.csv: List of test audio filenames for prediction.

audios_train/: Folder with training .wav files.

audios_test/: Folder with test .wav files.

sample_submission.csv: Sample output format.

🚀 Pipeline Summary
Mount Google Drive and extract the dataset.

Load and initialize:

Whisper model (base)

LanguageTool for grammar analysis (en-US)

Define Grammar Scoring Logic:

Score from 1 (poor) to 5 (excellent) based on grammar errors per 100 words.

Process the Dataset:

Transcribe audio files using Whisper.

Analyze grammar in transcriptions.

Save results as a DataFrame with filename and grammar columns.

Export Final Predictions for the test set to test_grammar_scores.csv.

📊 Grammar Scoring Criteria
Errors per 100 words	Grammar Score
> 30	1 (Poor)
> 20	2
> 10	3
> 5	4
≤ 5	5 (Excellent)
✅ Output
test_grammar_scores.csv: Final predictions with grammar scores for test audio files.

