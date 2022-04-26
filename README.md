DATASETS (CONTAINS INFO ON FILE NAME, SHAPE, ATTRIBUTE INFO)
~~~~~~~~~
DIM_CRYPTO_DATA.csv 

SHAPE:  (15, 4)

- Contains data on cryptocurrency and if it's mineable
+----+------+--------+-----------------+---------------+
|    |   Id | Code   | Currency_Name   |   Is_Mineable |
+====+======+========+=================+===============+
|  0 |    1 | ADA    | Cardano         |             0 |
+----+------+--------+-----------------+---------------+
|  1 |    2 | BTC    | Bitcoin         |             1 |
+----+------+--------+-----------------+---------------+
|  2 |    3 | DASH   | DASH            |             1 |
+----+------+--------+-----------------+---------------+
|  3 |    4 | DOGE   | Dogecoin        |             1 |
+----+------+--------+-----------------+---------------+
|  4 |    5 | EOS    | EOS             |             0 |
+----+------+--------+-----------------+---------------+
|  5 |    6 | ETH    | Ethereum        |             1 |
+----+------+--------+-----------------+---------------+
|  6 |    7 | LTC    | Litecoin        |             1 |
+----+------+--------+-----------------+---------------+
|  7 |    8 | MIOTA  | IOTA            |             0 |
+----+------+--------+-----------------+---------------+
|  8 |    9 | NEO    | NEO             |             0 |
+----+------+--------+-----------------+---------------+
|  9 |   10 | TRX    | TRON            |             0 |
+----+------+--------+-----------------+---------------+
| 10 |   11 | USDT   | Tether          |             0 |
+----+------+--------+-----------------+---------------+
| 11 |   12 | XEM    | NEM             |             0 |
+----+------+--------+-----------------+---------------+
| 12 |   13 | XLM    | Stellar         |             0 |
+----+------+--------+-----------------+---------------+
| 13 |   14 | XMR    | Monero          |             1 |
+----+------+--------+-----------------+---------------+
| 14 |   15 | XRP    | Ripple          |             0 |
+----+------+--------+-----------------+---------------+

ATTRIBUTES: 

ID: ID assigned to cryptocurrency ; numeric
CODE: Acronym assigned to crypto ; string
CURRENCY_NAME: full name of crypto ; string
IS_MINEABLE: whether not a person can mine the specific crpyto ; numeric


DIM_GPU_PROD.csv

SHAPE:  (2054, 6)

- Contains info on different GPUs that were made
+----+------+--------------------------+--------------+--------------------+-------------------+---------------+
|    |   Id | Processor_Manufacturer   | Processor    | GPU_Manufacturer   |   Memory_Capacity | Memory_Type   |
+====+======+==========================+==============+====================+===================+===============+
|  0 |    1 | AMD                      | C420         | Matrox             |             2     | GDDR5         |
+----+------+--------------------------+--------------+--------------------+-------------------+---------------+
|  1 |    2 | AMD                      | C680         | Matrox             |             2     | GDDR5         |
+----+------+--------------------------+--------------+--------------------+-------------------+---------------+
|  2 |    3 | AMD                      | C680         | Matrox             |             4     | GDDR5         |
+----+------+--------------------------+--------------+--------------------+-------------------+---------------+
|  3 |    4 | AMD                      | C900         | Matrox             |             4     | GDDR5         |
+----+------+--------------------------+--------------+--------------------+-------------------+---------------+
|  4 |    5 | AMD                      | FireGL V3300 | AMD                |             0.125 | GDDR2         |
+----+------+--------------------------+--------------+--------------------+-------------------+---------------+
(Contains a lot more rows, but shortened for informational purposes)

ATTRIBUTES: 
PROCESSOR_MANUFACTURER: Maker of processor ; string
PROCESSOR: Processor name of GPU ; string
GPU_MANUFACTURER: Maker of GPU ; string
MEMORY_CAPACITY: Memory capacity of the GPU in GB ; numeric
MEMORY_TYPE: What kind of memory the GPU holds ; string


FACT_GPU_PRICE.csv 

(997156, 6)

- Contains information on the price of a GPU 

+----+----------+-------------+------------+--------------+-------------+------------------+
|    |   ProdId |      TimeId |   RegionId |   MerchantId |   Price_USD |   Price_Original |
+====+==========+=============+============+==============+=============+==================+
|  0 |        1 | 2.01409e+07 |          4 |           32 |     601.738 |           463.9  |
+----+----------+-------------+------------+--------------+-------------+------------------+
|  1 |        1 | 2.01409e+07 |          4 |           32 |     551.885 |           425.87 |
+----+----------+-------------+------------+--------------+-------------+------------------+
|  2 |        1 | 2.01409e+07 |          4 |           32 |     548.099 |           424.53 |
+----+----------+-------------+------------+--------------+-------------+------------------+
|  3 |        1 | 2.01409e+07 |          4 |           32 |     545.094 |           424.53 |
+----+----------+-------------+------------+--------------+-------------+------------------+
|  4 |        1 | 2.01409e+07 |          4 |           32 |     544.674 |           424.53 |
+----+----------+-------------+------------+--------------+-------------+------------------+
(Shortened for informational purposes)

Attributes:
PRODID: Id of product; numeric
TIMEID: Timestamp of sale; Timestamp
REGIONID: ID of Where GPU was sold ; numeric
MERCHANTID: ID of Which place the GPU was sold at ; numeric
PRICE_USD: Sold price of GPU in USD ; numeric
PRICE_ORIGINAL: Original price of GPU in USD ; numeric 


FACT_CRYPTO_RATE.csv 

SHAPE:  (15844, 6)

- Contains information of Cryptocurrency price (Open, close, low, and high)

+----+----------+-------------+----------+----------+----------+----------+
|    |   CodeId |      TimeId |     Open |    Close |     High |      Low |
+====+==========+=============+==========+==========+==========+==========+
|  0 |        1 | 2.01711e+07 | 0.021418 | 0.022628 | 0.023213 | 0.019827 |
+----+----------+-------------+----------+----------+----------+----------+
|  1 |        1 | 2.01711e+07 | 0.022641 | 0.022022 | 0.023849 | 0.02197  |
+----+----------+-------------+----------+----------+----------+----------+
|  2 |        1 | 2.01711e+07 | 0.022054 | 0.020635 | 0.023006 | 0.020635 |
+----+----------+-------------+----------+----------+----------+----------+
|  3 |        1 | 2.01711e+07 | 0.020977 | 0.021881 | 0.023609 | 0.020534 |
+----+----------+-------------+----------+----------+----------+----------+
|  4 |        1 | 2.01711e+07 | 0.021846 | 0.022195 | 0.023347 | 0.021414 |
+----+----------+-------------+----------+----------+----------+----------+
(Shortened for informational purposes)

Attributes:
CODEID: Id of cryptocurrency ; numeric
TIMEID: Timestamp of recorded price ; TIMESTAMP
OPEN: Opening price of the crypto ; numeric
CLOSE: Closing price of the crpyto ; numeric
HIGH: Highest point of Crypto price ; numeric
LOW: Lowestpoint of Crpyto price ; numeric

