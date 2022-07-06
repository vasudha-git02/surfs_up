# Surf's Up

## Project Overview
While you were in Hawaii last year you found a new passion for surfing. You have been coming up with a plan that will let you not just return to Hawaii but live there forever. You finally come up with an idea that you think is foolproof. A surf 'n' shake shop serving surfboards and icecream to locals, tourists and of course yourself. you have some savings you are willing to invest but we will need some real investor backing to get this off the ground. So after putting together a strong business plan you reach out to an investor W.Avy who is famous for his love of surfing. You first meeting with him goes extremely well but he has one concern. What about the weather? He's extremely serious 
about this. He invested in a surf shop early in his career. However he didnt ask for any weather analysis and that early venture was rained out of existence. W.Avy knows you've been learning how to properly analyze data and asks if you can run some analytics on a weather dataset he has from the very island where you'd like to open your shop: The beautiful Oahu. 

## Resources
- Data Source : city_data.csv, ride_data.csv,PyBer_ride_data.csv
- Software    : Python 3.8, Visual studio code 1.67.2, Jupyter notebook

## Results 
Below are the results of the temperature observations for the months of June and December

- June
  - Total count is 1700
  - The mean is 74.9
  - The standard deviation is 3.25		
  - The minimum temperature is 64
  - The maximum temperature is 85

  
  Below is the image corresponding to the results.
  
  
<img width="200" alt="image" src="https://user-images.githubusercontent.com/104597335/177475998-be4a7091-696d-4d17-af47-736d2011e803.png">

  
- December
  - Total count is 1517
  - The mean is 71.04
  - The standard deviation is 3.74		
  - The minimum temperature is 56
  - The maximum temperature is 83

Below is the image corresponding to the results.


<img width="200" alt="image" src="https://user-images.githubusercontent.com/104597335/177476086-e8f863b5-65c7-4736-916b-49fb06f45378.png">



## Challenge Summary
When we look at the results for the month of June and December the minimum and maximum temperatures are more in June compared to December and so are the mean and standard deviation

## Additional queries
To get the precipitation data for the months of June and December
results_june = session.query((Measurement.prcp),(Measurement.date)).filter(extract("month",Measurement.date)==6).all()
df_june = pd.DataFrame(results_june, columns=['date','precipitation'])
results_dec = session.query((Measurement.prcp),(Measurement.date)).filter(extract("month",Measurement.date)==12).all()
df_dec = pd.DataFrame(results_dec, columns=['date','precipitation'])
df_june.describe()
df_dec.describe()
