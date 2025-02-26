# coupon_data_analysis


This project is practical analysis of a dataset about coupon data. The data is taken from [UCI Machine Learning Repository](https://archive.ics.uci.edu/) and was collected via a survey on Amazon Mechanical Turk.
The goal of this project is to use probability distributions and data visualization techniques to make some sense out of the given coupon dataset.

## Problem Statement
### Will the Customer Accept the Coupon?
The dataset contains data collected from drivers passing through a town. These drivers were offered some coupons  and the data about the drivers, the coupons and whether they use itor not was collected. 
Using the techniques to collect and clean the data, calculating probability distributions and visualizing the relationships between the attributes, predict whether a driver will accept a coupon based on these attributes. And provide some recommendations of what conditions will maximize coupon acceptance.

The commands and code to manipulate and visualize the data is provided in and Interactive Python Notebook (Jupyter Notebook) in the repository.

## Data Description
The dataset contains survey responses with the following attributes (values are averages):
### 1. User Attributes
- Gender: Male, Female
- Age: Below 21, 21–25, 26–30, etc.
- Marital Status: Single, Married, Unmarried Partner, Widowed
- Number of Children: 0, 1, 2+
- Education: High School, Bachelors, Associates, Graduate Degree
- Occupation: Architecture & Engineering, Business & Financial, etc.
- Annual Income: < $12,500, $12,500–$24,999, $25,000–$37,499, etc.
- Frequency of Visits to bars: 0, <1, 1–3, 4–8, >8 times
- Frequency of Visits to coffee houses: 0, <1, 1–3, 4–8, >8 times
- Frequency of food takeaway: 0, <1, 1–3, 4–8, >8 times
- Frequency of Visits to restaurants where expense per person is < $20: 0, <1, 1–3, 4–8, >8 times
- Frequency of Visits to restaurants where expense per person is between $20 and $50: 0, <1, 1–3, 4–8, >8 times
### 2. Contextual Attributes
- Driving Destination: Home, Work, No Urgent Destination
- Location: Distance and direction between user, destination, and venue (with driving time)
- Weather: Sunny, Rainy, Snowy
- Temperature: 30°F, 55°F, 80°F
- Time: 10 AM, 2 PM, 6 PM
- Passenger: Alone, Partner, Kid(s), Friend(s)
### 3. Coupon Attributes
- Expiration: 2 hours, 1 day
- Coupon Type: Restaurant (< $20), Restaurant ($20–$50), Coffee House, Carry Out, Bar

### Acceptance of coupon Y:  
- 0 (rejected: "no, I don’t want it")
- 1 (accepted: "right away" or "later before expiry"), 

The dataset is in the `/data` subfolder.

## Dependencies
This project requires the following Python libraries:
- `matplotlib.pyplot` (for plotting)
- `seaborn` (for enhanced visualizations)
- `pandas` (for data manipulation)
- `numpy` (for numerical operations)

To run the 


Local setup:
```bash
 pip install matplotlib seaborn pandas numpy
```

## Repository Structure
```
├── data/                       # Directory for dataset
│   └── coupons.csv             # Coupon dataset
├── images/                     # Directory for storing visualization images
├── coupon_data_analysis.ipynb  # Jupyter Notebook with analysis
└── README.md                   # Project documentation and analysis results
```

## Usage
1. Clone the repository:
   - Open terminal and run:
   `git clone https://github.com/nachiketpatil/coupon_data_analysis.git`
3. Install dependencies:
   `pip install matplotlib seaborn pandas numpy`
4. Open the Jupyter Notebook:
   jupyter notebook coupon_data_analysis.ipynb
   Run the cells to explore the analysis.

## License
This project is public (Unlicense). Feel free to download and use the code for your own analysis. 

## Analysis Report 


