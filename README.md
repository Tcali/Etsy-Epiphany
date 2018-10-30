# Etsy-Epiphany

Using API, NLP, and Machine learning, I will provide review mapping and sentiment analysis to enable Etsy shop owners to identify what qualities of their products are favorable or not, be able to address those during production, and thereby possibly increase their chances of getting favorited.

# Thinkful Capstone Project: "Etsy Epiphany"
### By Tiani Calip
# Problem Addressed
## Personal Interest and Problem
My mom owns an Etsy online store and is constantly stressing out about how well her products are doing, what price she should be listing her products at, and what product she should make and sell next. I want to create a solution for her to be able to identify what the most popular products are, how the reviews trend over time, and how the sentiment of review text maps against the review ratings. This way, she would be able to see how her products are doing compared to similar items on Etsy, and be able to respond to the demand for certain types of popular items and create and sell her own. Sometimes, she doesn’t understand why one shirt sells more than another. Providing review mapping and sentiment analysis will allow her and other users to identify what qualities of their products are favorable or not, be able to address those during production, and thereby possibly increase their chance of getting favorited.

## Goal
Using NLP and machine learning techniques, I will identify the top 30 important qualities (description, title, and tags) needed for any given Etsy user to use to improve their chance of getting favorited.

## Hypothesis
By using machine learning and NLP, I can give suggesthions on product descriptions and help a store increase their favorites by 5%.

### Gameplan:
Get the shop info for every shop that can be found with the keyword: "Disney"
Use shop_ids to get the listing info
Use the value of the feedback to train a classification model to know when a sentiment is positive or negative
Identify the most important digrams/phrases in a shop's collective messages that lead to a positive sentiment
Compare prices of the listings that have those positive sentiments
Compare # of favorites to price of the listings with the positive sentiments
Compare that with my mom's sentiments and prices and give suggestions for price and product qualities

fork out positive reviews and negative. see what ppl are saying abt both, give advice to the stores for what they could change abt their stores and improve.
give suggestions abt what shop can do that others/competetors are doing

## Impact
I can determine the important qualities of a product that lead to the best reviews and review sentiments, then identify the most optimal price to increase the number of favorites. This can help my mom and any other prospective users to get ideas for their next products, and have confidence to list the products at an optimal price for both the seller and the buyer.

## Dataset
Data source = Etsy itself! I used the Etsy API to collect the data in real time from shops that have the keyword "Disney"

## Existing Efforts
No existing Etsy apps look at both review scores and sentiments in an effort to identofy important qualities. I'm excited to see if I can be the first!

## Project Concerns
### Assumptions
I am making the assumption that the limits and offset that I chose for my API requests will give me a good representation of the Disney themed Etsy store population

### Risks (of data or models)
This is my first time using an API outside of the Thinkful course. I do not expect it to be an easy learning curve.
Some data that would be ideal requires an OAuthentification, which means any user I want to scrape data from needs to verify and approve my data scraping. I do not want random users to feel threatened by my data grabbing, so I will have to go in a roundabout way to grab the data I want.

### Questions Resulting
What is the best way to measure my scenario (binary outcome, probability outcome, or quantitative outcome)?

## Outcomes
__Top 10 vocabulary:__
Descriptions: 'button', 'band', 'ornament', 'check', 'epcot', 'fits', 'Christmas', 'shirts', 'listings', 'image'
Messages: 'magic', 'shipping', 'trip', 'christmas', 'ordered', 'shirts', 'family', 'disney', 'husband', 'pin'
Tags: 'epcot', 'band', 'vinyl', 'magic', 'ornament', 'custom', 'silver', 'movie', 'cruise', 'tank'

__Bottom 10 vocabulary:__
Descriptions: 'return', 'buy', 'item', 'cost', 'hang', 'pictures', 'mail', 'shirt', 'shipping', 'design
Messages: None (Makes sense because no one would favorite an item they didn't like)
Tags: 'stitch', 'new', 'fantasy', 'vacation', 'wars', 'star', 'girls', 'gold', 'vintage', 'book'

It seems:

As time increases since creation, the number of favorites decrease
As the number of listings per shop increases, the number of favorites increases
As the price increases, the number of favorites slightly increases
As the rating value of the shop increases, the number of favorites slightly decreases
According to our correlation matrix, the strongest correlation is 0.52, between the number of favorites and listing active count.

## Future work:
Look at the number of sales of those listing, which requires shop owner access and authentication to grab that data. Compare sales to price of the listings with the positive sentiments.
See how changing the descriptions, titles, tags, and prices can increase favorites and sales.
