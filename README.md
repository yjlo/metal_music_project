# Metal Around The World
##### Creator: Yan-Jen Lo &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Course: CMCS320 (Data Science)

<img src='Images/cover.jpg'>

## Project Links

<table>
  <tr>
    <th><Big>Menu</Big></th>
    <th><Big>Featured Python Libraries</Big></th>
    <th><Big>Links / References</Big></th>
  </tr>
  <tr>
    <td align="center"><Big><b>Part I: Web Scrapping</b></Big></td>
    <td>
        <table>
            <tr><td>Pandas</td></tr>
            <tr><td>BeautifulSoup</td></tr>
            <tr><td>Requests</td></tr>
            <tr><td>Asyncio (Asynchronous I/O)</td></tr>
            <tr><td>Aiohttp (HTTP Client/Server for Asyncio)</td></tr>
            <tr><td>JavaScript Object Notation (JSON)</td></tr>
            <tr><td>Comma Separated Values (CSV)</td></tr>
            <tr><td>Re (Regular Expressions)</td></tr>
        </table>
    </td>
    <td>
        <table>
            <tr><td><a href="https://www.metal-archives.com">Encyclopedia Metallum (The Metal Archives)</a></td></tr>
            <tr><td><a href="https://en.wikipedia.org/wiki/List_of_countries_and_dependencies_by_population">Wikipedia World Population</a></td></tr>
            <tr><td><a href="http://statisticstimes.com/geography/countries-by-continents.php">Countries By Continent</a></td></tr>
            <tr><td><a href="https://pawelmhm.github.io/asyncio/python/aiohttp/2016/04/22/asyncio-aiohttp.html">Asyncio / Aiohttp Example</a></td></tr>
            <tr><td><a href="https://github.com/jonchar/ma-scraper">GitHub: jonchar's Metal Archives Scraper</a></td></tr>
        </table>
    </td>
  </tr>
  <tr>
    <td align="center"><Big><b>Part II: Analysis With World Population</b></Big></td>  
    <td>
        <table>
            <tr><td>NumPy</td></tr>
            <tr><td>Matplotlib</td></tr>
            <tr><td>Seaborn</td></tr>
        </table>
    </td>
    <td>
        <table>
            <tr><td><a href="https://github.com/datasets/geo-countries/tree/master/data">World GeoJSON</a></td></tr>
            <tr><td><a href="https://blog.dominodatalab.com/creating-interactive-crime-maps-with-folium/">Interactive Maps With Folium </a></td></tr>
            <tr><td><a href="https://www.thetoptens.com/countries-with-metal-bands-per-capita-2016/">Top 10 Metal Countries</a></td></tr>
        </table>
    </td>
  </tr>
  <tr>
    <td align="center"><Big><b>Part III: Sub-Genre Analysis</b></Big></td>
    <td>
        <table>
            <tr><td>Matplotlib</td></tr>
            <tr><td>Seaborn</td></tr>
            <tr><td>Folium</td></tr>
        </table>
    </td>
    <td> 
        <table>
            <tr><td><a href="https://mapofmetal.com/">Map of Metal</a></td></tr>
            <tr><td><a href="https://metal.mit.edu/brief-history-metal">Brief History of Metal (MIT)</a></td></tr>
        </table>
    </td>
  </tr>
</table>

## Introduction

### Inspiration
><b>Kaggle's Metal by </b><a href="https://www.kaggle.com/mrpantherson/metal-by-nation/data"><b>Nation and Genre</b></a>  <b>Data</b>

While looking around for a data set to use, I stumbled upon this <b>Kaggle</b> entry on metal bands. Being a metal head since middle school, this peaked my interest like no other data set I've seen so far. Download the dataset with the link below (you need to creat a free account to download from <b>Kaggle</b>).

<table>
    <tr>
        <th>Link</th>
        <th>Contents</th>
    </tr>
    <tr>
        <td rowspan="2"><a href="https://www.kaggle.com/mrpantherson/metal-by-nation/downloads/metal-bands-by-nation.zip"><big><b>Kaggle</b></big></a>
        <td><b>metal_bands_2017.csv</b></td>
    </tr>
    <tr><td><b>world_population_1960_2015.csv</b></td></tr>
</table>

The dataset had only <b>5000</b> metal bands and the world population data didn't go up to 2018. Also if you check out this [kaggle notebook](https://www.kaggle.com/mrpantherson/metal-by-nation-and-genre/notebook), someone has already analyzed the data. I wanted to see for myself if the analysis for this dataset still holds for the <b>Encyclopedia Metallum</b> data which is <b>24x larger</b>.

### Why Encyclopedia Metallum?
<table>
    <tr align="left">
        <th><Big>Benefits</Big></th>
        <th><Big>Drawbacks</Big></th>
    </tr>
    <tr align="left">
        <td>Large Database</td>
        <td>Subjective Band Entry Submissions Acceptance<b>*</b></td>
    </tr>
    <tr align="left">
        <td>Band Entry Submissions Heavily Monitored</td>
        <td>Information Error (Rare)</td>
    </tr>
    <tr align="left">
        <td>Users Worldwide Contribute Entries</td>
        <td>No Ready-Made Data / RESTful API<b>**</b></td>
    </tr>
</table>

><b>\*What bands that are considered metal is determined by <b>administrators</b>, so some that are considered metal elsewhere aren't listed in the database.</b>

><b>\**there is one, but it was incomplete and currently down right now.</b>

<img src='Images/metal-archives homepage.jpg'>

## Project Goal

##### QUESTIONS:
<ol type="1">
  <li><b>Which genre type seems to dominate the metal playing field?</b>
      <ul type="list-style-type:square">
          <li>For the metal genre in general</li>
          <li>For each continent</li>
          <li>Are most genres mixed or pure?</li>
      </ul>
  </li>
      &nbsp;
  <li><b>Which part of the world is the most metal?</b>
      <ul type="list-style-type:square">
          <li>Most metal bands in proportion to population (by country)</li>
      </ul>
      &nbsp;
  </li>
  <li><b>How much has the metal music scene grown?</b>
      <ul type="list-style-type:square">
          <li>Overall</li>
          <li>By Continent</li>
      </ul>
      &nbsp;
  </li>
  <li><b>What is the future of the metal genre?</b>
      <ul type="list-style-type:square">
          <li>Are the number of new bands forming increasing?</li>
          <li>Is the number of currently active bands increasing, decreasing, or plateauing?</li>
          <li>On average, how long do bands stay together?</li>
      </ul>
  </li>
</ol>