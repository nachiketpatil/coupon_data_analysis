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

To run the code either use [Jupyter Notebook](https://jupyter.org/install) or upload the notebook and directories to [Google Colab](https://colab.research.google.com/).


Local setup:
```bash
 pip install matplotlib seaborn pandas numpy
 pip install notebook
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
2. Install dependencies:
   `pip install matplotlib seaborn pandas numpy`
3. Open the Jupyter Notebook:
   `jupyter notebook coupon_data_analysis.ipynb`
   Run the cells to explore the analysis.

## License
This project is public (Unlicense). Feel free to download and use the code for your own analysis. 

## Analysis Report 
The data represents several attributes of drivers, some attributes of coupons and some contextual attributes.
After cleaning up the data and visualizing the relationships between the attributes, here is a brief summary of the findings:

1. Driving Distance : The biggest factor that affects the coupon acceptance is the coupon destination distance. If it takes longer than 15 minutes to redeem coupon, drivers are significantly less likely to accept coupons. 
2. Driving Direction: The driving direction also plays a role in conjunction with the coupon distance. 5 minutes in any direction is okay but 15 minutes against current direction is significantly less desirable.  
3. Destination: A driver heading to no urgent destination is more likely to accept a coupon compared to those heading to work.
4. Time of the day: Drivers in the evening are more likely to accept a coupon. This goes hand in hand with the destination as drivers heading from work or on leisure trips are more likely to accept a coupon.
5. Eating & Drinking Habits: Regular visitors to bars, coffee houses, and restaurants are more likely to accept coupons, which makes sense—they are already inclined to spend on these activities.
6. Weather: Although warmer temperatues and Sunny weather sees more coupon acceptance, other conditions do not have a significantly large impact on coupon acceptance.
7. Passenger Type: Drivers with Kids as passengers are less likely to accept a coupon compared to others. This is probably because they have more planned routines or prefer specific places for their kids rather than spontaneous dining or shopping, which is the case with friends or only partner as passengers.
8. Education and Occupation: Individuals with graduate degrees and those in business, finance, or architecture & engineering careers tend to be less likely to accept coupons. This could indicate that professionals with structured schedules are less inclined toward spontaneous stops
9. Age: Age conveniently ties in with Education and Occupation. Younger drivers with more free time are more likely to accept coupons.
10. Income Level: Surprisingly, income doesn’t drastically impact coupon acceptance.

### Key Findings:
1. Convenience is key—people are more likely to redeem coupons if the location is on their way.
2. Leisure trips (home/no urgent destination) see higher coupon use than work trips.
3. Social settings (with friends/partners) lead to more coupon acceptance.
4. Weather & timing influence acceptance, with warmer, sunnier conditions and later times seeing higher rates.
5. Parents & professionals are less likely to take advantage of coupons.

### Recommendations:
- Target younger drivers with partners or friends heading home or to a casual destination on warmer sunny days in the evening. 
- The place to hand out coupons should be in the middle of the coupon destinations like downtown or town center to minimize the time to reach the coupon destination and this way the direction of the travel can be used to hand out the coupon with destination on the driver's way.
- As Students are more likely to accept the coupons, target the coupon distribution around the universities or colleges.
