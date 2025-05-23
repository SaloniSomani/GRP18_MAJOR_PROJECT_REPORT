
#  Multimodal Sarcasm Detection

##  Project Overview

**Multimodal Sarcasm Detection** aims to identify sarcastic expressions by analyzing multiple data modalities—text, audio, and visual cues. Traditional text-based approaches often fall short in detecting sarcasm, as it frequently relies on vocal tone, facial expressions, and contextual nuances. By leveraging multimodal data, this project enhances the accuracy of sarcasm detection systems.

##  Dataset: MUStARD++ Balanced

The [MUStARD++ Balanced dataset](https://github.com/cfiltnlp/MUStARD_Plus_Plus) is a curated collection designed for multimodal sarcasm detection research. It comprises:

* **Textual Transcripts**: Verbatim transcriptions of dialogues from the TV show *House MD*.
* **Utterance Video Clips**: Short video segments focusing on individual utterances, capturing facial expressions and gestures.
* **Context Video Clips**: Longer video sequences providing contextual background for each utterance.

The dataset is balanced, containing 1,365 instances—691 labeled as sarcastic and 674 as non-sarcastic—ensuring unbiased model training.

##  Model Architecture

This project employs a multimodal approach, integrating state-of-the-art models for each data modality:

* **Text Modality**: [BERT (Bidirectional Encoder Representations from Transformers)](https://huggingface.co/bert-base-uncased) for textual feature extraction.
* **Audio Modality**: [Wav2Vec 2.0](https://huggingface.co/facebook/wav2vec2-base-960h) for capturing acoustic features.
* **Visual Modality**: [TimesFormer](https://github.com/facebookresearch/TimeSformer) for analyzing visual cues from video frames.

The features extracted from each modality are fused to perform accurate sarcasm classification.

## Installation

### Prerequisites

Ensure you have the following installed:

* Python 3.8 or higher
* Git

### Clone the Repository

```bash
git clone https://github.com/your-username/multimodal-sarcasm-detection.git
cd multimodal-sarcasm-detection
```

### Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

**`requirements.txt` includes:**

```
torch==1.11.0
transformers==4.18.0
numpy==1.22.3
pandas==1.4.2
scikit-learn==1.0.2
matplotlib==3.5.1
Pillow==9.1.0
tqdm==4.64.0
opencv-python==4.5.5.64
jieba==0.42.1
torchvision==0.12.0
```

## 🚀 Usage

### Data Preparation

1. **Download the MUStARD++ Balanced dataset** from the [official repository](https://github.com/cfiltnlp/MUStARD_Plus_Plus).
2. **Organize the dataset** as follows:

```
data/
├── transcripts/
├── utterance_videos/
└── context_videos/
```

---

*This project leverages the MUStARD++ Balanced dataset for advancing research in multimodal sarcasm detection.*

---

