# Music-Generation-with-RNN-LSTM

### notebook/TF_Part2_Music_Generation.ipynb

This notebook walks through the process of generating music using Recurrent Neural Networks (RNNs) and LSTM architecture with TensorFlow. Here’s a detailed breakdown:

#### **Introduction & Setup**
- The notebook starts with links to MIT Deep Learning, Colab, and GitHub, plus copyright/license info.
- It explains the goal: building an RNN to generate music in ABC notation, a text-based format for folk tunes.

#### **Dependencies**
- Installs and imports required libraries: TensorFlow, NumPy, Comet ML for experiment tracking, MIT Deep Learning package, etc.
- Checks for GPU availability and sets up the API key for Comet ML.

#### **Dataset**
- Loads thousands of Irish folk songs in ABC notation.
- Shows a sample song as text, e.g.:
  ```
  X:1
  T:Alexander's
  M:C|
  L:1/8
  K:D Major
  (3ABc|dAFA DFAd|fdcd FAdf|...
  ```
- Converts an ABC song to audio and displays a player widget to listen to the result.

#### **Preprocessing**
- Prepares the dataset for training:
  - Combines all songs into one large string.
  - Creates a mapping from characters to integers and vice versa.
  - Converts songs to numerical sequences for model input.
- Shows vocab size and the mapping, e.g. how "X", "T", "M" are encoded.

#### **Model Architecture**
- Builds an LSTM-based neural network using TensorFlow/Keras:
  - Embedding layer, LSTM layers, Dense output.
- Model summary and diagram are displayed.
- Hyperparameters like sequence length, batch size, and learning rate are set.

#### **Training**
- Trains the model on the music data:
  - Loss and accuracy are tracked and plotted.
  - Uses callbacks for early stopping and best model checkpointing.
- Shows training progress and plots, e.g.:
  - _Loss curve image_
  - _Sample training logs_

#### **Music Generation**
- Uses the trained model to generate new music sequences:
  - Starts from a prompt string.
  - Samples next characters with temperature control for randomness.
- Converts generated sequences back to ABC notation, then to audio.
- Displays generated music text and a player to listen to the output.

#### **Visualization & Evaluation**
- Plots training/validation loss.
- Shows generated music samples (both ABC text and playable audio).
- Discusses differences between real and generated music.

#### **Conclusion**
- Summarizes achievements and limitations.
- Suggests improvements (e.g., using deeper models, more data, alternative sampling strategies).

---

**Outputs and Visuals:**  
- Example ABC notation songs  
- Playable audio (via IPython widgets)  
- Model summary and architecture diagram  
- Plots of loss/accuracy curves  
- Sample generated music (text and audio)

---
