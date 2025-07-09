Of course, Rohan! Here's a refined and well-structured version of your project documentation. I’ve broken it into clear sections with headings, bullets, and emphasis to make it more readable and professional:

🚗 Dynamic Pricing for Urban Parking – Capstone Project
📌 Project Overview
This capstone project presents a smart pricing simulation model for urban parking lots. It dynamically adjusts parking prices in real time or batch mode based on several influencing factors. Built using Python, it demonstrates demand-driven pricing algorithms integrated with real-time data processing tools.
🎯 Objective
To simulate and implement a demand-based pricing strategy for parking spaces by accounting for:
- Parking occupancy
- Queue length
- Traffic conditions
- Special day status
- Type of vehicle (Cycle, Bike, Car, or Truck)
The model ensures that parking prices adapt intelligently to dynamic environmental and usage variables, helping optimize space utilization in urban areas.

🧰 Technologies Used
- Pathway – For real-time and static data stream processing
- Pandas – For data manipulation
- Bokeh – For data visualization and trend analysis
- Google Colab – As the development and execution environment

📂 Project Files
| File Name | Description | 
| Dynamic_Pricing_Final.ipynb | Main notebook with complete logic, implementation, and outputs | 
| dataset.csv | Input dataset containing raw parking data (no headers) | 
| final_output.csv | Output file with computed parking prices after processing | 
| README.md | Documentation of the project workflow and key components | 



🧮 Core Logic
The pricing is determined by a weighted demand formula implemented in the pricing_logic() function:
Demand = 1.5 × (occupancy / capacity) 
       + 0.5 × queue length 
       - traffic weight 
       + 2.0 × special day 
       + vehicle weight


- Vehicle Weights: Truck > Car > Bike > Cycle
- Traffic Weights: Low < Average < High
- Base Price: ₹10
- Final Price Range: Smoothly adjusted between ₹5 and ₹20, based on normalized demand

🔄 Data Flow Architecture
dataset.csv 
   ↓
Pathway ingestion (has_header=False, mode="static") 
   ↓
pricing_logic() calculation 
   ↓
Result table creation 
   ↓
Write to CSV → final_output.csv 
   ↓
File download via files.download("final_output.csv")



📈 Pricing Models
- Model 1: Linear Pricing – Basic static pricing logic (baseline)
- Model 2: Demand-Based Pricing – Active model used in simulation
- Model 3: Competitive Pricing – (Optional & not implemented) Pricing based on GPS data from nearby parking lots

🚀 How to Run
- Open Google Colab and load Dynamic_Pricing_Final.ipynb
- When prompted, upload your dataset.csv file (must be headerless)
- Execute all cells in sequence
- The model will generate and download final_output.csv automatically with computed pricing

👨‍💻 Developer Info
Project developed by Anantha Rohan Krovvidi
GitHub: KRohanGit


