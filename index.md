## About Me

Welcome to my GitHub portfolio dedicated to data analysis and data science! I'm a junior at San Francisco State University majoring in Computer Science. I'm also a mentor for DataJam at Pittsburgh DataWorks. My passion for data is unwavering, and I'm actively seeking opportunities to break into the field of Data Science and Analytics. Feel free to reach out to me via email or mobile for any opportunities or collaborations.

## Skills
- **Programming**: Python (NumPy, Pandas), R, SQL
- **Visualization**: Tableau, Python (Matplotlib, Seaborn), R

## Projects

### Project Title: Analyzing Car Break-Ins in San Francisco
[![View on GitHub](https://img.shields.io/badge/GitHub-View_on_GitHub-blue?logo=GitHub)](https://github.com/cmeddata/SFO-Car-BreakIn/blob/main/SFO_BreakIn.ipynb)

Project Description:
In response to the rising number of car break-ins in San Francisco, I conducted a data exploration project using reported crime data from DataSF. The original dataset contained over 700,000 reported crimes, which required data cleaning to focus on the specific information relevant to my project. I used the Python Pandas library to filter the data, extracting only incidents categorized as "Larceny Theft" with the subcategory "Larceny -
  
```break
#reads csv file
Police_Report_df = pd.read_csv("Police_Report.csv")

#filters the csv file to Larceny Theft with Subcategory of Larceny from vehicle. then sets it to Police_Report_df
condition = (Police_Report_df['Incident Category'] == 'Larceny Theft') & (Police_Report_df['Incident Subcategory'] == 'Larceny - From Vehicle')
Police_Report_df = Police_Report_df[condition]
```

With the cleaned dataset in hand, I proceeded to analyze which neighborhoods in San Francisco had the highest number of car break-ins. To visualize this, I created a bar plot to illustrate the distribution of car break-ins across different neighborhoods.


```break
#Analysis by Neighborhood
def Analysis_by_Neighborhood(data):
    # Count the number of incidents for each neighborhood
    neighborhood_counts = Police_Report_df['Analysis Neighborhood'].value_counts()

    # Create a bar plot
    plt.figure(figsize=(10, 5))  # Adjust the figure size as needed
    neighborhood_counts.plot(kind='bar', color='lightcoral')
    plt.title('Car Break-ins by Neighbourhood')
    plt.xlabel('Neighborhood')
    plt.ylabel('Frequency')
    plt.xticks(rotation=90)  # Rotate x-axis labels for better readability
    plt.grid(axis='y', linestyle='--', alpha=0.7)
    plt.show()
```

 ![Neighbourhood](https://github.com/cmeddata/cmeddata.github.io/assets/124543750/2b34a2f0-846d-42be-bf8a-e1fd25908f86)

The resulting visualization provides valuable insights into the neighborhoods with the highest occurrence of car break-ins, enabling better understanding and informed decision-making.

This project allowed me to leverage data analysis techniques to address a real-world issue and can serve as a valuable addition to my project portfolio.





# Project Title: Assessing COVID-19 in San Francisco: A closer look at Neighborhoods and its impact on COVID-19 cases 
[![View on GitHub](https://img.shields.io/badge/GitHub-View_on_GitHub-blue?logo=GitHub)](https://github.com/cmeddata/sf-covid19-neighborhood-analysis)

![Poster](https://github.com/cmeddata/cmeddata.github.io/assets/124543750/b8999ef0-0ec0-49f1-9749-d37902712b0b)


## Project Description
In this project, I conducted a comprehensive analysis of neighborhoods in San Francisco and their potential impact on the cumulative rate of COVID-19. I utilized Excel to perform this analysis, employing various statistical techniques to explore the relationships between several independent variables and the dependent variable, which was the cumulative rate of COVID-19 cases.

The independent variables I considered in my analysis included the poverty rate, longitude, latitude, square miles, square feet, population, and the percentage of different ethnic groups in each neighborhood. By gathering and organizing this data, I aimed to uncover any potential patterns or correlations that could shed light on the factors influencing the spread of COVID-19 within the city.

Through data visualization, regression analysis, and other statistical methods, I was able to gain valuable insights into the complex interplay between these variables and the COVID-19 rates in San Francisco neighborhoods. This project not only honed my data analysis skills but also contributed to a better understanding of the factors that play a role in the pandemic's impact at the local level.

Overall, this analysis provides a valuable contribution to the ongoing efforts to comprehend and combat the COVID-19 pandemic. It showcases my ability to use Excel as a powerful tool for data analysis and offers insights into the unique dynamics of San Francisco's neighborhoods in relation to the virus's spread.




<center>© 2023 Carlos De Leon. Powered by Jekyll and the Minimal Theme.</center>

