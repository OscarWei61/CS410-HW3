Question1

Not including Stopword
Mean RMSE (tanh): 0.22068321704864502, Mean RMSE (ReLU): 0.2502865493297577
Std RMSE (tanh): 0.08645288646221161, Std RMSE (ReLU): 0.08630675822496414

Not including Stopword
Std RMSE (tanh): 0.08653884381055832, Std RMSE (ReLU): 0.08530408889055252
Mean RMSE (tanh): 0.21537311375141144, Mean RMSE (ReLU): 0.20502625405788422

### **Compare include stopwords or not**

Mean RMSE (relu) not: 0.20502625405788422, Mean RMSE (relu): 0.2055266946554184
Std RMSE (relu) not: 0.08530408889055252, Std RMSE (relu): 0.0843384861946106

![Compare Include Stopwords](images/Compare_include_stopwords.png)
The distribution is narrower but shifted slightly towards higher RMSE values, reflecting the slightly worse average performance when stop words are included.
Overall, the overlap in the histograms indicates minimal impact of stop words on the model's performance, with a slight preference for excluding stop words.

### **Compare tanh and Relu**

Mean RMSE (relu) not: 0.20502625405788422, Mean RMSE (relu): 0.2055266946554184
Std RMSE (relu) not: 0.08530408889055252, Std RMSE (relu): 0.0843384861946106

![Compare Include Stopwords](images/Compare_relu_tanh.png)
Use tanh if you prioritize model stability and lower RMSE variance.
Use relu if your task involves more complex patterns and you need better scalability and computational efficiency.
RMSE more lower might indicate that more accurate result.


Based on the above image, we might choose tanh for better result.


### **Predict last two words**
Last five words : unseen astronom first hour day
Input : unseen astronom first
Predict result(tanh_model_not_including_stopwords model) : ['side', 'greec']
Probability : 
[('side', 0.9954066872596741), ('greec', 0.9953985810279846), ('saw', 0.9953650832176208)]
[('greec', 0.9953914880752563), ('releas', 0.9953892827033997), ('side', 0.9953795671463013)]

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

---

### **Question2**

### **Data without puntuation**

In the situation, the data with punctuation
BERT Accuracy: 0
GPT-2 Accuracy: 0

the first three sets of data：
predictions_bert = ['.', '.', '.']
predictions_gpt2 = ['space', 'proteins', 'be']
actual_words = ['rocket.', 'proteins.', 'bring.']


In the situation, the data without punctuation
BERT Accuracy: 0.0046058691933149095
GPT-2 Accuracy: 0.23042505592841164


the first three sets of data：
predictions_bert = ['.', '.', '.']
predictions_gpt2 = ['space', 'proteins', 'be']
actual_words = ['rocket', 'proteins', 'bring']


GPT-2 perform more better!

---

### **First Image: Cosine Similarity Distributions with punctuation (BERT vs GPT-2)**

![BERT Cosine Similarity Distribution without punctuation](images/Compare_BERT_and_GPT-2_Cosine_Similarity_Distribution_with_punctuation.png)


### **Second Image: Cosine Similarity Distributions without punctuation (BERT vs GPT-2)**

![Compare BERT and GPT-2 Cosine Similarity Distribution without punctuation](images/Compare_BERT_and_GPT-2_Cosine_Similarity_Distribution_without_punctuation.png)