# IP Locator

A single-page web app that tells you **which country and city an IP address belongs to**.
Made for a Data Structures and Algorithms (DSA) Open Ended Lab.

## Features
- Check one or many IPv4 addresses at once
- Shows country, region, city, coordinates and distance from a reference city
- World map with the located IPs
- Rejects private (192.168.x.x, 127.0.0.1) and invalid addresses
- Works fully in the browser, no server needed

## Data structures used
| Feature | Data structure | Complexity |
|---|---|---|
| Repeated lookups | Hash Map (cache) | O(1) |
| Unique IPs | Hash Set | O(1) |
| Recent checks | Queue (last 10) | O(1) |
| Nearest IPs, most checked | Min-Heap | O(log n) per pop |
| Finding an IP in the database | Binary search on sorted IP blocks | O(log n) |
| Group by country | Hash Map of lists | O(1) per IP |

## How to use
Open the page, paste IP addresses (separated by space, comma or new line) and press **Locate**.
Press **Try examples** for a quick demo.

## Limitations
- IPv4 only
- Country is reliable, city is approximate
- A web page cannot read your own IP. Search "what is my IP" and paste it.

## Data
IP location data by [DB-IP.com](https://db-ip.com), licensed under CC BY 4.0.
