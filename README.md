# **CLUSTERIFY**
**Simple Spotify listening history comparison**

This is a 3-step process:
1. Individual users retrieve their Spotify listening history (see "takeify")
2. User histories are consolidated, and track features are accessed from the
Spotify API (see "apiify")
3. Features undergo PCA dimensionality reduction, then are visualized based on
user tag (see "clusterify")

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


**PCA Visualization, By User**<br>
<img src="https://github.com/LNickelsburg/clusterify/assets/35284172/041e8c83-02fe-42e3-b03d-5f3bbbb6c447" width="300" height="200">
<img src="https://github.com/LNickelsburg/clusterify/assets/35284172/8cb9ec71-4b56-42f0-aa32-e8cb64b1d302" width="300" height="200">

**Plotting based on manually selected features**<br>
After considering the feature impacts on each PCA component, I tried plotting the data using only 3 variables (with one variable per axis), rather than using all variables on all axes as PCA does. I found that using only 3 variables, I was still able to produce a very similar result.
<img src="https://github.com/LNickelsburg/clusterify/assets/35284172/5cadf94a-b41b-4752-8a88-7d0c4901cdeb" width="300" height="200">
<img src="https://github.com/LNickelsburg/clusterify/assets/35284172/1eb303b9-ed7e-42d3-8448-6458bd8db750" width="300" height="200">

In both the PCA-based example and the 3-variable example, the data is represented in a U-shape; the three users are distributed similarly throughout the plot, and similar musical artists and songs are close together.
