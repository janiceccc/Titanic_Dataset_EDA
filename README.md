# Data Description

| Variable | Definition | Key |
| ------------- | ------------- | ------------- |
| survival | Survival  |  0 = No, 1 = Yes |
| pclass  | Ticket | class 1 = 1st, 2 = 2nd, 3 = 3rd|
| sex | Sex | |
| Age | Age in years | |
| sibsp | # of siblings / spouses aboard the Titanic|  |
| parch | # of parents / children aboard the Titanic|  |
| ticket | Ticket number |  |
| cabin | Cabin number|  |
| embarked | Port of Embarkation| C = Cherbourg, Q = Queenstown, S = Southampton |


# Analysis

### Main attributes used in the analysis


**Pclass:** 62.98% 1st class passenger survided , 47.28% 2nd class passenger survived, and 24.24% third class survived, whcih indicates passengers with higer ticket class are more likely to survive.

**Sex:** 74.2% female survived and 18.89% male survived, which indicates females are more likely to survive.

**Age:** Ages are evenly splited into 8 intervals, passengers from age 0-10 has the highest survival rate, passnengers from age 70-80 has the lowest survival rate, indicates younger passengers are more likely to survive.

**Fare:** Fares are evenly splited into 11 intervals. From the calculation, passengers paid for higher fare tickets have higher survival rate, and passengers did not paid or paid low fare tickets have the lowest survival rate, indicates passeneger paid higher fare are more likely to survive.

**Embarked:** There are three embarked points, includes two passengers's embarked points are unknown. 55.36% passengers embarked from Cherbourg survived, 38.96% passengers embarked from Queenstown survived, and 33.7% passengers embarked from Southampton survived, which indicates passengers embarked from Cherbourg are more likely to survive.

###  Attributes engineered

**Family_size_aboard:** family_size_aboard is calculated by sibsp + parch + 1(passenger him/herself). Passengers with family size =4 has survival rate = 72.41% , passenger with family size = 2 and 3 has survival rate = 55.28%, 57.84% respectively, which indicates passengers with mid family size aboard are more likely to survive.

**Deck:** The initial letter of Cabin indicates the Deck level. For passengers have more than one cabin, most of them have cabins on the same level Deck, but there are cases that cabins from different Deck too, in this case, the initial letter of each Cabin are combined to create a new Deck. Deck A is the toppest level, B is the 2nd toppest...

There are 77% Passengers has no infomation about what deck they live on, in this case, 'NA' is assigned and treated as a group. In the analysis, first calculate the total number of passengers from each deck, including NAs, and number of passengers survived, then caluclate the survival rates. The result indicates passengers live on deck B, D, E, F, FE have survival rates greater than 74%, which are more likely to survive.

**Special_title:** titles are retrieved from Passenger Names, includes ['Mr.', 'Mrs.', 'Miss.', 'Master.','Don.', 'Rev.', 'Dr.','Mme.', 'Ms.', 'Major.', 'Lady.', 'Sir.', 'Mlle.', 'Col.','Capt.', 'Countess.', 'Jonkheer.']. Titles not in [' Mr.', ' Mrs.', ' Miss.', ' Mme.', ' Ms.', ' Mlle.'] are treated as Special titles.

Passengers are seperated into two groups, with Non-Special Title and Special Title. 49.21% passengers with special title are survived, and 35.56% passengers with non-special title are survived, which indicates passengers with special titles are more likely to survive.


### Summary
Passengers embarked at Cherbourg, with mid family size (2-4) aboard, live on mid to high level deck (B-FE), with higher Ticket class (Pclass = 1), bought high fare ticket, younger age and sex = female are more likely to survive the Titanic disaster.


