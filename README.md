# Reddit_Unmasked
## TASK - <br><br>
1. Takes as input a reddit user’s profile URL.<br>
Example: <br> 
https://www.reddit.com/user/kojied/ <br>
https://www.reddit.com/user/Hungry-Move-6603/ <br>
2. Scrapes **comments and posts** created by the redditor.<br>
3. Builds a **User Persona** based on details found on their reddit. <br><br>
## APPROACH -<br><br>

### Web Scraping <br>
**Features**<br>
1) Asynchronous scraping using httpx.AsyncClient for improved performance.<br>
2) Parses key post details: title, author, score, comment count, subreddit, etc.<br>
3) Follows pagination and supports scraping multiple pages (max_pages).<br>
4) Lightweight custom logger for console output.<br>

Compatible with the "new", "top", and "controversial" post sort options.

**Key Libraries**<br>
1) **httpx** – for asynchronous web requests.<br>
2) **parsel** – for XPath-based HTML parsing.<br>
3) **pandas** – for storing the Data.<br>
#### Code
I have written all the code in ***Scraping.ipynb*** File. <br><br>
**How to use**<br>
Just provide the username and run all the  cells in the jupyter notebook.<br>
```bash
posts = await scrape_user_posts("reddit_username", sort="top", max_pages=3)
```
**This will scrape up to 3 pages of top posts from the specified user**.<br>

Same for comments -
```bash
comments = await scrape_user_comments("reddit_username", sort="top", max_pages=3)
```
**Saving the Data as CSV_FILES**<br><br>
*{username}_posts.csv* <br>
*{username}_comments.csv*<br>



