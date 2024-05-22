# Hotel-Booking-EDA-Data-Analysis-Python
Hotel Booking EDA Data Analysis Python


Hotel Booking EDA Data Analysis Python
Type text or HTML
<!-- wp:paragraph -->
<p>In this project, we conducted a comprehensive data analysis on a hotel booking dataset to identify key issues affecting booking performance and revenue.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Using Python and its powerful data analysis libraries such as Pandas, Matplotlib, and Seaborn, we explored various aspects of the dataset, including cancellation rates, booking distribution, pricing strategies, customer types, seasonal trends, lead times, and the reliance on online travel agencies.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Through visualizations and statistical analysis, we uncovered insights that can help hotels optimize their marketing, pricing, and operational strategies to improve overall performance and customer satisfaction.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3 class="wp-block-heading" id="h-problem-statement">Problem Statement</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The hotel booking dataset reveals several issues that need to be addressed:</p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->
<ol><!-- wp:list-item -->
<li><strong>High Cancellation Rate</strong>:</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>A significant portion of bookings are being canceled, especially for City Hotels.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:list {"ordered":true} -->
<ol><!-- wp:list-item -->
<li><strong>Uneven Distribution of Bookings</strong>:</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>City Hotels receive a higher number of bookings compared to Resort Hotels, indicating a potential imbalance in marketing or pricing strategies.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:list {"ordered":true} -->
<ol><!-- wp:list-item -->
<li><strong>Pricing Inefficiencies</strong>:</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>The Average Daily Rate (ADR) for Resort Hotels is higher, yet they receive fewer bookings. This suggests that pricing strategies may not be optimized.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:list {"ordered":true} -->
<ol><!-- wp:list-item -->
<li><strong>Customer Type Imbalance</strong>:</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>Transient customers dominate the bookings, while other customer types (Contract, Group, etc.) are underrepresented.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:list {"ordered":true} -->
<ol><!-- wp:list-item -->
<li><strong>Seasonal Booking Trends</strong>:</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>There are significant peaks in bookings during the summer months (July and August), which may lead to overbooking issues or underutilization during off-peak seasons.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:list {"ordered":true} -->
<ol><!-- wp:list-item -->
<li><strong>Lead Time Distribution</strong>:</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>Most bookings are made with a lead time of less than 100 days, indicating a potential for optimizing early bird discounts or last-minute deals.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:list {"ordered":true} -->
<ol><!-- wp:list-item -->
<li><strong>Dependence on Online Travel Agencies (OTAs)</strong>:</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>The majority of bookings come through Online Travel Agencies, suggesting a heavy reliance on these channels, which may affect profit margins.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:list {"ordered":true} -->
<ol><!-- wp:list-item -->
<li><strong>Geographic Concentration</strong>:</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>The majority of bookings are from a limited number of countries, indicating potential untapped markets.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Addressing these problems through strategic adjustments in pricing, marketing, customer service, and distribution channels will help improve overall booking performance, reduce cancellations, and optimize revenue.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3 class="wp-block-heading" id="h-explanation-of-each-line-and-function">Explanation of Each Line and Function</h3>
<!-- /wp:heading -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre>import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load the dataset
file_path = '/mnt/data/hotel_booking.csv'
df = pd.read_csv(file_path)</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true} -->
<ol><!-- wp:list-item -->
<li><strong>Import Libraries</strong>: We import the necessary libraries, <code>pandas</code> for data manipulation, <code>seaborn</code> and <code>matplotlib.pyplot</code> for data visualization.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong>Load Dataset</strong>: The dataset is loaded into a DataFrame <code>df</code> from the specified file path.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre># Display the first few rows of the dataset
print(df.head())</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true,"start":3} -->
<ol start="3"><!-- wp:list-item -->
<li><strong>Preview Data</strong>: Display the first few rows of the dataset to get an initial look at the data.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre># Display the structure of the dataset
print(df.info())</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true,"start":4} -->
<ol start="4"><!-- wp:list-item -->
<li><strong>Data Structure</strong>: Print the structure of the dataset, showing information about the columns, data types, and non-null counts.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre># Check for missing values
missing_values = df.isnull().sum()
print(missing_values[missing_values &gt; 0])</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true,"start":5} -->
<ol start="5"><!-- wp:list-item -->
<li><strong>Check for Missing Values</strong>: Identify columns with missing values and display the count of missing values for each.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre># Handle missing values (drop rows with missing values for simplicity)
df = df.dropna()

