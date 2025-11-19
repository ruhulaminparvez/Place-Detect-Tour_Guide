# Place Detection – AI Tour Guide

According to recent reports from the World Tourism Organization (WTO), international tourist arrivals surpassed 1,235 million in 2017, outpacing the 3.9 % growth recorded in 2015 and showing a remarkable jump from 2001. As more people travel, they increasingly rely on tour guides to make their journeys reliable, yet finding a trustworthy guide remains difficult and often leads to avoidable challenges. To address this gap, we propose an AI-based Tour Guide system that lets travelers communicate through their phones, combining modern computer-science technologies to deliver dependable guidance anywhere. While prior literature explores similar ideas, most solutions are limited in scope; by embracing fast-evolving technology, we can hand over this responsibility to a scalable AI-driven system.

## Project Overview
This repository houses an AI assistant that detects notable landmarks from user images and summarizes key facts, forming the backbone of an intelligent tour companion. The system includes:
- Computer-vision pipelines for landmark detection (multiple iterations under `Detect Landmark v1` and `Detect Landmark v2`)
- A React-based web interface (`Tour Guide (Web App)`) that surfaces detections and guidance information

Live demo:
- [AI Tour Guide](https://ai-tour-guide-web.vercel.app)

**Authors**
Ruhul Amin Parvez · Khandoker Md. Mashiur Rahman

**Faculty Supervisor**
Dr. Sheak Rashed Haider Noori
Associate Professor & Associate Head, Department of CSE, Daffodil International University

## Technologies
- Python 3.9+, Streamlit, TensorFlow/Keras, OpenCV (landmark detection prototypes)
- Jupyter/Google Colab for experimentation (`Detect Landmark v2/CoLab/LM_Detection.ipynb`)
- React 18, Vite tooling (via `create-react-app` structure), CSS Modules for the tour-guide interface
- Node.js 18+ (front-end tooling)

## Repository Structure
```
├── Detect Landmark v1/
│   ├── Images/                  # Sample landmark photos for baseline model
│   ├── Logo/                    # Branding assets
│   ├── landmark-detect.py       # Streamlit/TensorFlow inference script
│   └── requirements.txt         # Python dependencies for v1 pipeline
├── Detect Landmark v2/
│   ├── CoLab/LM_Detection.ipynb # Improved detection notebook
│   ├── Images/                  # Expanded landmark dataset
│   ├── Labels/*.csv             # Label maps for classifier
│   └── PyCharm/LM_Detection.py  # Refined Python implementation
├── Tour Guide (Web App)/
│   ├── package.json             # React app dependencies/scripts
│   ├── public/                  # Static assets and HTML shell
│   └── src/                     # React components, styles, assets
└── README.md
```

## Getting Started
1. **Landmark detection**
   - `cd "Detect Landmark v1"`
   - `python -m venv .venv && .venv\Scripts\activate`
   - `pip install -r requirements.txt`
   - `streamlit run landmark-detect.py`
2. **Web app**
   - `cd "Tour Guide (Web App)"`
   - `npm install`
   - `npm start`

## Sample Output
Below are screenshots from the `Demo Image` directory that illustrate how the AI tour guide surfaces landmark insights:

![Sample 1 – Search place overview](Demo%20Image/one.png)
![Sample 2 – Detected restaurants](Demo%20Image/two.png)
![Sample 3 – Detected attractions](Demo%20Image/three.png)

## Contributing
Feel free to open issues or submit pull requests for enhancements, bug fixes, or documentation improvements. Please include screenshots or logs when reporting UI/UX or inference problems.