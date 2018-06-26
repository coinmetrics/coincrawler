## Coincrawler

**Warning**: this is a legacy software which is no longer used by coinmetrics.io. We currently utilize [Haskell](https://github.com/coinmetrics-io/haskell-tools) and [Python](https://github.com/coinmetrics-io/python-tools) tools for data extraction and aggregation.

Coincrawler is a set of programs used for data extraction from blockchains and block explorers. Transaction volume, transaction count, fees and amount of generated coins are computed for each block and stored in the Postgres database. Additionaly, the suite contains utilities for grabbing price and exchange volume data from coinmarketcap.com, and dumping the obtained information to CSV file.

### Prerequisites 

Python 2.7, Postgres database.
Python modules: psycopg2, bs4, python-dateutil, lmdb, requests.

### Supported cryptocurrencies

Coincrawler supports Bitcoin, Bitcoin Cash, Bitcoin Gold, Litecoin, Dash, PIVX, Monero, Dogecoin, Decred, NEM, Ethereum, Ethereum Classic, ZCash, Vertcoin, Verge, Digibyte and, probably, many other currencies based on Bitcoin or Ethereum code.

Data for all cryptocurrencies, except NEM and Decred, is fetched from blockchains via RPC API.

Decred and XEM data is fetched from block explorers https://mainnet.decred.org and http://chain.nem.ninja respectively.

### How to use

Please look at files in the examples folder. Coincrawler is a client-server software: postgres database hosting machine fetches data from servers on which cryptocurrency nodes run. 
