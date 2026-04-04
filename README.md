# Deep-Scene-Vision_Advanced-Image-Classification-and-Interpretability_PyTorch
Advanced Image Classification and Interpretability using PyTorch, Featuring custom CNN architectures and Grad-CAM Visualization.

​​📸 Intel Image Classification| 
تصنيف صور المشاهد الطبيعية

​📝 Project Overview |
نبذة عن المشروع

​English: This project implements an advanced Computer Vision pipeline using PyTorch to classify natural scenes. By leveraging Transfer Learning with a pre-trained ResNet50 backbone, the model accurately identifies 6 categories: Buildings, Forest, Glacier, Mountain, Sea, and Street.

العربية:

يقدم هذا المشروع مساراً متقدماً في الرؤية الحاسوبية باستخدام مكتبة PyTorch لتصنيف المشاهد الطبيعية. بالاعتماد على تعلم النقل (Transfer Learning) ونموذج ResNet50 المدرب مسبقاً، يستطيع النموذج تصنيف 6 فئات بدقة: المباني، الغابات، الأنهار الجليدية، الجبال، البحار، والشوارع
.
​🛠️ Technical Stack | التقنيات المستخدمة
​Framework: PyTorch (Deep Learning Core).
​Architecture: ResNet50 (Pre-trained on ImageNet).
​Explainability: Grad-CAM (Gradient-weighted Class Activation Mapping).
​Optimization: Adam Optimizer & StepLR Scheduler.
​Data Engineering: Custom Dataset wrappers & DataLoaders.

​🚀 Key Implementation Steps | خطوات التنفيذ الأساسية
​
1. Data Augmentation | تحسين وتوسيع البيانات
​
English:
Applied techniques like Random Rotation, Color Jitter, and Horizontal Flips to enhance model generalization and prevent overfitting.
العربية:
 تم تطبيق تقنيات مثل الدوران العشوائي، تعديل الإضاءة، والقلب الأفقي لتحسين قدرة النموذج على التعميم ومنع الإفراط في التخصيص (Overfitting)

​2. Model Fine-Tuning | ضبط النموذج
​
English:
Froze the convolutional base of ResNet50 and added a custom classification head consisting of Linear layers, ReLU activation, and Dropout (0.4).
العربية:
قمنا بتجميد طبقات ResNet50 الأساسية وإضافة رأس تصنيف مخصص يحتوي على طبقات Linear مع تفعيل ReLU وطبقة Dropout بنسبة 0.4 لضمان استقرار التعلم.

​3. XAI with Grad-CAM | تفسير النموذج (الذكاء الاصطناعي القابل للتفسير)

​English:
Implemented Grad-CAM to visualize "Heatmaps" on images. This explains the model's decision by highlighting the specific features (like trees or peaks) it used for prediction.
العربية:
تم دمج تقنية Grad-CAM لاستخراج خرائط حرارية توضح "مناطق الاهتمام". هذا يفسر قرار النموذج من خلال تسليط الضوء على العناصر (مثل الأشجار أو قمم الجبال) التي استند إليها في التوقع.
​
📊 Performance Evaluation | تقييم الأداء

​English:
The model's performance was rigorously tested using:
​Confusion Matrix: To identify misclassifications between similar classes.
​Classification Report: Measuring Precision, Recall, and F1-Score.
​Learning Curves: Plotting Loss and Accuracy for both Training and Validation.

​العربية:
تم اختبار أداء النموذج بدقة من خلال
​مصفوفة الارتباك (Confusion Matrix): لتحديد التداخل بين الفئات المتشابهة.
​تقرير التصنيف: لقياس الدقة (Precision) والاستدعاء (Recall) لكل فئة.
​منحنيات التعلم: رسم بياني لمعدل الخطأ والدقة خلال مراحل التدريب والتحقق

​📊 Model Performance & Visual Results
​To demonstrate the model's reliability and transparency, we provide the following metrics and interpretability visualizations:

### 1. Training Metrics (Accuracy & Loss)
![Accuracy and Loss](Accuracy_and_Loss.png)

​📊 Training Performance Analysis | تحليل أداء التدريب
​
English:

​The Loss Curves demonstrate a consistent downward trend, confirming that the model effectively minimized error and converged smoothly. The Accuracy Curves show that the model reached a high performance level, with the validation accuracy closely following the training progress, which indicates a well-generalized model without overfitting.

​العربية

​توضح منحنيات الخسارة (Loss) انخفاضاً مستمراً، مما يؤكد قدرة الموديل على تقليل نسبة الخطأ والوصول لحالة الاستقرار (Convergence). كما تظهر منحنيات الدقة (Accuracy) وصول الموديل لمستوى أداء عالٍ، مع تقارب دقة التحقق (Validation) من دقة التدريب، مما يدل على قدرة الموديل على التعميم بشكل ممتاز دون الوقوع في مشكلة الـ Overfitting.


