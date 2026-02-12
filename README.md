# ADAPTIVE API RATE LIMITING USING HEURISTIC PATTERN CLASSIFICATION AND TOKEN BUCKET OPTIMIZATION

## Project Overview
This repository contains the implementation of a lightweight Application Programming Interface (API) middleware designed to provide adaptive security for Micro, Small, and Medium Enterprises (MSMEs). The system addresses the gap in traditional static rate limiting by utilizing **Heuristic Pattern Classification** to distinguish between human-like and robotic traffic patterns in real-time. By dynamically optimizing **Token Bucket** parameters, the middleware ensures high service availability for legitimate users while mitigating automated abuse with minimal processing delay.

## Key Features
* **Heuristic Classification Engine:** Categorizes API traffic into normal, bursty, and suspicious profiles based on request rate, interval regularity (jitter), and burst persistence.
* **Dynamic Parameter Optimization:** Automatically adjusts the Token Bucket refill rate ($r$) and bucket capacity ($b$) based on real-time classification output.
* **Reverse Proxy Implementation:** Developed as a high-performance middleware using FastAPI to decouple security logic from core application business logic.
* **Resource Efficiency:** Specifically designed for resource-constrained environments, prioritizing lightweight rule-based logic over computationally intensive machine learning.

The system follows an **Input-Process-Output (IPO)** framework:
1. **Input:** API traffic metadata, timing intervals, and initial rate limiting configurations.
2. **Process:** Real-time monitoring, heuristic-based behavioral classification, and dynamic parameter adjustment.
3. **Output:** Optimized request acceptance, performance reports, and classification accuracy (FPR/FNR).

## License
This project is for academic purposes as part of a undergraduate research study at the University of Cabuyao. Distributed under the MIT License.
