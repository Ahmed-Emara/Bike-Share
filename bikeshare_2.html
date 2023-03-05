import time
import pandas as pd
import numpy as np

CITY_DATA = { 'chicago': 'chicago.csv',
              'new york city': 'new_york_city.csv',
              'washington': 'washington.csv' }

# Defining input and validate to call it when needed to reduce repetitive code.
def input_and_validate(array, prompt_string, invalid_string):
    while True:
        entry = input(prompt_string).lower()

        if np.array(array).__contains__(entry):
            return entry
        else:
            print(invalid_string)

# filtering user inputs by calling input and validate def function.
def get_filters():
    """
    Asks user to specify a city, month, and day to analyze.

    Returns:
        (str) city - name of the city to analyze
        (str) month - name of the month to filter by, or "all" to apply no month filter
        (str) day - name of the day of week to filter by, or "all" to apply no day filter
    """
    
    print('Hello! Let\'s explore some US bikeshare data!')

    # get user input for city (chicago, new york city, washington). HINT: Use a while loop to handle invalid inputs
    cities = ["chicago" , "new york city" , "washington"]
    cities_prompt_message = "Enter City Name:\n1.chicago\n2.new york city\n3.washington\n"
    cities_invalid_message = "Enter a valid city!"
    city = input_and_validate(cities, cities_prompt_message, cities_invalid_message)


    # get user input for month (all, january, february, ... , june)
    months = ["all", "january", "february", "march", "april", "may", "june"]
    months_prompt_message = "Enter month: all, january, february, march, april, may, june\n"
    months_invalid_message = "Enter a valid month!"
    month = input_and_validate(months, months_prompt_message, months_invalid_message)
    


    # get user input for day of week (all, monday, tuesday, ... sunday)
    days = ["all", "monday", "tuesday", "wednessday", "thursday", "friday", "saturday", "sunday"]
    days_prompt_message = "Enter a day of week: all, monday, tuesday, wednessday, thursday, friday, saturday, sunday\n"
    days_invalid_message = "Enter a vaild a day of week"
    day = input_and_validate(days, days_prompt_message, days_invalid_message)

    print('-'*40)
    return city, month, day

# loading data from given files.
def load_data(city, month, day):
    """
    Loads data for the specified city and filters by month and day if applicable.
    
    Args:
        (str) city - name of the city to analyze
        (str) month - name of the month to filter by, or "all" to apply no month filter
        (str) day - name of the day of week to filter by, or "all" to apply no day filter
    Returns:
        df - Pandas DataFrame containing city data filtered by month and day
    """
    df = pd.read_csv(CITY_DATA[city])

   
    # Converting the Start Time column to datetime
    df['Start Time'] = pd.to_datetime(df['Start Time'])
    # Extracting month from the Start Time column to create an month column.
    df['month'] = df['Start Time'].dt.month
    # Extracting day of week from the Start Time column to create an day of week column.
    df['day_of_week'] = df['Start Time'].dt.day_name()
    # Extracting hour from the Start Time column to create an hour column.
    df['hour'] = df['Start Time'].dt.hour
    # Getting start & end station column by adding start station column values to end station column values.
    df["start_end_station"] = df["Start Station"] + " / " + df["End Station"]

   
    # Filtering by month.   
    if month != 'all':
        # Useing the index of the months list to get the corresponding int.
        months = ["all", "january", "february", "march", "april", "may", "june"]
        month = months.index(month) + 1
        # Filtering by month to create the new dataframe.
        df = df[df["month"] == month]

    
    # Filtering by day of week.
    if day != 'all':
        # Filtering by day of week to create the new dataframe.
        df = df[df["day_of_week"] == day.title()]


    return df

