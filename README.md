# 🛡️ DDoS Attack Detection and Prevention using SDN and Machine Learning.


![Ddos-attack-main-featured-image](https://github.com/user-attachments/assets/f65ce92f-1c3e-40bd-a7b0-2d74b0611161)   


This project focuses on the detection and mitigation of Distributed Denial of Service (DDoS) attacks in Software-Defined Networking (SDN) environments using Machine Learning (ML) techniques. The aim is to provide an intelligent, real-time system that identifies malicious traffic patterns and prevents network disruption by enabling dynamic traffic control via SDN controllers.



![Schematic-diagram-of-a-DDoS-attack](https://github.com/user-attachments/assets/9e3e2209-8467-4f65-b97e-d208111570f7)



🎯 Objective:    
1.To detect DDoS attacks in SDN networks with high accuracy using machine learning.

2.To analyze real network traffic and extract relevant features for classification.

3.To classify and filter normal vs. malicious traffic in real time.

4.To automate mitigation using the SDN controller’s capabilities.


📦 Dataset:     
CICIDS 2017 / 2019, NSL-KDD, or custom Mininet-generated traffic datasets.

Features include: packet rate, flow duration, protocol, source/destination IP, port numbers, byte count, etc.


🧰 Tools & Technologies:     
* Python – Core ML implementation and data processing.

* Scikit-learn – ML models (e.g., Random Forest, SVM).

* Mininet – Simulated SDN network environment.

* POX / Ryu Controller – SDN controller to dynamically manage flow rules.

* Wireshark / Tcpdump – Network traffic capture and analysis.

* Pandas / NumPy / Matplotlib – Data handling and visualization.


  🛠️ Architecture

             ┌─────────────┐
           │ SDN Network │
           └─────┬───────┘
                 │
         ┌───────▼────────┐
         │ SDN Controller │◄──────┐
         └───────┬────────┘       │
                 │                │
         ┌───────▼────────┐       │
         │ Feature Extractor│      │
         └───────┬────────┘       │
                 │                │
         ┌───────▼────────┐       │
         │ ML Classifier  │◄──────┘
         └───────┬────────┘
                 │
         ┌───────▼────────┐
         │ Mitigation Rules│
         └────────────────┘

  
🔍 Methodology
* Simulate Network Traffic using Mininet (normal + attack).

* Capture Packets and extract flow-based features.

* Preprocess Dataset and label attack vs. normal traffic.

* Train ML Classifier on labeled data.

* Integrate with SDN Controller for real-time detection.

* Block/Redirect Malicious Traffic using controller rules.


📈 ML Models Used:  
Random Forest ✅.

Support Vector Machine (SVM).

Decision Tree.

Logistic Regression.

KNN (for comparison).


![download](https://github.com/user-attachments/assets/b86fda91-7d16-49be-a012-9c752c7e7d64)




🚀 How to Run
1.Clone the repository:

bash
Copy
Edit
git clone https://github.com/yourusername/ddos-sdn-ml.git
cd ddos-sdn-ml

2.Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt

3.Train the model:

bash
Copy
Edit
python train_model.py

4.Run the SDN simulation:

bash
Copy
Edit
sudo mn --controller=remote --topo=tree,depth=2

5.Deploy detection script integrated with the SDN controller (e.g., pox):

bash
Copy
Edit
./pox.py my_ddos_detector



✅ Results:   
Achieved >95% accuracy using Random Forest classifier.

Real-time detection and blocking of DDoS traffic.

Reduced packet loss and network downtime during attack simulation.


![image](https://github.com/user-attachments/assets/39613cf6-b494-4252-9041-e423d960b5b1)



![download](https://github.com/user-attachments/assets/8fd040e7-9c94-4aca-8699-f87579caadef)





