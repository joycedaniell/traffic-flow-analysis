# Traffic Flow Analysis — Lane-wise Vehicle Detection, Tracking, and Counting  

**Author:** Joyce Daniel  
**Video Source:** [Traffic Camera Feed](https://www.youtube.com/watch?v=MNn9qKG2UFI)  

---

## 📌 Technical Summary  
This project implements an automated traffic flow analysis system that detects, tracks, and counts vehicles across multiple lanes in a traffic video. The solution leverages Ultralytics YOLOv5 for real-time object detection and SORT (Simple Online and Realtime Tracking) for multi-object tracking, ensuring consistent vehicle IDs across frames. Vehicles are assigned to lanes based on their position, and a CSV log is generated with vehicle ID, lane, frame number, and timestamp. An annotated video with bounding boxes, IDs, and lane-wise counts is also produced. The system is reproducible in Google Colab, requires minimal setup via `requirements.txt`, and outputs both tabular and visual results suitable for traffic analysis applications.  

---

## 📂 Repository Structure  
```
traffic-flow-analysis/
│
├── traffic_flow_analysis.ipynb   # Google Colab notebook
├── traffic_flow_analysis.py      # Python script version (exported from Colab)
├── requirements.txt              # Dependencies
├── README.md                     # This file
│
├── annotated_output.mp4          # Sample annotated output video
├── vehicle_counts.csv            # Sample output CSV
│
├── examples/                     # Example outputs
│   ├── frame_sample.png          # Sample annotated frame
│   └── csv_head.png              # First few rows of CSV
│

```

---

## ⚙️ Setup & Installation  

### Option 1: Run on Google Colab  
1. Open the notebook: `traffic_flow_analysis.ipynb`  
2. Go to **Runtime → Run all**  
3. Wait for processing to finish  
4. Download results:  
   - `annotated_output.mp4` → annotated traffic video  
   - `vehicle_counts.csv` → CSV logs  

### Option 2: Run Locally  
1. Clone this repo:  
   ```bash
   git clone https://github.com/<your-username>/traffic-flow-analysis.git
   cd traffic-flow-analysis
   ```
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
3. Run the script:  
   ```bash
   python traffic_flow_analysis.py
   ```

---

## 📊 Outputs  

- **Annotated Video**: bounding boxes, IDs, and lane counts overlayed (`annotated_output.mp4`)  
- **CSV Log**: per-vehicle log with ID, lane, frame, and timestamp (`vehicle_counts.csv`)  

**Sample Frame (from annotated video):**  
![Sample Frame](examples/frame_sample.png)

**First Rows of CSV:**  
![CSV Head](examples/csv_head.png)  

---

## 🎥 Demo Video  
👉 [Demo Link](demo/demo.mp4) *(or upload to Google Drive / YouTube and paste the link here)*  

---

## 🛠️ Notes & Tuning  
- Lane boundaries are defined in the code (`LANES = {1: (0,400), 2: (401,800), 3: (801,1280)}`). Adjust for different videos.  
- YOLO model used: `yolov5s.pt` for speed. Use larger models (`yolov5m`, `yolov5l`) for higher accuracy.  
- Confidence threshold set to `0.3`. Increase for stricter detections.  

---

## ✅ Deliverables Checklist  
- [x] Google Colab Notebook  
- [x] Python Script  
- [x] README.md (this file)  
- [x] requirements.txt  
- [x] Annotated Video Output  
- [x] Vehicle Count CSV  
- [x] Example Screenshots  
 
