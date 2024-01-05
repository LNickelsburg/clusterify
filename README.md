# **CLUSTERIFY**
**Simple Spotify listening history comparison**

This is a 3-step process:
1. Individual users retrieve their Spotify listening history (see "takeify")
2. User histories are consolidated, and track features are accessed from the
Spotify API (see "apiify")
3. Features undergo PCA dimensionality reduction, then are visualized based on
K-means clustering and based on user tag (see "clusterify")

## **Future Modifications**
- I have not yet implemented a user interface for the data retrieval step. Eventually, it will all be able to happen with just a few clicks; for now, please follow the instructions in the "takeify" section below to retrieve your data.
- I intend to modify my dimensionality reduction process so that each component is influenced by no more than three features, and no two components are influenced by the same feature. My goal is to be able to visualize this data in three dimensions, with each axis conveying clear and interpretable information (as opposed to the current visualization, in which each axis represents a weighted combination of every feature).

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

## **Example Output**


**Feature Distribution Visualization**

![image](https://github.com/LNickelsburg/clusterify/assets/35284172/2c60e4cf-072b-4f63-88b5-d4d9de76f52b)

**PCA Visualization, By User**
![image](https://github.com/LNickelsburg/clusterify/assets/35284172/b23c5357-1bd6-4c46-8237-32a7d6b2200e)

**Feature Impacts**
```
Explained variance by component: [0.21200714 0.11807601 0.09357741]

                       PC1       PC2       PC3
release_date     -0.105860  0.108055 -0.270989
acousticness      0.825978  0.212372  0.046326
danceability     -0.096656  0.598422 -0.524664
duration_ms      -0.011871 -0.422806  0.266580
energy           -0.910906 -0.056231 -0.013218
explicit         -0.140060  0.638455  0.422264
instrumentalness  0.053705 -0.430325 -0.257584
key              -0.312674 -0.106028  0.127881
liveness         -0.391453 -0.097495  0.070925
loudness         -0.890545 -0.026545 -0.060358
popularity       -0.544505 -0.014066  0.373624
mode              0.496088  0.352569  0.214964
speechiness      -0.248396  0.557099  0.536748
tempo            -0.064173 -0.207483  0.364337
time_signature   -0.301227  0.141320 -0.242334
valence          -0.357743  0.446483 -0.393975
```