# Getting the mode to get common month, day of week & start hour.
def time_stats(df):
    """Displays statistics on the most frequent times of travel."""

    print('\nCalculating The Most Frequent Times of Travel...\n')
    start_time = time.time()

    # display the most common month
    popular_month = df['month'].mode()[0]
    print("popular month is ", popular_month)

    # display the most common day of week
    popular_day = df['day_of_week'].mode()[0]
    print("popular day of week is ", popular_day)

    # display the most common start hour
    popular_hour = df['hour'].mode()[0]
    print("popular hour is ", popular_hour)

    print("\nThis took %s seconds." % (time.time() - start_time))
    print('-'*40)

# Getting the mode to get common start station, end station & its combination.
def station_stats(df):
    """Displays statistics on the most popular stations and trip."""

    print('\nCalculating The Most Popular Stations and Trip...\n')
    start_time = time.time()

    # display most commonly used start station
    popular_start_station = df["Start Station"].mode()[0]
    print("popular start station is ", popular_start_station)

    # display most commonly used end station
    popular_end_station = df["End Station"].mode()[0]
    print("popular end station is ", popular_end_station)

    # display most frequent combination of start station and end station trip
    popular_start_end_station = df["start_end_station"].mode()[0]
    print("popular start and end station combinatiom is ", popular_start_end_station)

    print("\nThis took %s seconds." % (time.time() - start_time))
    print('-'*40)

# Using arithmetic and statistical Operations sum & mean to get total & average.
def trip_duration_stats(df):
    """Displays statistics on the total and average trip duration."""

    print('\nCalculating Trip Duration...\n')
    start_time = time.time()

    # display total travel time
    total_travel_time = df["Trip Duration"].sum().__round__()
    print("The total travel time is ", total_travel_time)

    # display mean travel time
    
    average_travel_time = df["Trip Duration"].mean().__round__()
    print("The average travel time is ", average_travel_time)

    print("\nThis took %s seconds." % (time.time() - start_time))
    print('-'*40)

# Using arithmetic and statistical Operations min, max, mode to get earliest, most recent, and most common year of birth.
def user_stats(df, should_calculate_gender_counts_and_birth):
    """Displays statistics on bikeshare users."""

    print('\nCalculating User Stats...\n')
    start_time = time.time()

    # Display counts of user types
    user_type_values_count = len(pd.unique(df["User Type"]))
    user_types_counts = df["User Type"].value_counts().to_frame()

    print("The count of distinct user type is", user_type_values_count)
    print(user_types_counts)

    if should_calculate_gender_counts_and_birth:
        # Display counts of gender
        gender_types_counts = df["Gender"].value_counts().to_frame()
        print(gender_types_counts)
        
        # Display earliest, most recent, and most common year of birth
        earliest_year_of_birth = df["Birth Year"].min()
        most_recent_year_of_birth = df["Birth Year"].max()
        most_common_year_of_birth = df["Birth Year"].mode()[0]

        print("Earliest year of birth is ", earliest_year_of_birth)
        print("Most recent year of birth is ", most_recent_year_of_birth)
        print("Most common year of birth is ", most_common_year_of_birth)



    print("\nThis took %s seconds." % (time.time() - start_time))
    print('-'*40)

# Using while loop to keep displaying row data as user like.
def display_raw_data(df):
    i = 0
    while i+5 < df.shape[0]:
        choices = ["yes", "no"]
        choices_prompt_message = "Would yoy like to read 5 rows of row data? (yes/no)\n"
        choices_invalid_message = "Invalid choice."
        choice = input_and_validate(choices, choices_prompt_message, choices_invalid_message)
        if choice == "yes":
            print(df.iloc[i:i+5])
            i += 5
        else:
            print("Thank you!")
            break
    

def main():

    while True:
        city, month, day = get_filters()
        df = load_data(city, month, day)

        time_stats(df)
        station_stats(df)
        trip_duration_stats(df)
        user_stats(df, city != "washington")
        display_raw_data(df)
        restart = input('\nWould you like to restart? Enter yes or no.\n')
        if restart.lower() != 'yes':
            break


if __name__ == "__main__":
	main()
