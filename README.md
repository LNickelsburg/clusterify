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

1. **Setup**

Run code in the "Setup" section. You will be asked to confirm that you want to connect to Google Drive. Please connect to your personal Drive - this is necessary so that your output can be saved and easily shared with whoever is executing the later steps.

2. **Taking Your Data**

In the "Give me your name" section, please put your name in the quotes. For example, that line of code would read as follows after I modify it:\
```user = "Leah"``` 

Next, run the "Let me into your account" section. You should see a brief prompt, a URL, and an empty text box. Click on the URL.

*If you are already logged into Spotify:* You should be taken to a page that says "Example Domain". Copy the URL of this page from the search bar, paste it into the empty text box, and press enter.

*If you are not yet logged into Spotify:* You will see a login page. Log in, and then you should be taken to a page that says "Example Domain". Copy the URL of this page from the search bar, paste it into the empty text box, and press enter.

3. **This part saves your top spotify tracks to a file that I will be playing with**

Run the code in this section. 

If you are retrieving your data to be analyzed but *not* analyzing it yourself: locate the newly created .csv file in your Google Drive, and share it with whoever will be executing the next two steps.



### **apiify**
Simply place user .csv files are in the correct directory, and run

### **clusterify**
Just run it woooooo



