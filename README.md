# Helmet Detection for Construction Safety Monitoring 🪖

This project was developed as part of a Deep Learning group project. Using real construction site images, we built an object detection system to automatically identify whether workers are wearing safety helmets — addressing a practical safety problem where manual monitoring can be inconsistent and difficult to scale.

## ✨ Project Overview

**Goal:** Detect and classify objects in construction site images into two categories:

* Helmet (worker wearing a helmet)
* Head (worker without a helmet)

**Dataset:** 5,000 real construction site images (70% train / 20% validation / 10% test)

**Models Compared:**

* YOLOv11n (baseline, 3 classes) ->  YOLOv11n (refined, 2 classes)
* YOLOv8m (refined, 2 classes)
* YOLOv12n (refined, 2 classes)

**Key Insight:** In safety monitoring, recall is often more important than accuracy. Missing a helmetless worker can have more serious consequences than generating a false alarm.

---

## 📊 Key Findings

* YOLOv11n struggled with severe class imbalance, as the person class contained only ~800 instances compared to ~19,000 helmet instances.
* Refining the dataset and removing the person class improved recall from **58.0% → 84.5%** and mAP@50 from **62.9% → 91.6%**.
* The helmet class consistently outperformed the head class, likely due to its more distinctive visual features.
* The final model achieved inference speeds below **5 ms per image**, making real-time deployment feasible.

---

## 💡 What I Learned

This project showed me that data quality and class balance can have a greater impact on performance than simply choosing a more advanced model architecture.

---

## 🛠️ Tech Stack

* Python
* PyTorch
* Ultralytics YOLO
* Roboflow
* Google Colab (GPU)

---

## 🚀 Future Improvements

* Deploy on live CCTV feeds for real-time construction site monitoring
* Expand and rebalance the person class for full 3-class detection
* Test on edge devices such as Raspberry Pi or Jetson Nano
* Explore larger YOLO variants for improved detection in crowded or partially occluded scenes

---

## 👥 Team Members

* Luna Alexa
* Nysa Setiawan
* Indira Rubita Bianca
* Nazhifa Kirana Mulya Nugraha
* Franciska Olivia Putri Warae
* Angelyn Nathasya Br. Marpaung

Data Science Students — BINUS University
