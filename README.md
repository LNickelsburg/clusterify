# **CLUSTERIFY**
**A tool for users to compare their Spotify listening histories**

This is a 3-step process:
1. Individual users retrieve their Spotify listening history (see "takeify")
2. User histories are consolidated, and track features are accessed from the
Spotify API
3. Features undergo PCA dimensionality reduction, then are visualized based on
K-means clustering and based on user tag

## **Instructions**
### **takeify**
If you are retrieving your data to be analyzed but *not* analyzing it yourself, this is the only file you will need to use. Open takeify.ipynb, then select "Open In Colab" at the top of the code preview. This will take you to Google Colab, where you will run the code. 
1. **Setup**\
Run code in the "Setup" section. You will be asked to confirm that you want to connect to Google Drive. Please connect to your personal Drive - this is necessary so that your output can be saved and easily shared with whoever is executing the later steps.
2. **Taking Your Data**\
In the "Give me your name" section, please put your name in the quotes. For example, for me that line of code would read as follows:\
```user = "Leah"```\
Next, run the "Let me into your account" section.



### **apiify**
Simply place user .csv files are in the correct directory, and run

### **clusterify**
Just run it woooooo



