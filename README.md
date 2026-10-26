🛠️ Data Preprocessing & Feature Engineering
Data Loading: The anime.csv dataset was loaded into a pandas DataFrame.
Episodes Extraction: A custom parsing function, extract_episode, extracted the numeric string inside the parentheses (e.g., (64 eps)). The 'eps' substring was removed, and the column was cast to integer (int) for mathematical sorting.
Time Range Extraction: The extraction_time function parsed the text following the closing parenthesis to isolate the air date string (e.g., 'Apr 2011 - Sep 2011') and saved it as 'Total Time'.
Duration Calculation: Using datetime parsing and dateutil.relativedelta, the total duration in months was calculated and saved in the 'Months' column (adding +1 month to encompass the start month).
📊 Key Findings
Highest Rated Anime: Fullmetal Alchemist: Brotherhood with a score of 9.10.
Highest Episode Count: Gintama with 201 episodes.
Longest Running Anime: Ginga Eiyuu Densetsu which ran for 111 months (approximately 9 years, from Jan 1988 to Mar 1997).
 
