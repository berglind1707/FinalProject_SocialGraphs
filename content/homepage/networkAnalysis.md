---
title: "Network Analysis"
weight: 2
header_menu: true
---
The goal for this part is to analyse the network that was created and look into the relationships between
the characters in the Harry Potter world. The data comes from the Harry Potter Wiki.
After capturing the names of the characters, along with their wiki pages and entities such as blood type and gender,
we built a network based on them. We will look at the size of the giant connected component (GCC),
the degree distribution, find the most connected characters, look at which house has the most characters,
look at the gender distribution of each house, draw the network and finally see if the Friendship Paradox
holds for the network.




---

### Harry Potter extended network analysis

![total_network](images/plots_updated/total_network.png)

Red - Gryffindor

Green - Slytherin

Blue - Ravenclaw

Yellow - Huffelpuff

Beige - Characters without houses

The network is quite big, so it is very dense at some places. The biggest node is, unsurprisingly, Harry Potter. The nodes with names are all well-known characters from the Harry Potter universe. Red and green are dominant colors here which is expected too, because Gryffindor and Slytherin were the houses with the highest number of characters, as shown earlier.


![house_plots](images/plots_updated/Total_in_dist.png)

![house_plots](images/plots_updated/Total_out_dist.png)

![house_plots](images/plots_updated/Total_loglog_dist.png)

![house_plots](images/plots_updated/Total_degree_dist.png)




---

#### General House Information

![house_plots](images/plots_updated/gender_dist.png)

![house_plots](images/plots_updated/number_of_characters.png)

![house_plots](images/plots_updated/pure_blood_dist.png)


---