# Verify no missing values remain
print(df.isnull().sum())</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true,"start":6} -->
<ol start="6"><!-- wp:list-item -->
<li><strong>Handle Missing Values</strong>: Drop rows with missing values to simplify the analysis. Verify that no missing values remain.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre># Display the data types of each column
print(df.dtypes)</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true,"start":7} -->
<ol start="7"><!-- wp:list-item -->
<li><strong>Display Data Types</strong>: Show the data types of each column in the dataset.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre># Select numerical columns for correlation analysis
numerical_columns = df.select_dtypes(include=['float64', 'int64']).columns
print(&quot;Numerical columns:&quot;, numerical_columns)</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true,"start":8} -->
<ol start="8"><!-- wp:list-item -->
<li><strong>Select Numerical Columns</strong>: Select columns with numerical data types for correlation analysis.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre># Compute the correlation matrix for numerical columns
correlations = df[numerical_columns].corr()
print(correlations)</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true,"start":9} -->
<ol start="9"><!-- wp:list-item -->
<li><strong>Correlation Matrix</strong>: Compute and print the correlation matrix for numerical columns to identify relationships between them.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre># Visualize correlations
plt.figure(figsize=(10, 8))
sns.heatmap(correlations, annot=True, cmap='coolwarm')
plt.title('Correlation Matrix')
plt.show()</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true,"start":10} -->
<ol start="10"><!-- wp:list-item -->
<li><strong>Visualize Correlations</strong>: Create a heatmap to visualize the correlation matrix, showing the strength and direction of relationships between numerical variables.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre># Distribution of Bookings by Hotel Type
plt.figure(figsize=(10, 6))
sns.countplot(data=df, x='hotel')
plt.title('Distribution of Bookings by Hotel Type')
plt.xlabel('Hotel Type')
plt.ylabel('Number of Bookings')
plt.show()</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true,"start":11} -->
<ol start="11"><!-- wp:list-item -->
<li><strong>Bookings by Hotel Type</strong>: Plot the distribution of bookings by hotel type to see which type of hotel receives more bookings.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre># Average Daily Rate (ADR) by Hotel Type
plt.figure(figsize=(10, 6))
sns.boxplot(data=df, x='hotel', y='adr')
plt.title('Average Daily Rate (ADR) by Hotel Type')
plt.xlabel('Hotel Type')
plt.ylabel('ADR')
plt.show()</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true,"start":12} -->
<ol start="12"><!-- wp:list-item -->
<li><strong>Average Daily Rate by Hotel Type</strong>: Create a boxplot to compare the average daily rate between different hotel types.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre># Bookings by Customer Type
plt.figure(figsize=(10, 6))
sns.countplot(data=df, x='customer_type')
plt.title('Bookings by Customer Type')
plt.xlabel('Customer Type')
plt.ylabel('Number of Bookings')
plt.show()</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true,"start":13} -->
<ol start="13"><!-- wp:list-item -->
<li><strong>Bookings by Customer Type</strong>: Plot the distribution of bookings by customer type to see the most common customer types.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre># Bookings by Market Segment
plt.figure(figsize=(10, 6))
sns.countplot(data=df, x='market_segment')
plt.title('Bookings by Market Segment')
plt.xlabel('Market Segment')
plt.ylabel('Number of Bookings')
plt.show()</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true,"start":14} -->
<ol start="14"><!-- wp:list-item -->
<li><strong>Bookings by Market Segment</strong>: Visualize the distribution of bookings by market segment to identify the most important market segments.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre># Booking Cancellations
plt.figure(figsize=(10, 6))
sns.countplot(data=df, x='is_canceled')
plt.title('Booking Cancellations')
plt.xlabel('Is Canceled')
plt.ylabel('Number of Bookings')
plt.show()</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true,"start":15} -->
<ol start="15"><!-- wp:list-item -->
<li><strong>Booking Cancellations</strong>: Plot the distribution of booking cancellations to understand the proportion of canceled bookings.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre># Lead Time Analysis
plt.figure(figsize=(10, 6))
sns.histplot(df['lead_time'], bins=30, kde=True)
plt.title('Lead Time Distribution')
plt.xlabel('Lead Time')
plt.ylabel('Frequency')
plt.show()</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true,"start":16} -->
<ol start="16"><!-- wp:list-item -->
<li><strong>Lead Time Analysis</strong>: Create a histogram to visualize the distribution of lead times for bookings.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre># Monthly Booking Trends
df['arrival_date_month'] = pd.Categorical(df['arrival_date_month'], categories=[
    'January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'], ordered=True)

monthly_bookings = df['arrival_date_month'].value_counts().sort_index()

plt.figure(figsize=(12, 6))
sns.barplot(x=monthly_bookings.index, y=monthly_bookings.values)
plt.title('Monthly Booking Trends')
plt.xlabel('Month')
plt.ylabel('Number of Bookings')
plt.xticks(rotation=45)
plt.show()</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true,"start":17} -->
<ol start="17"><!-- wp:list-item -->
<li><strong>Monthly Booking Trends</strong>: Plot the number of bookings by month to identify peak booking periods.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:heading {"level":3} -->
<h3 class="wp-block-heading" id="h-more-visuals">More Visuals </h3>
<!-- /wp:heading -->

