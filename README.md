**Contact Tracing using Machine Learning**

**Overview**
This project explores the use of chest X-ray images to detect potential contact links between patients by analyzing visual similarities in their lungs. The core idea is to build a graph-based network where patients are connected if their X-ray images show high similarity — helping visualize possible contact chains and aiding in early tracing efforts.

**Dataset Source**: (http://kaggle.com/datasets/tawsifurrahman/covid19-radiography-database)

**Classes:**
1) Normal
2) COVID
3) Lung Opacity
4) Viral Pneumonia

**Structure**: Images are organized into folders by class. Each folder contains a large number of chest X-ray images.

**Project Workflow** : 
1) **Data Collection & Organization** : 
Images are loaded from class-specific folders stored in Google Drive.
2) **Image Preprocessing** : 
All images are resized to a standard size for fair comparison. Basic exploratory analysis is done to understand image brightness, contrast, and structure.
3) **Image Similarity Detection** : 
Image similarity is calculated using visual histograms. If the similarity exceeds a defined threshold, the images are considered "linked."
4) **Graph Construction** : 
Each image is treated as a node. Edges are drawn between nodes (patients) if their images are similar enough. This forms a graph that highlights potential contact links.
5) **Visualization** : 
The contact tracing graph is plotted, where clusters or connected components may indicate related transmission or exposure.

**Insights & Outcomes** : 
1) Patterns in lung opacity and structure can be compared visually to find image-level similarities.
2) Patients with similar lung X-ray features often cluster in the graph, suggesting potential exposure linkage.
3) Graph theory provides a compelling way to model and visualize contact networks from visual data.

**Tools Used** : 
1) Google Colab + Google Drive
2) Python
3) Pandas, NumPy
4) PIL & OpenCV (for image processing)
5) NetworkX (for graph construction)
6) Matplotlib & Plotly (for visualization)
