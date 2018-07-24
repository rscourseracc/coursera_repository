### coursera_repository
# IBM Applied Data Science Capstone Project

## Problem Statement
## Help prospective students choose the University most suited to their circumstances by factoring in location advantage/disadvantage in the decision making process.

#### For the purpose of this project we limit ourselves to Universities in the US.
#### US is a popular destination for higher studies the worldover. Foreign and US in-state/out-of-state Students shortlist the Universities based on a number of factors. Some of the more important factors are:
  ###### Ranking of the University
  ###### Tuition Fees
  ###### Cost of Living
  ###### Quality of Faculty
  ###### Quality of students (Cutoffs)
  ###### Resources/Amenities at the University
  ###### Research quality
  ###### General performance of the University's alumni base
  ###### On-campus diversity
  ###### Student Engagement (Clubs/Student-led initiatives)
  ###### Industry connect
  ###### Average starting salaries
  ###### Average Salaries after 5/10 years
  ###### Part-time jobs availability
  ###### Transportation facilities
  ###### City specific parameters (Safety/Crime, Arts, Sports, Nightlife, general quality of life etc.)
#### The list goes on ....

#### Many rating agencies calculate and rank Universities on a number of these parameters. While Academic burden, teaching quality, resource-richness/funding availability, diversity & salaries are chosen as evaluation parameters by all rating agencies, the subtler aspects are often overlooked. 
#### Many foreign students, as well as resident students with fewer means, look for a University/City combination that will allow them to earn a living through part time work. 
#### There are usually jobs available on campus - Library Assistants, Teaching Assistants, Tour Guides etc. - but these are much coveted and the chances that a student will find such a job are slim. The uncertainty involved in decision making process often forces students to play cautious and apply to lower ranked Universities when they could have done much better.

### Value Proposition to Students Scouting for Universities

#### Providing additional data, apart from what's already included in University rankings tables, on locations around the campus can help students become more assured of their ability to sustain themselves while pursuing higher education at a University of their choice. The locations data can include such details as: no. of offices, food venues/restaurants, industrial zones, sports and recreation facilities,  residential areas, city transportation facilities within a reasonable radius of campus.

#### By performing clustering & segmentation analysis on the consolidated dataset, one can also help identify Universities which are similar/dissimilar to each other based on a set of chosen parameters. Armed with this data, a student may then opt for a University within a cluster of their choice which offers better value to them.

## Data Availability

##### We make use of the University Rankings Data published annually by Times Higher Education. Link to the 2017 University Rankings is given below:
##### https://www.timeshighereducation.com/rankings/united-states/2017#!/page/0/length/50/sort_by/rank/sort_order/asc/cols/stats

##### The webpage loads data through a json request, so, static html table scraping cannot be used. Instead, I have identified the json request url & will be reading the response directly. The response data will be normalized into a pandas dataframe for further processing. Below is the url for the json request:

##### https://www.timeshighereducation.com/sites/default/files/the_data_rankings/united_states_rankings_2017_limit0_068d27a033ada75528617769a8a4c4c2.json

###### The dataset includes rankings of 1061 Universities across US. The evaluation is based on 14 parameters across 4 pillars - 

###### Resources
###### Engagement
###### Outcomes
###### Environment

###### In addition, helpful figures on Annual Tuition Fees, Room & Board, and, Average Salary after 10 years is provided as well.

###### We will supplement the provided fields with Latitude & Longitude data from Google Geocode API. Based on obtained locations, Foursquare API will be made use of to explore & search places of interest.

###### To facilitate analysis, we will limit the choice of Universities to top 200. 
###### We also limit the venue categories to the following in order to not overshoot the free/developer quota offered by Foursquare:
###### Offices
###### Shops
###### Food Joints, Restaurants, Cafes
###### Arts venues
###### Sports & Recreation Venues
###### Entertainment Venues
###### Libraries
###### Colleges
###### Nightlife venues
###### Residetial areas
###### Government Offices
###### Transportation venues
###### These are subjective but reasonable choices for most sought after neighborhood venues for college students.









