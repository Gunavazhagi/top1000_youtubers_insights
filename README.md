# Top1000_Youtubers_Insights

## Problem Context:
"The dataset was obtained through data extraction from top YouTube content creators using the HypeAuditor platform. This dataset contains valuable information related to the presence and performance of these content creators on the world's largest video-sharing platform, YouTube. It includes various variables that provide insights into the creators' activities and metrics."

## Dataset variables:
Below is a detailed description of each of the variables included in the dataset, offering a comprehensive overview of the data's contents and potential analysis opportunities.
**Rank:** This variable indicates the position or ranking of the streamer on the list of top YouTube streamers. A lower number signifies a higher ranking.
**Username:** It is the streamer's username on YouTube, allowing for the unique identification of each content creator.
**Categories:** Represents the categories in which the streamer has tagged their content. Categories can span a wide variety of topics, including gaming, beauty, fashion, travel, comedy, and more.
**Subscribers:** Indicates the average number of subscribers the streamer's YouTube channel has. This value represents the regular following of content by the audience.
**Country:** Shows the average country of origin or location of the streamer. This can provide insights into the primary audience of the creator and their base of operations.
**Visits:** This variable records the average number of accumulated visits to the streamer's channel. It represents the average number of times the creator's videos have been viewed by viewers.
**Likes:** Indicates the average number of "Likes" received on the streamer's videos. "Likes" are an engagement metric that shows how many viewers appreciate the content.
**Comments:** Reflects the average number of comments left on the streamer's videos. Comments are an important form of audience interaction and participation.
**Links:** Provides links or URLs to the streamer's YouTube channels, allowing direct access to their content.
## Data Transformation Process:
    In this dataset categories and country column are in spanish language. To make the dataset more accessible, we translated the values in the "categories" and "country" columns from Spanish to English using SQL queries. Below are the SQL queries used for this purpose:
**UPDATE Categories name from Spanish from English**
UPDATE[dbo].[youtubers_df$]
SET Categories = 
    CASE
        WHEN Categories ='Animación' THEN 'Animation'
        WHEN Categories = 'Música y baile' THEN 'Music and Dance'
        WHEN Categories = 'Videojuegos' THEN 'Video Games'
        WHEN Categories = 'ASMR' THEN ' ASMR (Autonomous Sensory Meridian Response)'
        WHEN Categories = 'Animales y mascotas' THEN 'Animals and Pets'
		WHEN Categories = 'Humor' THEN  'Comedy'
        WHEN Categories = 'Juguetes' THEN 'Toys'
		WHEN Categories = 'Comida y bebida' THEN 'Food and Drink'
        WHEN Categories = 'Belleza' THEN 'Beauty'
		WHEN Categories =  'Moda' THEN  'Fashion'
        WHEN Categories ='Ciencia y tecnologìa' THEN ' Science and Technology'
		WHEN Categories = 'Coches y vehìculos' THEN 'Cars and Vehicles'
        WHEN Categories = 'Salud y autoayuda Deportes' THEN 'Health, and Self-Help'
		WHEN Categories ='Deportes' THEN 'Sports'
		WHEN Categories = 'Diseño/arte' THEN 'Design/Art'
        WHEN Categories = 'DIY y Life Hacks' THEN 'DIY and Life Hacks'
		WHEN Categories = 'Educación' THEN 'Education'
		WHEN Categories ='Fitness' THEN 'Fitness'
		WHEN Categories = 'Pelìculas' THEN 'Movies'
        WHEN Categories = 'Noticias y Polìtica' THEN 'News and Politicss'
		WHEN Categories ='Vlogs diarios' THEN 'Daily vlogs'
		WHEN Categories = 'Viajes'  THEN 'Travel'
        WHEN Categories = 'Espectáculos' THEN 'Entertainment'
        ELSE 'None'
		END
  Explanation: This query updates the "categories" column by translating Spanish category names to English.
  **UPDATE Country name from Spanish to English**

UPDATE[dbo].[youtubers_df$]
SET Country = 
    CASE
        WHEN Country = 'Bangladesh' THEN 'Bangladesh'
		WHEN Country = 'Brasil' THEN 'Brazil'
		WHEN Country = 'Colombia' THEN 'Colombia'
		WHEN Country = 'España' THEN 'Spain'
	    WHEN Country = 'Estados Unidos' THEN 'United States'
		WHEN Country = 'Francia' THEN 'France'
		WHEN Country = 'India' THEN 'India'
		WHEN Country = 'Inodonesia' THEN 'Indonesia'
		WHEN Country = 'México' THEN 'Mexico'
		WHEN Country = 'Pakistán' THEN 'Pakisthan'
		WHEN Country = 'Reino Unido' THEN 'United Kingdom'
		WHEN Country = 'Rusia' THEN 'Russia'
		WHEN Country = 'Turquìa' THEN 'Turkey'
	    ELSE 'Unknown'
		END
Explanation: This query updates the "country" column by translating Spanish country names to English.

## Data Visualization Process

Before diving into the insights, let's briefly discuss how the data visualizations were created using Power BI. The following steps were taken to analyze and visualize the top 1000 YouTubers' statistics:

1. **Data Preparation**: The dataset was loaded into Power BI, and any necessary data cleaning or formatting steps were performed.

2. **Querying and Transformation**: SQL queries and data transformations were used to shape the data, translate categories and country names, and prepare it for visualization.

3. **Visualization Creation**: Power BI's visualization tools were employed to create the charts, graphs, and tables that represent our insights.

Now, let's proceed to the insights and visualizations.

## Data Source: https://www.kaggle.com/datasets/computingvictor/top1000youtubers/
