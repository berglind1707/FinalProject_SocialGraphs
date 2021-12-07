---
title: "Network Analysis"
weight: 2
header_menu: true
---
The goal for this part is to analyse the network that was created and look into the relationships between the characters in the Harry Potter world. The data was collected from [The Harry Potter Wiki API](https://harrypotter.fandom.com/wiki/Main_Page). From the Wiki page, we managed to collect the names of the characters attending Hogwarts by looking at the pages of the four houses ([Gryffindor](https://harrypotter.fandom.com/wiki/Gryffindor), [Slytherin](https://harrypotter.fandom.com/wiki/Slytherin), [Ravenclaw](https://harrypotter.fandom.com/wiki/Ravenclaw) and [Hufflepuff](https://harrypotter.fandom.com/wiki/Hufflepuff)). But not all the characters of the Harry Potter world are wizards, so we collected the names of the remaining characters from [this API](https://hp-api.herokuapp.com/api/characters). The names were captured using regular expressions on the text from the HTTP response. 

After capturing the names of the characters, along with their wiki pages and entities such as blood type and gender, we built a network based on them. Here we will look at the size of the giant connected component (GCC), its degree distribution, find the most connected characters, look at which house has the most characters, examine the gender distribution of each house, draw the network and finally see if the Friendship Paradox holds for the network.




---

### Harry Potter extended network analysis

![total_network](images/plots_updated/total_network.png)

Red - Gryffindor

Green - Slytherin

Blue - Ravenclaw

Yellow - Hufflepuff

Beige - Characters without houses

The network is quite big, so it is very dense at some places. The biggest node is, unsurprisingly, Harry Potter. The nodes with names are all well-known characters from the Harry Potter universe. Red and green are dominant colors here which is expected too, because Gryffindor and Slytherin were the houses with the highest number of characters, as shown earlier.

### Distribution
Let's now take a look at the degree distributions of the network. We will look at plots visualising the in- and out-degree distribution, along with the distribution on a log-log scale and the degree distribution of the undirected giant connected component.


![house_plots](images/plots_updated/Total_in_dist.png)

![house_plots](images/plots_updated/Total_out_dist.png)

![house_plots](images/plots_updated/Total_loglog_dist.png)

![house_plots](images/plots_updated/Total_degree_dist.png)

As expected, the vast majority of the nodes has a degree close to 0, while very few nodes have a high degree. The x-axis is cut off at 60, for better visualisation, although some nodes have a lot higher degree.


### Sentiment of communities and characters

![total_network](images/comm_sent/char_dist_TotalNetwork.png)
![total_network](images/comm_sent/comm_dist_TotalNetwork.png)


Minerva McGonagall - Sirius Black - Lily J. Potter

| Word      | tf-idf score |
|-----------|--------------|
| jacob     | 6.76         |
| coltrane  | 6.30         |
| hogwarts  | 6.01         |
| invention | 5.93         |
| year      | 5.78         |


---


## General House Information

![house_plots](images/plots_updated/number_of_characters.png)
It is not surprising that Gryffindor has the most characters, followed by Slytherin, as those are the main houses in the books. Ravenclaw and Hufflepuff play a smaller role in the series, and have almost the same number of characters. Then there are some characters that are not members of any houses. Those are the characters that were not attending the Hogwarts school, or characters attending Hogwarts, but whose house is unknown.

![house_plots](images/plots_updated/gender_dist.png)

The gender distribution is quite even for all of the houses, except for Slytherin which is quite male-dominant. For characters without a house, the males are dominant characters, that might be because many of those characters are trolls and other creatures.
![house_plots](images/pure_blood_dist.png)

The one house that stands out here is Slytherin. When digging deeper, this is no surprise. On the website *Pottermore*, J.K. Rowling wrote:

> "The term 'pure-blood' refers to a family or individual without Muggle (non-magic) blood. The concept is generally associated with Salazar Slytherin, one of the four founders of Hogwarts School of Witchcraft and Wizardry, whose aversion to teaching anybody of Muggle parentage eventually led to a breach with his three fellow founders, and his resignation from the school."

This shows that Slytherin has much pride in keeping their purity. The diminshing number of pure-bloods over the years led to inbreeding within the families that wanted to keep the purity in the family. The Malfoy family was one of those who wanted to stick to that, but eventually allowed marrying half-bloods.

---