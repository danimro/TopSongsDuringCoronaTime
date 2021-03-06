# TopSongsDuringCoronaTime
This project is part of our top corona songs analysis project of the course **Topics in Digital Humanities** Spring/2020

# Main purpose of the Project
This project aims to find out how these crazy times of dealing with the COVID19 pandemic effect human emotions through music
we took different countries from across the globe, some were more influenced by the pandemic and for some it hit hard only during the last months and later. For each country, we took data about the cases and deaths from COVID19 as well as data about the 20 most heard songs from each week since the virus started spreading and analyzing the emotions in those songs

## Used API's
- Lyric Genius API
- NLTK Sentiment Analysis Algorithm which uses **'mymemory.translated.net/api'** to translate non eng text to eng.
- corona API using **https://api.thevirustracker.com/**
- Spotify API

## Main Functions
| **Fucntion Name** | **Description**|
| --- | ---|
| corona_stats_by_country() | Function that calculates the stat of corona in a specific country. |
| get_list_of_all_songs(by_country) |		Function which creates json files which contain the data of the songs of a specific country from START_DATE_SONGS until END_DATE_SONGS.|
| analysis_songs_by_country_monthly(by_country) |		Function that creates a list of all analysis of a country from START_DATE until END_DATE_SONGS after the algorithem ran. |
| analysis_songs_by_country_monthly_divided_to_weekly(by_country) | Function which saves the monthly data into csv files divided into weeks. |
| all_analysis() | Functio which returns the analysis of all countries and the number of positive, negative and neutral songs during the whole period. |

## Order of Events
### Corona Statistics
First we gathers all the inforamation regarding corona statistics from each of the chosen countries with the next keys:
- Start Date
- End Date
- New cases
- New Deaths
- Total Cases 
- Total Deaths

### Songs Lists
We gathers on each week from november until may the top 20 songs on spotify for each chosen country.
We gathers together the weeks from each month and saved:
- song_artist
- track number
- country
- start date
- end date

### Lyrics of Top songs
After gathering the top songs lists, we had to get the lyrics of those songs in order to run the analysis alogorithm, as this algorithm runs on the works of the songs and based on lexicon and rule-based  it returns the sentiment analysis of the text.
In order to do so,we used the lyrics genius api.

### Ran NLTK Sentiment Analysis Algorithm on The lyrics
With those lyrics we used the algorith and saved its results into a data stracture with the next keys:
- Negative
- Positive
- Neutral
- Start Date
- End Date  
- Total cases


