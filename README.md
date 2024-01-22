# Aviation Analysis 
Author: DDurrant


Dashboard: https://public.tableau.com/views/Learn-wb-12-24-2023Aviation/AviationData?:language=en-US&:display_count=n&:origin=viz_share_link


# Overview 
The project analyzes historical Aviation Accident Database & Synopse dataset to inform Company Y regarding diversification into the aviation industry. Company Y will utilize the analysis to determine airplane risk and key stakeholders tolerance  along with other metrics beyond the scope of this project.
# Business Problem

Company Y portfolio diversification maybe possible when airplane safety is aligned with not just asset damage but more closely with the community consequences. Identifying the risk or the riskiest models and aircraft, the occurrence of accidents and the extremes of human cost that is fatality versus non injury. Using the aviation accident data, I analyzed trends and patterns of accidents; fatalities; non-injury(uninjured); purpose of flight; country, and airplane make and model.

# Data Understanding
The aviation accident data set is a global public data set of accidents and incidents since 1979. Each event year has unique ID's associated with fatalities, country and injuries including categorical data such as aircraft type make model etc..




# To answer business question and  make recommendations
Only airplanes as  aircraft category is required.
Analysis will be done for Accidents per year, for country, fatalities and Uninjured  
Analyze the number of accident to make and model; make and model to fatalities, uninjured
Purpose of flight, accidents, fatalities and uninjred 
Business is interested in both commercial and private business segments 


# Columns for analysis 
['Investigation.Type', ''Event.Date''Injury.Severity', 'Aircraft.Category''Make', 'Model''Purpose.of.flight 'Total.Fatal.Injuries', 'Total.Serious.Injuries', 'Total.Minor.Injuries', 'Total.Uninjured']

# Aviation Data Dictionary

Column Name	           Short Description           Meaning

#InvestigationType   Type of Event     Refers to a regulatory definition of the event severity. The severity of a general aviation accident or incident is classified as the combination of the highest level of injury sustained by the personnel involved (that is, fatal, serious, minor, or none) and level of damage to the aircraft involved (that is, destroyed, substantial, minor, or none). The

#EventDate	Event Date	The date of the event. Dates are be entered in the format: MM/DD/YYYY
Country	Event Country	The country in which the event took place.

#AircraftCategory	   Aircraft Category	The category of the involved aircraft. In this case, the definition of aircraft category is the same as that used with respect to the certification, ratings, privileges, and limitations of airmen. Also note that there is some overlap of category and class in the available choices.

#Make	Aircraft Manufacturer's Full Name	Name of the manufacturer of the involved aircraft.

#Model	Aircraft Model	The full alphanumeric aircraft model code, including any applicable series or derivative identifiers. For example, a 200 series Boeing 737 is entered as 737-200.


# Analyzing the data and building visualizations

# Investigation.Type has 2 subsets
Aviation_data_filtered[ 'Investigation.Type'].value_counts()
Accident    25924
Incident     1649
Name: Investigation.Type, dtype: int64

# Aviation Incident vs Accident
According to Annex 5, "an incident is defined as an occurrence, other than an accident, associated with the operation of an aircraft which affects or could affect the safety of operation".

#Accident is defined as "accident as an occurrence associated with the operation of an aircraft: in which a person is fatally or seriously injured; in which an aircraft sustains damage or structural failure requiring repairs; after which the aircraft in question is classified as being missing.#"

#https://applications.icao.int/postalhistory/annex_13_aircraft_accident_and_incident_investigation.htm#:~:text=Annex%2013%20outlines%20how%20accident,following%20completion%20of%20the%20investigation.

# Human Cost for Year
The number of fatalities trends downward as the occurrence of uninjured increases through the years, peaking in 2011. 

Throughout the timeframe there are approximately 10 times the number of uninjured to fatalities. This is  indicative of a certain level of confidence regarding safety when the mode of transportation is airplane.

#Next analyze the geographical data


# Community Consequences 
The United States has the most accidents followed by a distanced Brazil.
The United States has the highest rate of fatalities, injuries and non-injured, this is expected 
as it has the largest number of accidents for the data period. Of the top 30 countries 100% of Lebanon's  and 97% Libya's records are fatalities.

# Personal and Social Consequences
A significant number of fatalities occur when the travel purpose is 'Personal'. 
The ‘Unknown ‘category has the highest fatality and uninjured rates. The Unknown subset was created from the missing data. When the unknown subset is removed the top 5 safest based on the aggregate of uninjured are 'Personal'. 'Business', 'Instructional', 'Aerial Application’ and 'Skydiving.  There are no fatalities for the AirDrop and PUBS subsets.


# Examine the actual aircraft data
Riskiest models¶
The riskest models are 172, 152, 182, 172N, 172s
Make¶
The airplane Make with the highest accident rates are Cessna, Piper, Beech and Boeing. Highest fatalities for Make are Cessna, Boeing, Piper and Airbus The 'Make' with the most uninjured are Boeing Cessna, Airbus and McDonnell Douglas

Now that we have identified riskest and safest Makes and Models , what are the associated make and model? Group the make and model to determine the safest.
Make    Model  
BOEING  737        6468.000000
        777        2184.000000
Boeing  737        2155.000000
BOEING  767        2148.000000
        737 7H4    1506.000000
        747        1416.000000

# Impact on lives
Cessna multiple models are highly associated with the purpose of flight in specifically the "Personal" and 'Instructional' subsets.Cessna 172 is one of the top 10 safest airplane.


# Conclusion 
Boeing (Make & Model) manufactures lowest risk aircraft.

Least human consequences or the highest uninjured by manufacturer resulted from Boeing, Airbus and Cessna. 

Business enterprise - Primary purpose of flight – The most common purposes are Personal and Instructional. The airplane 'Make'most frequently used for these primary purposes is the Cessna. Cessna 172  carries the lowest risk and is in the top 10 safest ariplane.
                   

