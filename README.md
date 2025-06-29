
# ⚽️ Player Re-Identification & Tracking from Single Video

A **YOLO + ReID + Kalman Filter-based Player Tracking System** for football (or any team sport) that assigns **persistent IDs to players**, even if they leave and re-enter the frame. IDs are displayed with **human-readable labels like "Player 1", "Player 2"**, etc.

---

## 📦 Features

- ✅ Detects players using YOLOv11 (fine-tuned model).
- ✅ Assigns consistent IDs even if players temporarily leave the frame.
- ✅ Combines **motion tracking (Kalman Filter + IoU)** with **appearance-based ReID (TorchReID)**.
- ✅ Outputs a playable `.mp4` video with bounding boxes and labels like `Player 1`.
- ✅ Fully works locally on **CPU or GPU**.

---

## 🔧 Requirements

### ✅ Python Version:
- **Python 3.8 or higher**

### ✅ Dependencies:
- ultralytics (YOLOv11)
- opencv-python
- numpy
- torch
- torchvision
- torchreid
- filterpy
- scikit-learn

### ✅ Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 🚀 Folder Structure

```
player_tracking/
├── yolo_model.pt           # YOLOv11 trained weights
├── Inputs                  # Input videos
│   └── 15sec_input_720.mp4
├── Output                  # Processed output videos
│   └── output_new.mp4
├── player_ReID.ipynb      # Main tracking script
```

---

## ⚙️ Setup & Running

### ✅ Step 1: Clone the repository

```bash
git clone https://github.com/KarthikeyatheDev/Player-ReID
cd Player-ReID
```

### ✅ Step 2: Install dependencies

```bash
pip install -r requirements.txt
```

### ✅ Step 3: Add your YOLOv11 trained model

Place your YOLO model (trained on players and ball) into the root folder.  
Example filename: **`betst.pt`**

### ✅ Step 4: Add input video

Put your input video into the `Inputs/` folder.  
Example: **`15sec_input_720.mp4`**

### ✅ Step 5: Run the tracker

Click Run all in the Notebook.

### ✅ Step 6: Check output

The output video will be saved in:

```
Output/output_new.mp4
```

Open with any media player (VLC, Windows Media Player, etc.).

---

## 💻 Environment Tips

- 🚀 **GPU Recommended:** for faster processing.(~5m)
- ✅ Works on CPU but slower.(~24m)
- 📦 Tested on:
  - Windows 10/11

---

## 📈 Example Output

- Bounding boxes with labels like:

```
Player 1
Player 2
Player 3
...
```

- Smooth tracking with consistent IDs even if players leave and re-enter the frame.

---

## 📊 Future Improvements

- [ ] Export player trajectories to CSV
- [ ] Draw movement trails
- [ ] Multi-camera ReID
- [ ] Streamlit web dashboard for real-time tracking
- [ ] Metrics computation (IDF1, MOTA, MOTP)

---

## 🤖 Credits

- **YOLOv11:** [Ultralytics](https://github.com/ultralytics/ultralytics)  
- **TorchReID:** [Kaiyang Zhou et al.](https://github.com/KaiyangZhou/deep-person-reid)  
- Tracking pipeline inspired by **ByteTrack**, **DeepSORT**, and **SORT** concepts.

---

## 🏆 License

This project is for **research and educational purposes.**  

---

## 🚀 Author

**Ch.M.Karthikeya** — Built with effort and caffeine ☕.

---

## ⭐️ Feel free to suggest improvements or report issues!

---