<!-- wp:codemirror-blocks/code-block {"fileName":"query.sql","mode":"sql","mime":"text/x-sql"} -->
<div class="wp-block-codemirror-blocks-code-block code-block"><pre># Bookings by Distribution Channel
plt.figure(figsize=(10, 6))
sns.countplot(data=df, x='distribution_channel')
plt.title('Bookings by Distribution Channel')
plt.xlabel('Distribution Channel')
plt.ylabel('Number of Bookings')
plt.show()

# Bookings by Meal Type
plt.figure(figsize=(10, 6))
sns.countplot(data=df, x='meal')
plt.title('Bookings by Meal Type')
plt.xlabel('Meal Type')
plt.ylabel('Number of Bookings')
plt.show()

# Average Lead Time by Hotel Type
plt.figure(figsize=(10, 6))
sns.boxplot(data=df, x='hotel', y='lead_time')
plt.title('Average Lead Time by Hotel Type')
plt.xlabel('Hotel Type')
plt.ylabel('Lead Time')
plt.show()

# Booking Changes by Hotel Type
plt.figure(figsize=(10, 6))
sns.boxplot(data=df, x='hotel', y='booking_changes')
plt.title('Booking Changes by Hotel Type')
plt.xlabel('Hotel Type')
plt.ylabel('Number of Booking Changes')
plt.show()

# Bookings by Country
top_countries = df['country'].value_counts().head(10)
plt.figure(figsize=(10, 6))
sns.barplot(x=top_countries.index, y=top_countries.values)
plt.title('Top 10 Countries by Number of Bookings')
plt.xlabel('Country')
plt.ylabel('Number of Bookings')
plt.xticks(rotation=45)
plt.show()</pre></div>
<!-- /wp:codemirror-blocks/code-block -->

<!-- wp:list {"ordered":true,"start":18} -->
<ol start="18"><!-- wp:list-item -->
<li><strong>Bookings by Distribution Channel</strong>: Plot the distribution of bookings by distribution channel to see which channels are most effective.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong>Bookings by Meal Type</strong>: Visualize the distribution of bookings by meal type to understand customer preferences.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong>Average Lead Time by Hotel Type</strong>: Compare the average lead time for bookings between different hotel types.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong>Booking Changes by Hotel Type</strong>: Compare the number of booking changes between different hotel types.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong>Bookings by Country</strong>: Plot the number of bookings by country, focusing on the top 10 countries.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:heading {"level":3} -->
<h3 class="wp-block-heading" id="h-summary-of-key-findings-and-solutions">Summary of Key Findings and Solutions</h3>
<!-- /wp:heading -->

<!-- wp:heading {"level":4} -->
<h4 class="wp-block-heading" id="h-key-findings">Key Findings:</h4>
<!-- /wp:heading -->

<!-- wp:list {"ordered":true} -->
<ol><!-- wp:list-item -->
<li><strong>Distribution of Bookings</strong>:</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>Most bookings are for the City Hotel.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>The average daily rate is higher for the Resort Hotel.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>The majority of bookings are made by Transient customers.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Online TA is the most common market segment.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>37% of bookings are canceled.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Lead time distribution shows most bookings are made less than 100 days in advance.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Peak booking months are July and August.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>TA/TO is the most common distribution channel.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>The most common meal type is BB (Bed &amp; Breakfast).</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Average lead time is higher for City Hotel than Resort Hotel.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Booking changes are slightly higher for City Hotel.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Portugal is the country with the highest number of bookings.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:heading {"level":4} -->
<h4 class="wp-block-heading" id="h-solutions">Solutions:</h4>
<!-- /wp:heading -->

<!-- wp:list {"ordered":true} -->
<ol><!-- wp:list-item -->
<li><strong>Reduce Cancellations</strong>:</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>Implement stricter cancellation policies, especially for City Hotels.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Offer incentives for non-cancelable bookings.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:list {"ordered":true} -->
<ol><!-- wp:list-item -->
<li><strong>Optimize Pricing</strong>:</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>Adjust pricing strategies for Resort Hotels to increase bookings.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Consider dynamic pricing based on booking lead times and peak seasons.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:list {"ordered":true} -->
<ol><!-- wp:list-item -->
<li><strong>Target Marketing Efforts</strong>:</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>Focus marketing efforts on the Transient customer segment.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Strengthen partnerships with Online Travel Agencies (OTAs) to leverage their reach.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:list {"ordered":true} -->
<ol><!-- wp:list-item -->
<li><strong>Improve Customer Experience</strong>:</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>Enhance the meal offerings, focusing on the most popular BB meal type.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Ensure a smooth booking change process to improve customer satisfaction.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:list {"ordered":true} -->
<ol><!-- wp:list-item -->
<li><strong>Expand International Reach</strong>:</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:list -->
<ul><!-- wp:list-item -->
<li>Target marketing campaigns to countries with fewer bookings but high potential.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Customize offerings based on preferences of top countries like Portugal.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>These insights and solutions should help the hotel improve its booking performance, reduce cancellations, and optimize its marketing and pricing strategies.</p>
<!-- /wp:paragraph -->