### 2. Classification Report
![Classification Report](Classification_Report.png)

### 3. Confusion Matrix
![Confusion Matrix](Confision_Matrix.png)

​📉 Model Evaluation | تقييم أداء النموذج
​
English:

​The Classification Report shows an overall accuracy of 91%, with high precision and recall across most classes, especially the "Forest" category. The Confusion Matrix further confirms this strong performance, as the majority of predictions lie on the main diagonal. While there is minor confusion between "Glacier" and "Mountain" due to visual similarities, the model effectively distinguishes between most distinct environments.

​العربية

​يوضح تقرير التصنيف (Classification Report) أن الدقة الإجمالية للموديل بلغت 91%، مع قيم مرتفعة لـ Precision و Recall في معظم الفئات، وخاصة فئة "Forest". وتؤكد مصفوفة الارتباك (Confusion Matrix) هذا الأداء القوي، حيث تتركز معظم التوقعات الصحيحة على القطر الرئيسي للمصفوفة. وبالرغم من وجود تداخل بسيط بين فئتي "Glacier" و "Mountain" نظراً للتشابه البصري بينهما، إلا أن الموديل أظهر كفاءة عالية في التمييز بين البيئات المختلفة



### 4. Model Interpretability (Grad-CAM)
![Grad-CAM 1](Grad_CAM_1.png)
![Grad-CAM 2](Grad_CAM_2.png)
![Grad-CAM 3](Grad_CAM_3.png)

​🔍 Model Interpretability with Grad-CAM
​To ensure the model is making decisions based on relevant features rather than background noise, I implemented Grad-CAM (Gradient-weighted Class Activation Mapping).

​How it Works:

​Feature Extraction: It uses the gradients of the target class (e.g., Mountain, Sea, Forest) flowing into the last convolutional layer (layer4 or layer3 of ResNet50).
​Heatmap Generation: We calculate the importance of each neuron to the final prediction and produce a coarse localization map.
​Visualization: The heatmap is superimposed on the original image using Bilinear Interpolation for a smooth, professional finish.

​💡 تفسير النتائج بالعربية

​استخدمت تقنية Grad-CAM لزيادة شفافية الموديل وفهم كيفية اتخاذ القرار:
​المناطق الدافئة (الأحمر/الأصفر): تمثل الأجزاء التي ركز عليها الموديل لتصنيف الصورة (مثل قمم الجبال أو أفق البحر).
​الدقة: باستخدام bilinear interpolation وتجربة طبقات مختلفة، تمكنت من الحصول على خريطة حرارية دقيقة توضح كفاءة التدريب.

### 5. Prediction Samples
![Prediction 1](Predicted_1.png)

🔮 Advanced Prediction & Probability Analysis | التوقع المتقدم وتحليل الاحتمالات
​
English:

​Beyond simple classification, this section utilizes the Softmax output to visualize the model's confidence levels for each prediction. By displaying the top 3 class probabilities alongside each image, we can identify cases where the model is highly certain or when it struggles to differentiate between visually similar classes like "Street" and "Buildings".

​العربية

​أبعد من مجرد التصنيف البسيط، يستخدم هذا القسم مخرجات دالة Softmax لعرض مستويات ثقة الموديل في كل توقع بشكل مرئي. من خلال عرض احتمالات أفضل 3 فئات بجانب كل صورة، يمكننا تحديد الحالات التي يكون فيها الموديل واثقاً تماماً أو الحالات التي يواجه فيها صعوبة في التمييز بين الفئات المتشابهة بصرياً مثل "Street" و "Buildings"


![Prediction 2](predicted_2.png)

​👁️ Visualizing Model Decisions | تفسير قرارات النموذج
​
English:

​This final stage combines Grad-CAM heatmaps with Top-3 Probability bar charts to provide a comprehensive view of the model's reasoning. The heatmap highlights the specific pixels that triggered the classification, while the probability chart shows how confident the model is compared to other potential classes. For instance, it can achieve a confidence level as high as 99.89% for clear-cut classes like "Sea".

​العربية

​تدمج هذه المرحلة النهائية بين الخرائط الحرارية لتقنية Grad-CAM والرسوم البيانية لـ أفضل 3 احتمالات لتقديم رؤية شاملة لكيفية اتخاذ الموديل لقراره. توضح الخريطة الحرارية البكسلات المحددة التي أدت لعملية التصنيف، بينما يوضح مخطط الاحتمالات مدى ثقة الموديل مقارنة بالفئات الأخرى المحتملة. على سبيل المثال، يمكن للموديل أن يصل لمستوى ثقة مرتفع جداً يصل إلى 99.89% في الفئات الواضحة مثل "البحر"



## 👤 Author
**[MOHAMED BELAL]** *Deep Learning & Data Engineering Enthusiast*
MY PHONE [01018689118]


