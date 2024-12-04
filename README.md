
Not including Stopword
Mean RMSE (tanh): 0.22068321704864502, Mean RMSE (ReLU): 0.2502865493297577
Std RMSE (tanh): 0.08645288646221161, Std RMSE (ReLU): 0.08630675822496414

Based on the given results, here’s the analysis:

---

### **1. Mean RMSE**
- The mean RMSE for **tanh** is **0.2207**, which is significantly lower than the **0.2503** of **ReLU**.
- A lower RMSE indicates smaller prediction errors, meaning **tanh** outperforms **ReLU** in this regard.

---

### **2. Standard Deviation (Std RMSE)**
- The standard deviation of RMSE for **tanh** is **0.0865**, while for **ReLU** it is **0.0863**.
- Both activation functions demonstrate almost identical stability, as the difference in standard deviation is negligible.

---

### **3. Overall Analysis**
- **tanh** exhibits better performance in terms of lower prediction errors (mean RMSE) while maintaining similar stability (standard deviation) compared to **ReLU**.
- While **ReLU** remains competitive in stability, its higher RMSE makes it less preferable in this case.

---

### **Conclusion**
Given the lower mean RMSE and comparable stability, **tanh** is the better choice of activation function for this dataset and task. It minimizes prediction errors while maintaining consistent performance, making it more suitable for further experimentation or application.