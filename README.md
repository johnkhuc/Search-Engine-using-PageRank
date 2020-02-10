# Search Engine 
> Using a web crawler to put information into a sql database and then ranking the websites based on the old Google search engine's page rank algorithm

`John Khuc`

## Visualization of Nodes!
![Recordit GIF](http://g.recordit.co/rwyyKhcTq5.gif)

## Table of Contents
- [Libraries Used](#libraries-used)
- [Results](#results)
- [Making Your Own Example](#making-your-own-example)

## Libraries Used
- **BeautifulSoup4** (formatting web pages and making them readable)
- **SQLite** (storing data for ranks and links)
- **URLlib** (for parsing web pages and links)
- **SSL** (Secure Sockets Layer) (for certification)

## Results
- First, using **WebCrawler.py**, we choose a starting point for gathering websites. In this case, I pick github.com.
![first](https://i.gyazo.com/f3dbfbdd282049da8bf8b72a0c869664.png)
- Currently, using **ShowRank.py**, they are stored in a sqlite database with default rank information (1.0)
![second](https://i.gyazo.com/b578f0317f7efd6442a6cd799956e40e.png)
- Now, lets use **PageRank.py** to update the information! I use 10 iterations because the overall change will converge to a miniscule amount.
![third](https://i.gyazo.com/b58a65cbbfbb7808f079fd0711f2cdea.png)
- After the page rank algorithm, using **ShowRank.py**, the updated scores are shown in the third parameter with some websites having more weight (higher scores) and others pushed way below 1.0.
![fourth](https://i.gyazo.com/0212504ab98a6a48aa2834f09bf09891.png) 
- Bonus: Let's make the node visualizer to see the size of the connections of each node. Here, I chose 20 nodes.
![fifth](https://i.gyazo.com/a9388db28d09b904bd24bdd22ca8c20d.png)
- Here it is! Check the gif at the start of the document if you haven't already!
![sixth](https://i.gyazo.com/3659f089e43fc356bc48edde78f295d8.png)

## Making Your Own Example
1. Run **WebCrawler.py**, enter a starting url and number of iterations
  - To restart the process, simply delete your sqlite database.
2. Run **PageRank.py**
  - You can reset the ranks of using the page rank algorithm using **ResetRank.py**
3. Run **WebCrawlerToJson.py** to format the data
4. Open **Force.html** in your browser and play with the nodes
