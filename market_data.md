# Market Data Table Stucture

A series of simple examples are provided showing how to retrieve different types of market data from `OneTick Cloud`.
Data is stored in databases specific to the venue (equity, future, option or index provider), and commonly consists of the following tables:

* TRD - `Trade Events`
* QTE - `Quote Events`
* MKT - `Market Phase Events`
* DAY - `End of Day Record`
* NBBO - `NBBO Events`
* PRL / PRL_FULL  - `Book Depth Events`
* IND - `Auction Imbalance Events`
* STAT - `Static Reference Data Record`
* TRD_1M - `Trade Bar Retrieval`
* QTE_1M - `Quote Bar Retrieval`

## Symbol Universe

All collected symbols are centrally stored in the `SYMBOL_UNIVERSE` database, with reference information such as Name, Security Type, Currency, MIC, etc,
and importantly which `DB_NAME` and `DB_SYMBOL` stores the historic market data.
The `SYMBOL_UNIVERSE` database is partitioned by Database and Security Type, allowing fast filtering on these terms.
Common Security Types include:  `Equity`, `Future`, \`\` Futures Spread\`\`, `Option`, `Option Spread`, `Index`, and `ETF`.

```
SELECT * FROM  SYMBOL_UNIVERSE.STAT
WHERE SYMBOL_NAME = 'LSE Equity'
and TIMESTAMP >= '2024-01-03 00:00:00 UTC'
and TIMESTAMP < '2024-01-04 00:00:00 UTC'
LIMIT 5
```

#### Symbol Universe Retrieval Filtered on LSE Equities

| Symbol                      | Timestamp           | SYMBOL_NAME                 | TICK_TYPE   |   OMDSEQ | DB_NAME   | NAME                            | ISIN         | EXCH_SYMBOL   |   TRADING_CODE | MIC   | OPERATING_MIC   | SEC_TYPE   | MKT_SEGMENT   | CURRENCY   | BSYM           |        OID | STRIKE_PRICE   | CONTRACT_SIZE   | DB_SYMBOL   | CFI_CODE   | EXPIRATION_DATE   | CALL_PUT_IND   | PRODUCT_CODE   | STRATEGY_TYPE   | UNDERLYING_SYMBOL   | SIP_SYMBOL   |
|-----------------------------|---------------------|-----------------------------|-------------|----------|-----------|---------------------------------|--------------|---------------|----------------|-------|-----------------|------------|---------------|------------|----------------|------------|----------------|-----------------|-------------|------------|-------------------|----------------|----------------|-----------------|---------------------|--------------|
| SYMBOL_UNIVERSE::LSE Equity | 2024-01-03 04:00:00 | SYMBOL_UNIVERSE::LSE Equity | STAT        |      124 | LSE       | Groupe Parot                    | FR0013204070 | 0A04          |         151949 | XLOM  | XLON            | Equity     | SSX4          | EUR        | 0A04 LN Equity | 1015725922 |                |                 | 0A04        |            |                   |                |                |                 |                     |              |
| SYMBOL_UNIVERSE::LSE Equity | 2024-01-03 04:00:00 | SYMBOL_UNIVERSE::LSE Equity | STAT        |      125 | LSE       | Medacta Group SA                | CH0468525222 | 0A05          |         151987 | XLOM  | XLON            | Equity     | SSX4          | CHF        | 0A05 LN Equity | 1015743877 |                |                 | 0A05        |            |                   |                |                |                 |                     |              |
| SYMBOL_UNIVERSE::LSE Equity | 2024-01-03 04:00:00 | SYMBOL_UNIVERSE::LSE Equity | STAT        |      132 | LSE       | Stadler Rail AG                 | CH0002178181 | 0A0C          |         151996 | XLOM  | XLON            | Equity     | SSX4          | CHF        | 0A0C LN Equity | 1015747442 |                |                 | 0A0C        |            |                   |                |                |                 |                     |              |
| SYMBOL_UNIVERSE::LSE Equity | 2024-01-03 04:00:00 | SYMBOL_UNIVERSE::LSE Equity | STAT        |      133 | LSE       | Societa Editoriale Il Fatto Spa | IT0005353484 | 0A0G          |         152040 | XLOM  | XLON            | Equity     | SSX4          | EUR        | 0A0G LN Equity | 1015758539 |                |                 | 0A0G        |            |                   |                |                |                 |                     |              |
| SYMBOL_UNIVERSE::LSE Equity | 2024-01-03 04:00:00 | SYMBOL_UNIVERSE::LSE Equity | STAT        |      135 | LSE       | Twenty First Century Fox A Inc  | US35137L1052 | 0A0X          |         152064 | XLOM  | XLON            | Equity     | SSX4          | EUR        | 0A0X LN Equity | 1015762601 |                |                 | 0A0X        |            |                   |                |                |                 |                     |              |
```
SELECT NAME, EXCH_SYMBOL, DB_SYMBOL, DB_NAME, CURRENCY, SEC_TYPE FROM SYMBOL_UNIVERSE.STAT
WHERE SYMBOL_NAME LIKE '% Equity'
and CURRENCY = 'GBX'
and NAME LIKE 'Voda%'
and TIMESTAMP >= '2024-01-03 00:00:00 UTC'
and TIMESTAMP < '2024-01-04 00:00:00 UTC'
LIMIT 5
```

#### Symbol Universe Retrieval Filtered on Equity, Currency and Instrument Name

| Symbol   | Timestamp           | DB_NAME        | NAME               | EXCH_SYMBOL   | SEC_TYPE   | CURRENCY   | DB_SYMBOL    |
|----------|---------------------|----------------|--------------------|---------------|------------|------------|--------------|
|          | 2024-01-03 00:00:00 | EU_COMP        | Vodafone Group plc | VOD           | Equity     | GBX        | GB00BH4HKS39 |
|          | 2024-01-03 00:00:00 | EU_COMP_SAMPLE | Vodafone Group plc | VOD           | Equity     | GBX        | GB00BH4HKS39 |
|          | 2024-01-03 02:00:00 | CBOE_APA       | Vodafone Group plc | VODl          | Equity     | GBX        | VODl         |
|          | 2024-01-03 03:00:00 | EQUIDUCT       | Vodafone Group plc | VODl          | Equity     | GBX        | VODl         |
|          | 2024-01-03 04:00:00 | BXE            | Vodafone Group PLC | VODl          | Equity     | GBX        | VODl         |



## Trade Events

Trade events are retrieved by specifying the `TRD` table, along with the specified database, symbol and time range.
Trades are represented with `PRICE`, `SIZE`, and other fields.

```
SELECT * FROM US_COMP_SAMPLE.TRD
WHERE SYMBOL_NAME='AAPL'
and TIMESTAMP >= '2024-01-03 00:00:00 UTC'
and TIMESTAMP < '2024-01-04 00:00:00 UTC'
LIMIT 10
```

#### Trade Retrieval Results

| Symbol               | Timestamp                     |   PRICE |   SIZE | SYMBOL_NAME          | TICK_TYPE   |   OMDSEQ |   TRADE_ID | DELETED_TIME   |   TICK_STATUS | TICKER   | EXCHANGE   | COND   | PARTICIPANT_TIME              | TRF_TIME                      | STOP_STOCK   | SOURCE   | TRF   |   TTE |   CORR |   SEQ_NUM |
|----------------------|-------------------------------|---------|--------|----------------------|-------------|----------|------------|----------------|---------------|----------|------------|--------|-------------------------------|-------------------------------|--------------|----------|-------|-------|--------|-----------|
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:00.218558977 |  185.3  |     33 | US_COMP_SAMPLE::AAPL | TRD         |        0 |      86475 |                |             0 | AAPL     | P          | @FTI   | 2024-01-03 00:00:00.218213653 |                               |              | N        |       |     1 |      0 | 7,564,627 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:00.218560994 |  185.3  |     23 | US_COMP_SAMPLE::AAPL | TRD         |        1 |      86476 |                |             0 | AAPL     | P          | @FTI   | 2024-01-03 00:00:00.218213653 |                               |              | N        |       |     1 |      0 | 7,564,628 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:00.220299709 |  185.31 |    270 | US_COMP_SAMPLE::AAPL | TRD         |        0 |      86477 |                |             0 | AAPL     | P          | @FT    | 2024-01-03 00:00:00.219957729 |                               |              | N        |       |     1 |      0 | 7,564,629 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:00.435767951 |  185.31 |    163 | US_COMP_SAMPLE::AAPL | TRD         |        0 |      86478 |                |             0 | AAPL     | P          | @FT    | 2024-01-03 00:00:00.435425583 |                               |              | N        |       |     1 |      0 | 7,564,642 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:02.601960283 |  185.29 |      6 | US_COMP_SAMPLE::AAPL | TRD         |        0 |      86479 |                |             0 | AAPL     | P          | @FTI   | 2024-01-03 00:00:02.601616588 |                               |              | N        |       |     1 |      0 | 7,564,650 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:02.645347419 |  185.3  |      1 | US_COMP_SAMPLE::AAPL | TRD         |        0 |     525468 |                |             0 | AAPL     | D          | @ TI   | 2024-01-03 00:00:02.419488    | 2024-01-03 00:00:02.645322626 |              | N        | Q     |     0 |      0 | 7,564,651 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:03.039775401 |  185.31 |      1 | US_COMP_SAMPLE::AAPL | TRD         |        0 |      86480 |                |             0 | AAPL     | P          | @FTI   | 2024-01-03 00:00:03.039432526 |                               |              | N        |       |     1 |      0 | 7,564,652 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:03.208757357 |  185.3  |      1 | US_COMP_SAMPLE::AAPL | TRD         |        0 |     525469 |                |             0 | AAPL     | D          | @ TI   | 2024-01-03 00:00:02.920041    | 2024-01-03 00:00:03.208730105 |              | N        | Q     |     0 |      0 | 7,564,653 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:09.805361739 |  185.3  |      1 | US_COMP_SAMPLE::AAPL | TRD         |        0 |     525470 |                |             0 | AAPL     | D          | @ TI   | 2024-01-03 00:00:09.600971    | 2024-01-03 00:00:09.805332604 |              | N        | Q     |     0 |      0 | 7,564,663 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:10.888731406 |  185.31 |      3 | US_COMP_SAMPLE::AAPL | TRD         |        0 |      86481 |                |             0 | AAPL     | P          | @ TI   | 2024-01-03 00:00:10.888387762 |                               |              | N        |       |     0 |      0 | 7,564,664 |



## Quote Events

Quote events are retrieved by specifying the `QTE` table, along with the specified database, symbol and time range.
Quotes are represented with `BID_PRICE`, `BID_SIZE`, `ASK_PRICE`, `ASK_SIZE` and other fields.

```
SELECT * FROM US_COMP_SAMPLE.QTE
WHERE SYMBOL_NAME='AAPL'
and TIMESTAMP >= '2024-01-03 00:00:00 UTC'
and TIMESTAMP < '2024-01-04 00:00:00 UTC'
LIMIT 10
```

#### Quote Retrieval Results

| Symbol               | Timestamp                     |   BID_PRICE |   ASK_PRICE |   BID_SIZE |   ASK_SIZE | SYMBOL_NAME          | TICK_TYPE   |   OMDSEQ | DELETED_TIME   |   TICK_STATUS | TICKER   | EXCHANGE   | COND   | PARTICIPANT_TIME              | SOURCE   | CORR   |     SEQ_NUM | FINRA_ADF_TIME   |   NBBO_IND | FINRA_BBO_IND   | FINRA_ADF_MPID_IND   | RPI   |   RESTRICTION_IND | LULD_BBO_IND   | SIP_MSG_ID   | NBBO_LULD_IND   | FINRA_ADF_IND   | SECURITY_STATUS_IND   |
|----------------------|-------------------------------|-------------|-------------|------------|------------|----------------------|-------------|----------|----------------|---------------|----------|------------|--------|-------------------------------|----------|--------|-------------|------------------|------------|-----------------|----------------------|-------|-------------------|----------------|--------------|-----------------|-----------------|-----------------------|
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:00.220300383 |      185.29 |      185.31 |          3 |          6 | US_COMP_SAMPLE::AAPL | QTE         |        0 |                |             0 | AAPL     | P          | R      | 2024-01-03 00:00:00.219957729 | N        |        | 110,384,045 |                  |          4 |                 |                      |       |                 0 |                |              |                 |                 |                       |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:00.435768604 |      185.29 |      185.31 |          3 |          4 | US_COMP_SAMPLE::AAPL | QTE         |        0 |                |             0 | AAPL     | P          | R      | 2024-01-03 00:00:00.435425583 | N        |        | 110,384,063 |                  |          4 |                 |                      |       |                 0 |                |              |                 |                 |                       |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:00.494951248 |      183.1  |      185.64 |          1 |          4 | US_COMP_SAMPLE::AAPL | QTE         |        0 |                |             0 | AAPL     | Z          | R      | 2024-01-03 00:00:00.494771    | N        |        | 110,384,082 |                  |          0 |                 |                      |       |                 0 |                |              |                 |                 |                       |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:02.601960874 |      185.29 |      185.31 |          3 |          4 | US_COMP_SAMPLE::AAPL | QTE         |        0 |                |             0 | AAPL     | P          | R      | 2024-01-03 00:00:02.601616588 | N        |        | 110,384,093 |                  |          0 |                 |                      |       |                 0 |                |              |                 |                 |                       |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:03.039776531 |      185.29 |      185.31 |          3 |          4 | US_COMP_SAMPLE::AAPL | QTE         |        0 |                |             0 | AAPL     | P          | R      | 2024-01-03 00:00:03.039432526 | N        |        | 110,384,095 |                  |          0 |                 |                      |       |                 0 |                |              |                 |                 |                       |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:10.888732704 |      185.29 |      185.31 |          3 |          4 | US_COMP_SAMPLE::AAPL | QTE         |        0 |                |             0 | AAPL     | P          | R      | 2024-01-03 00:00:10.888387762 | N        |        | 110,384,113 |                  |          0 |                 |                      |       |                 0 |                |              |                 |                 |                       |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:11.286962866 |      182.99 |      185.62 |          1 |          2 | US_COMP_SAMPLE::AAPL | QTE         |        0 |                |             0 | AAPL     | U          | R      | 2024-01-03 00:00:11.286771307 | N        |        | 110,384,114 |                  |          0 |                 |                      |       |                 0 |                |              |                 |                 |                       |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:13.149205540 |      185.29 |      185.31 |          3 |          3 | US_COMP_SAMPLE::AAPL | QTE         |        0 |                |             0 | AAPL     | P          | R      | 2024-01-03 00:00:13.148859752 | N        |        | 110,384,117 |                  |          4 |                 |                      |       |                 0 |                |              |                 |                 |                       |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:13.149701425 |      185.29 |      185.33 |          3 |          1 | US_COMP_SAMPLE::AAPL | QTE         |        1 |                |             0 | AAPL     | P          | R      | 2024-01-03 00:00:13.149359783 | N        |        | 110,384,118 |                  |          4 |                 |                      |       |                 0 |                |              |                 |                 |                       |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:15.996461820 |      185.01 |      185.39 |          2 |          1 | US_COMP_SAMPLE::AAPL | QTE         |        0 |                |             0 | AAPL     | K          | R      | 2024-01-03 00:00:15.996258    | N        |        | 110,384,125 |                  |          0 |                 |                      |       |                 0 |                |              |                 |                 |                       |



## Market Phase Events

Market Phase events are retrieved by specifying the `MKT` table, along with the specified database, symbol and time range.  This table is only available for a subset of databases.
Phases are represented with `OMD_STATUS` and other fields.

`OMD_STATUS` has the following enumeration.

> * “A” - Auction
> * “B” - Break / Pause
> * “C” - Closing auction
> * “D” - Delisted / Pending deletion
> * “H” - Halted
> * “I” - Scheduled intraday auction
> * “M” - Mandatory quoting period
> * “N” - New instrument / Pre-listing
> * “O” - Opening auction
> * “P” - Pre-market
> * “Q” - Indicative quoting period
> * “R” - Off-book trade reporting
> * “S” - Suspended
> * “T” - Continuous trading
> * “U” - Unscheduled auction
> * “c” - Closed
> * “i” - IPO / Public offering auction
> * “n” - No market phase / Unspecified
> * “o” - Order management
> * “p” - Post-market
> * “t” - Trading at last price
```
SELECT * FROM LSE_SAMPLE.MKT
WHERE SYMBOL_NAME='VOD'
and TIMESTAMP >= '2024-01-03 00:00:00 UTC'
and TIMESTAMP < '2024-01-04 00:00:00 UTC'
LIMIT 10
```

#### Market Phase Retrieval Results

| Symbol          | Timestamp               | SYMBOL_NAME     | TICK_TYPE   | MKT_PHASE   | QUOTE_BOOK_STATUS   | OFF_BOOK_STATUS   | OMD_STATUS   |   OMDSEQ |
|-----------------|-------------------------|-----------------|-------------|-------------|---------------------|-------------------|--------------|----------|
| LSE_SAMPLE::VOD | 2024-01-03 07:15:00.037 | LSE_SAMPLE::VOD | MKT         |             |                     | T                 | R            |       77 |
| LSE_SAMPLE::VOD | 2024-01-03 07:50:00.067 | LSE_SAMPLE::VOD | MKT         | a           |                     | T                 | O            |      134 |
| LSE_SAMPLE::VOD | 2024-01-03 08:00:06.226 | LSE_SAMPLE::VOD | MKT         | T           |                     | T                 | T            |       26 |
| LSE_SAMPLE::VOD | 2024-01-03 16:30:00.107 | LSE_SAMPLE::VOD | MKT         | d           |                     | T                 | C            |       91 |
| LSE_SAMPLE::VOD | 2024-01-03 16:35:07.331 | LSE_SAMPLE::VOD | MKT         | u           |                     | T                 | t            |        0 |
| LSE_SAMPLE::VOD | 2024-01-03 16:40:00.025 | LSE_SAMPLE::VOD | MKT         | b           |                     | T                 | p            |       34 |
| LSE_SAMPLE::VOD | 2024-01-03 17:15:00.080 | LSE_SAMPLE::VOD | MKT         | x           |                     | T                 | p            |      106 |
| LSE_SAMPLE::VOD | 2024-01-03 17:30:00.041 | LSE_SAMPLE::VOD | MKT         | c           |                     | T                 | c            |       34 |
| LSE_SAMPLE::VOD | 2024-01-03 17:30:00.041 | LSE_SAMPLE::VOD | MKT         | c           |                     | c                 | c            |        0 |



## End of Day Record

End of Day Records are retrieved by specifying the `DAY` table, along with the specified database, symbol and time range.  This table is only available for a subset of databases.

```
SELECT * FROM LSE_SAMPLE.DAY
WHERE SYMBOL_NAME='VOD'
and TIMESTAMP >= '2024-01-03 00:00:00 UTC'
and TIMESTAMP < '2024-01-04 00:00:00 UTC'
LIMIT 10
```

#### Day Retrieval Results

| Symbol          | Timestamp           | SYMBOL_NAME     | TICK_TYPE   |   OMDSEQ |   HIGH |   LOW |     VOLUME |   OPEN |   CLOSE |   ON_BOOK_VOLUME |   OFF_BOOK_VOLUME |
|-----------------|---------------------|-----------------|-------------|----------|--------|-------|------------|--------|---------|------------------|-------------------|
| LSE_SAMPLE::VOD | 2024-01-03 19:30:00 | LSE_SAMPLE::VOD | DAY         |        0 |  70.75 | 69.38 | 90,161,664 |     70 |   69.51 |       31,819,135 |        58,342,529 |



## NBBO Events

National Best Bid & Offer (NBBO) events are retrieved by specifying the `NBBO` table, along with the specified database, symbol and time range.
This table is only available for databases that host composite exchanges, and has a similar schema to `QTE` tables, with `BID_PRICE`, `ASK_PRICE`, `BID_SIZE`, `ASK_SIZE`.
Additionally it also includes `BID_EXCHANGE` and `ASK_EXCHANGE`.

```
SELECT * FROM US_COMP_SAMPLE.NBBO
WHERE SYMBOL_NAME='AAPL'
and TIMESTAMP >= '2024-01-03 00:00:00 UTC'
and TIMESTAMP < '2024-01-04 00:00:00 UTC'
LIMIT 10
```

#### NBBO Retrieval Results

| Symbol               | Timestamp                     |   BID_PRICE |   ASK_PRICE |   BID_SIZE |   ASK_SIZE | SYMBOL_NAME          | TICK_TYPE   |   OMDSEQ |   BID_SIZE_TOTAL | BID_EXCHANGE   |   ASK_SIZE_TOTAL | ASK_EXCHANGE   |   IS_PRE_OPEN |
|----------------------|-------------------------------|-------------|-------------|------------|------------|----------------------|-------------|----------|------------------|----------------|------------------|----------------|---------------|
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:00.220300383 |      185.29 |      185.31 |          3 |          6 | US_COMP_SAMPLE::AAPL | NBBO        |        0 |                3 | P              |                6 | P              |             0 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:00.435768604 |      185.29 |      185.31 |          3 |          4 | US_COMP_SAMPLE::AAPL | NBBO        |        0 |                3 | P              |                4 | P              |             0 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:13.149205540 |      185.29 |      185.31 |          3 |          3 | US_COMP_SAMPLE::AAPL | NBBO        |        0 |                3 | P              |                3 | P              |             0 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:13.149701425 |      185.29 |      185.33 |          3 |          1 | US_COMP_SAMPLE::AAPL | NBBO        |        1 |                3 | P              |                1 | P              |             0 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:22.472943947 |      185.3  |      185.33 |          1 |          1 | US_COMP_SAMPLE::AAPL | NBBO        |        0 |                1 | P              |                1 | P              |             0 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:27.860325809 |      185.3  |      185.34 |          1 |          1 | US_COMP_SAMPLE::AAPL | NBBO        |        0 |                1 | P              |                1 | P              |             0 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:29.781038128 |      185.3  |      185.33 |          1 |          1 | US_COMP_SAMPLE::AAPL | NBBO        |        0 |                1 | P              |                1 | P              |             0 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:30.124465063 |      185.29 |      185.33 |          4 |          1 | US_COMP_SAMPLE::AAPL | NBBO        |        0 |                4 | P              |                1 | P              |             0 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:00:57.937608932 |      185.29 |      185.33 |          3 |          1 | US_COMP_SAMPLE::AAPL | NBBO        |        0 |                3 | P              |                1 | P              |             0 |
| US_COMP_SAMPLE::AAPL | 2024-01-03 00:01:08.332968256 |      185.29 |      185.34 |          3 |          1 | US_COMP_SAMPLE::AAPL | NBBO        |        0 |                3 | P              |                1 | P              |             0 |



## Book Depth Events

Book depth events are retrieved by specifying either the `PRL` or `PRL_FULL` table, depending on whether Market by Level (MBL) or Market by Order (MBO) data is available.
Typically book depth data is analysed using orderbook processing.

```
SELECT * FROM LSE_SAMPLE.PRL_FULL
WHERE SYMBOL_NAME='VOD'
and TIMESTAMP >= '2024-01-03 00:00:00 UTC'
and TIMESTAMP < '2024-01-04 00:00:00 UTC'
LIMIT 10
```

#### Book Depth Event Retrieval Results

| Symbol          | Timestamp               |   PRICE |   SIZE | SYMBOL_NAME     | TICK_TYPE   |   OMDSEQ | DELETED_TIME   |   TICK_STATUS |   BUY_SELL_FLAG | UPDATE_TYPE   |           ORDER_ID | PART_ID   | ORDER_TYPE   | RECORD_TYPE   |
|-----------------|-------------------------|---------|--------|-----------------|-------------|----------|----------------|---------------|-----------------|---------------|--------------------|-----------|--------------|---------------|
| LSE_SAMPLE::VOD | 2024-01-03 05:00:07.876 |    0    |      0 | LSE_SAMPLE::VOD | PRL_FULL    |        0 |                |             0 |               0 |               |                    |           |              | Z             |
| LSE_SAMPLE::VOD | 2024-01-03 05:00:07.876 |   69    |    600 | LSE_SAMPLE::VOD | PRL_FULL    |        0 |                |             0 |               0 | A             | 233244094926020495 |           | L            | R             |
| LSE_SAMPLE::VOD | 2024-01-03 05:00:07.876 |   69    |  5,800 | LSE_SAMPLE::VOD | PRL_FULL    |        1 |                |             0 |               0 | A             | 233244094926209592 |           | L            | R             |
| LSE_SAMPLE::VOD | 2024-01-03 05:00:07.876 |   67.2  | 50,000 | LSE_SAMPLE::VOD | PRL_FULL    |        2 |                |             0 |               0 | A             | 232452446553925487 |           | L            | R             |
| LSE_SAMPLE::VOD | 2024-01-03 05:00:07.876 |   67    | 10,000 | LSE_SAMPLE::VOD | PRL_FULL    |        3 |                |             0 |               0 | A             | 233244094925636785 |           | L            | R             |
| LSE_SAMPLE::VOD | 2024-01-03 05:00:07.876 |   66.94 |  7,300 | LSE_SAMPLE::VOD | PRL_FULL    |        4 |                |             0 |               0 | A             | 233244094925636407 |           | L            | R             |
| LSE_SAMPLE::VOD | 2024-01-03 05:00:07.876 |   66.66 | 20,000 | LSE_SAMPLE::VOD | PRL_FULL    |        5 |                |             0 |               0 | A             | 233244094925845524 |           | L            | R             |
| LSE_SAMPLE::VOD | 2024-01-03 05:00:07.876 |   66.34 |  7,360 | LSE_SAMPLE::VOD | PRL_FULL    |        6 |                |             0 |               0 | A             | 233244094925636400 |           | L            | R             |
| LSE_SAMPLE::VOD | 2024-01-03 05:00:07.876 |   66    |  3,000 | LSE_SAMPLE::VOD | PRL_FULL    |        7 |                |             0 |               0 | A             | 233244094925636417 |           | L            | R             |
| LSE_SAMPLE::VOD | 2024-01-03 05:00:07.876 |   65    | 70,000 | LSE_SAMPLE::VOD | PRL_FULL    |        8 |                |             0 |               0 | A             | 233244094925636406 |           | L            | R             |



## Auction Imbalance Events

Auction Imbalance events are retrieved by specifying the `IND` table, , along with the specified database, symbol and time range.
Events are represented with `PRICE`, `SIZE`, `IMB_SIDE`, `IMB_VOLUME` and other fields.

```
SELECT * FROM LSE_SAMPLE.IND
WHERE SYMBOL_NAME='VOD'
and TIMESTAMP >= '2024-01-03 00:00:00 UTC'
and TIMESTAMP < '2024-01-04 00:00:00 UTC'
LIMIT 10
```

#### Auction Imbalance Event Retrieval Results

| Symbol          | Timestamp               |   PRICE |   SIZE | SYMBOL_NAME     | TICK_TYPE   |   OMDSEQ | EXCH_TIME                     | IMB_SIDE   |   IMB_VOLUME | AUCTION_TYPE   |
|-----------------|-------------------------|---------|--------|-----------------|-------------|----------|-------------------------------|------------|--------------|----------------|
| LSE_SAMPLE::VOD | 2024-01-03 07:50:00.075 |   69    |  6,000 | LSE_SAMPLE::VOD | IND         |       28 | 2024-01-03 07:50:00.074938266 | B          |        2,900 | O              |
| LSE_SAMPLE::VOD | 2024-01-03 07:50:00.076 |   69    |  6,880 | LSE_SAMPLE::VOD | IND         |        5 | 2024-01-03 07:50:00.075324726 | B          |        2,020 | O              |
| LSE_SAMPLE::VOD | 2024-01-03 07:50:00.085 |   69    |  7,370 | LSE_SAMPLE::VOD | IND         |        8 | 2024-01-03 07:50:00.085221086 | B          |        1,530 | O              |
| LSE_SAMPLE::VOD | 2024-01-03 07:50:00.088 |   69    |  8,870 | LSE_SAMPLE::VOD | IND         |        1 | 2024-01-03 07:50:00.087546226 | B          |           30 | O              |
| LSE_SAMPLE::VOD | 2024-01-03 07:50:00.090 |   68.28 |  9,505 | LSE_SAMPLE::VOD | IND         |        8 | 2024-01-03 07:50:00.089537586 | B          |        1,945 | O              |
| LSE_SAMPLE::VOD | 2024-01-03 07:50:00.102 |   68.28 |  9,847 | LSE_SAMPLE::VOD | IND         |        1 | 2024-01-03 07:50:00.101007326 | B          |        1,603 | O              |
| LSE_SAMPLE::VOD | 2024-01-03 07:50:00.116 |   68.28 | 10,006 | LSE_SAMPLE::VOD | IND         |        0 | 2024-01-03 07:50:00.116153726 | B          |        1,444 | O              |
| LSE_SAMPLE::VOD | 2024-01-03 07:50:00.459 |   68.28 | 10,006 | LSE_SAMPLE::VOD | IND         |        1 | 2024-01-03 07:50:00.458532226 | B          |        1,534 | O              |
| LSE_SAMPLE::VOD | 2024-01-03 07:50:00.476 |   68.28 | 10,006 | LSE_SAMPLE::VOD | IND         |        1 | 2024-01-03 07:50:00.475473766 | B          |        1,634 | O              |
| LSE_SAMPLE::VOD | 2024-01-03 07:50:00.482 |   68.28 | 10,006 | LSE_SAMPLE::VOD | IND         |        3 | 2024-01-03 07:50:00.482214626 | B          |        2,234 | O              |



## Static Reference Data Record

The Symbol Universe database holds a standardized schema across all collected venues.  Additional fields may be available by querying the `STAT` table in a specific database.

```
SELECT * FROM LSE_SAMPLE.STAT
WHERE SYMBOL_NAME='VOD'
and TIMESTAMP >= '2024-01-03 00:00:00 UTC'
and TIMESTAMP < '2024-01-04 00:00:00 UTC'
LIMIT 10
```

#### Static Reference Record Retrieval Results

| Symbol          | Timestamp           | SYMBOL_NAME     | TICK_TYPE   |   OMDSEQ | NAME               | ISIN         | SEDOL   | EXCH_SYMBOL   |   TRADING_CODE | MIC   | OPERATING_MIC   | SEC_TYPE   | MKT_SEGMENT   | MKT_SECTOR   | COUNTRY_REG   | CURRENCY   |   LOT_SIZE |   EXCH_MKT_SIZE |
|-----------------|---------------------|-----------------|-------------|----------|--------------------|--------------|---------|---------------|----------------|-------|-----------------|------------|---------------|--------------|---------------|------------|------------|-----------------|
| LSE_SAMPLE::VOD | 2024-01-03 04:00:00 | LSE_SAMPLE::VOD | STAT        |   24,595 | Vodafone Group plc | GB00BH4HKS39 | BH4HKS3 | VOD           |         133215 | XLON  | XLON            | Equity     | SET1          | FE10         | GB            | GBX        |          1 |          30,000 |
| LSE_SAMPLE::VOD | 2024-01-03 04:00:00 | LSE_SAMPLE::VOD | STAT        |   50,834 | Vodafone Group plc | GB00BH4HKS39 | BH4HKS3 | VOD           |         133215 | XLON  | XLON            | Equity     | SET1          | FE10         | GB            | GBX        |          1 |          30,000 |
| LSE_SAMPLE::VOD | 2024-01-03 04:00:00 | LSE_SAMPLE::VOD | STAT        |   77,076 | Vodafone Group plc | GB00BH4HKS39 | BH4HKS3 | VOD           |         133215 | XLON  | XLON            | Equity     | SET1          | FE10         | GB            | GBX        |          1 |          30,000 |



## Trade Bar Retrieval

Pre-calculated 1 minute Trade bars are retrieved by specifying the `TRD_1M` table, along with the specified bar database, symbol and time range.
Trade Bars are represented with fields:
`FIRST_TIME`, `FIRST`, `FIRST_SIZE`, `HIGH_TIME`, `HIGH`, `HIGH_SIZE`, `LOW_TIME`,
`LOW`, `LOW_SIZE`, `LAST_TIME`, `LAST`, `LAST_SIZE`, `VWAP`, `TWAP`, `VOLUME`,
`TRADE_TICK_COUNT`, `TRADE_CURRENCY`

```
SELECT * FROM LSE_SAMPLE_BARS.TRD_1M
WHERE SYMBOL_NAME='VOD'
and TIMESTAMP >= '2024-01-03 00:00:00 UTC'
and TIMESTAMP < '2024-01-04 00:00:00 UTC'
LIMIT 10
```

#### 1 Minute Trade Bar Retrieval Results

| Symbol               | Timestamp           | SYMBOL_NAME          | TICK_TYPE   |   OMDSEQ | CLOUD_DB   | TRADE_CURRENCY   | FIRST_TIME              |   FIRST |   FIRST_SIZE | HIGH_TIME               |   HIGH |   HIGH_SIZE | LOW_TIME                |   LOW |   LOW_SIZE | LAST_TIME               |   LAST |   LAST_SIZE |    VWAP |    TWAP |   VOLUME |   TRADE_TICK_COUNT |
|----------------------|---------------------|----------------------|-------------|----------|------------|------------------|-------------------------|---------|--------------|-------------------------|--------|-------------|-------------------------|-------|------------|-------------------------|--------|-------------|---------|---------|----------|--------------------|
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:01:00 | LSE_SAMPLE_BARS::VOD | TRD_1M      |        0 | LSE        | GBX              | 2024-01-03 08:00:06.232 |   70    |      184,613 | 2024-01-03 08:00:39.921 |  70.41 |       5,700 | 2024-01-03 08:00:06.232 | 70    |    184,613 | 2024-01-03 08:00:51.881 |  70.36 |       4,742 | 70.0738 | 70.2289 |  238,528 |                 23 |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:02:00 | LSE_SAMPLE_BARS::VOD | TRD_1M      |        0 | LSE        | GBX              | 2024-01-03 08:01:53.833 |   70.45 |        5,657 | 2024-01-03 08:01:55.576 |  70.57 |       2,039 | 2024-01-03 08:01:53.833 | 70.45 |      5,657 | 2024-01-03 08:01:57.450 |  70.5  |       6,150 | 70.4932 | 70.4996 |  150,253 |                 20 |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:03:00 | LSE_SAMPLE_BARS::VOD | TRD_1M      |        0 | LSE        | GBX              | 2024-01-03 08:02:04.030 |   70.51 |          327 | 2024-01-03 08:02:34.619 |  70.52 |       5,459 | 2024-01-03 08:02:44.016 | 70.44 |      5,760 | 2024-01-03 08:02:44.016 |  70.44 |       5,760 | 70.4685 | 70.474  |   32,040 |                 18 |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:04:00 | LSE_SAMPLE_BARS::VOD | TRD_1M      |        0 | LSE        | GBX              | 2024-01-03 08:03:10.598 |   70.43 |        2,850 | 2024-01-03 08:03:45.045 |  70.44 |      17,124 | 2024-01-03 08:03:55.985 | 70.41 |      5,000 | 2024-01-03 08:03:55.985 |  70.41 |       5,000 | 70.4329 | 70.4306 |   24,974 |                  3 |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:05:00 | LSE_SAMPLE_BARS::VOD | TRD_1M      |        0 | LSE        | GBX              | 2024-01-03 08:04:52.586 |   70.51 |        5,093 | 2024-01-03 08:04:52.586 |  70.53 |       9,000 | 2024-01-03 08:04:54.271 | 70.46 |        711 | 2024-01-03 08:04:54.294 |  70.46 |       1,352 | 70.5045 | 70.4723 |   61,472 |                 13 |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:06:00 | LSE_SAMPLE_BARS::VOD | TRD_1M      |        0 | LSE        | GBX              | 2024-01-03 08:05:00.144 |   70.43 |            7 | 2024-01-03 08:05:00.144 |  70.43 |           7 | 2024-01-03 08:05:00.144 | 70.43 |          7 | 2024-01-03 08:05:15.027 |  70.43 |       4,614 | 70.43   | 70.43   |    7,814 |                  5 |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:07:00 | LSE_SAMPLE_BARS::VOD | TRD_1M      |        0 | LSE        | GBX              | 2024-01-03 08:06:00.017 |   70.36 |        1,580 | 2024-01-03 08:06:00.017 |  70.36 |       1,580 | 2024-01-03 08:06:15.026 | 70.24 |        100 | 2024-01-03 08:06:15.026 |  70.24 |       1,440 | 70.3157 | 70.2695 |    4,791 |                  5 |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:08:00 | LSE_SAMPLE_BARS::VOD | TRD_1M      |        0 | LSE        | GBX              | 2024-01-03 08:07:00.027 |   70.27 |          803 | 2024-01-03 08:07:33.169 |  70.42 |       3,729 | 2024-01-03 08:07:00.027 | 70.27 |        803 | 2024-01-03 08:07:33.169 |  70.42 |       3,729 | 70.3988 | 70.3716 |   20,576 |                  8 |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:09:00 | LSE_SAMPLE_BARS::VOD | TRD_1M      |        0 | LSE        | GBX              | 2024-01-03 08:08:35.140 |   70.42 |          711 | 2024-01-03 08:08:58.543 |  70.49 |      11,122 | 2024-01-03 08:08:35.140 | 70.42 |        711 | 2024-01-03 08:08:59.251 |  70.47 |         100 | 70.4583 | 70.4571 |   52,611 |                 13 |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:10:00 | LSE_SAMPLE_BARS::VOD | TRD_1M      |        0 | LSE        | GBX              | 2024-01-03 08:09:00.619 |   70.46 |          100 | 2024-01-03 08:09:05.549 |  70.51 |       1,408 | 2024-01-03 08:09:00.619 | 70.46 |        100 | 2024-01-03 08:09:05.549 |  70.51 |       4,560 | 70.4885 | 70.5058 |   11,583 |                  6 |



## Quote Bar Retrieval

Pre-calculated 1 minute Quote bars are retrieved by specifying the `QTE_1M` table, along with the specified bar database, symbol and time range.
Bars databases have the suffix `_BAR`.
Quote Bars are represented with fields:
`FIRST_BID_TIME`, `FIRST_BID_PRICE`, `FIRST_BID_SIZE`, `FIRST_ASK_TIME`, `FIRST_ASK_PRICE`, `FIRST_ASK_SIZE`,
`HIGH_BID_TIME`, `HIGH_BID`, `HIGH_BID_SIZE`, `ASK_PRICE_AT_HIGH_BID`, `ASK_SIZE_AT_HIGH_BID`,
`LOW_ASK_TIME`, `LOW_ASK`, `LOW_ASK_SIZE`, `BID_PRICE_AT_LOW_ASK`, `BID_SIZE_LOW_ASK`,
`LAST_BID_TIME`, `LAST_BID_PRICE`, `LAST_BID_SIZE`, `LAST_ASK_TIME`, `LAST_ASK_PRICE`, `LAST_ASK_SIZE`,
`MID_TWAP`, `MID_MEDIAN`, `MID_LAST`,
`SPREAD_MIN`, `SPREAD_MAX`, `SPREAD_TWAP`, `SPREAD_MEDIAN`, `SPREAD_LAST`,
`QUOTE_CURRENCY`, `QUOTE_TICK_COUNT`

```
SELECT * FROM LSE_SAMPLE_BARS.QTE_1M
WHERE SYMBOL_NAME='VOD'
and TIMESTAMP >= '2024-01-03 00:00:00 UTC'
and TIMESTAMP < '2024-01-04 00:00:00 UTC'
LIMIT 10
```

#### 1 Minute Quote Bar Retrieval Results

| Symbol               | Timestamp           | SYMBOL_NAME          | TICK_TYPE   |   OMDSEQ | FIRST_BID_TIME          |   FIRST_BID_PRICE |   FIRST_BID_SIZE | FIRST_ASK_TIME          |   FIRST_ASK_PRICE |   FIRST_ASK_SIZE | HIGH_BID_TIME           |   HIGH_BID |   HIGH_BID_SIZE |   ASK_PRICE_AT_HIGH_BID |   ASK_SIZE_AT_HIGH_BID | LOW_ASK_TIME            |   LOW_ASK |   LOW_ASK_SIZE |   BID_PRICE_AT_LOW_ASK |   BID_SIZE_LOW_ASK | LAST_BID_TIME           |   LAST_BID_PRICE |   LAST_BID_SIZE | LAST_ASK_TIME           |   LAST_ASK_PRICE |   LAST_ASK_SIZE |   MID_TWAP |   MID_MEDIAN |   MID_LAST |   SPREAD_MIN |   SPREAD_MAX |   SPREAD_TWAP |   SPREAD_MEDIAN |   SPREAD_LAST | QUOTE_CURRENCY   |   QUOTE_TICK_COUNT | CLOUD_DB   |
|----------------------|---------------------|----------------------|-------------|----------|-------------------------|-------------------|------------------|-------------------------|-------------------|------------------|-------------------------|------------|-----------------|-------------------------|------------------------|-------------------------|-----------|----------------|------------------------|--------------------|-------------------------|------------------|-----------------|-------------------------|------------------|-----------------|------------|--------------|------------|--------------|--------------|---------------|-----------------|---------------|------------------|--------------------|------------|
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:01:00 | LSE_SAMPLE_BARS::VOD | QTE_1M      |        0 | 2024-01-03 08:00:06.226 |             70.25 |            2,809 | 2024-01-03 08:00:06.226 |             69.76 |              100 | 2024-01-03 08:00:39.919 |      70.38 |           4,716 |                   70.41 |                  5,700 | 2024-01-03 08:00:06.226 |     69.76 |            100 |                  70.25 |              2,809 | 2024-01-03 08:00:59.796 |            70.36 |             247 | 2024-01-03 08:00:59.796 |            70.45 |           5,657 |    70.2922 |       70.355 |     70.405 |        -0.49 |         0.41 |     0.1021    |            0.12 |          0.09 | GBX              |                526 | LSE        |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:02:00 | LSE_SAMPLE_BARS::VOD | QTE_1M      |        0 | 2024-01-03 08:01:00.799 |             70.34 |              493 | 2024-01-03 08:01:00.799 |             70.45 |            5,657 | 2024-01-03 08:01:55.577 |      70.54 |             100 |                   70.61 |                    711 | 2024-01-03 08:01:23.004 |     70.44 |          2,160 |                  70.35 |                234 | 2024-01-03 08:01:59.461 |            70.51 |             100 | 2024-01-03 08:01:59.461 |            70.6  |           2,236 |    70.4122 |       70.475 |     70.555 |         0.04 |         0.12 |     0.0974884 |            0.08 |          0.09 | GBX              |                283 | LSE        |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:03:00 | LSE_SAMPLE_BARS::VOD | QTE_1M      |        0 | 2024-01-03 08:02:00.189 |             70.51 |              100 | 2024-01-03 08:02:00.189 |             70.61 |           16,156 | 2024-01-03 08:02:00.190 |      70.52 |             322 |                   70.61 |                  2,084 | 2024-01-03 08:02:42.034 |     70.49 |            711 |                  70.44 |              6,865 | 2024-01-03 08:02:47.656 |            70.41 |           6,814 | 2024-01-03 08:02:47.656 |            70.51 |           5,093 |    70.5214 |       70.535 |     70.46  |         0.01 |         0.13 |     0.0952159 |            0.09 |          0.1  | GBX              |                409 | LSE        |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:04:00 | LSE_SAMPLE_BARS::VOD | QTE_1M      |        0 | 2024-01-03 08:03:00.466 |             70.41 |            6,814 | 2024-01-03 08:03:00.466 |             70.5  |            2,252 | 2024-01-03 08:03:45.045 |      70.44 |          17,124 |                   70.48 |                 13,173 | 2024-01-03 08:03:55.985 |     70.44 |            711 |                  70.36 |              3,904 | 2024-01-03 08:03:57.934 |            70.39 |           1,381 | 2024-01-03 08:03:57.934 |            70.49 |           7,154 |    70.4416 |       70.435 |     70.44  |         0.04 |         0.13 |     0.0972481 |            0.09 |          0.1  | GBX              |                114 | LSE        |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:05:00 | LSE_SAMPLE_BARS::VOD | QTE_1M      |        0 | 2024-01-03 08:04:00.107 |             70.39 |            1,481 | 2024-01-03 08:04:00.107 |             70.49 |            7,154 | 2024-01-03 08:04:52.590 |      70.51 |             100 |                   70.57 |                    711 | 2024-01-03 08:04:00.107 |     70.49 |          7,154 |                  70.39 |              1,481 | 2024-01-03 08:04:59.430 |            70.43 |           2,682 | 2024-01-03 08:04:59.430 |            70.5  |           4,716 |    70.4694 |       70.47  |     70.465 |         0.04 |         0.11 |     0.0789207 |            0.07 |          0.07 | GBX              |                204 | LSE        |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:06:00 | LSE_SAMPLE_BARS::VOD | QTE_1M      |        0 | 2024-01-03 08:05:00.136 |             70.43 |            2,675 | 2024-01-03 08:05:00.136 |             70.5  |            4,716 | 2024-01-03 08:05:00.224 |      70.45 |             711 |                   70.52 |                    711 | 2024-01-03 08:05:15.026 |     70.42 |            711 |                  70.4  |                100 | 2024-01-03 08:05:54.602 |            70.36 |           2,330 | 2024-01-03 08:05:54.602 |            70.42 |           4,440 |    70.4102 |       70.47  |     70.39  |         0.01 |         0.09 |     0.0653059 |            0.07 |          0.06 | GBX              |                 85 | LSE        |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:07:00 | LSE_SAMPLE_BARS::VOD | QTE_1M      |        0 | 2024-01-03 08:06:00.015 |             70.36 |              750 | 2024-01-03 08:06:00.015 |             70.42 |            4,440 | 2024-01-03 08:06:00.015 |      70.36 |             750 |                   70.42 |                  4,440 | 2024-01-03 08:06:28.573 |     70.27 |          2,072 |                  70.21 |             10,000 | 2024-01-03 08:06:54.402 |            70.27 |          14,355 | 2024-01-03 08:06:54.402 |            70.34 |           2,450 |    70.3002 |       70.28  |     70.305 |         0.04 |         0.1  |     0.0747614 |            0.08 |          0.07 | GBX              |                304 | LSE        |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:08:00 | LSE_SAMPLE_BARS::VOD | QTE_1M      |        0 | 2024-01-03 08:07:00.025 |             70.27 |           13,552 | 2024-01-03 08:07:00.025 |             70.34 |            2,450 | 2024-01-03 08:07:33.153 |      70.38 |           2,700 |                   70.42 |                  5,151 | 2024-01-03 08:07:00.025 |     70.32 |            711 |                  70.27 |             13,552 | 2024-01-03 08:07:59.610 |            70.34 |           5,400 | 2024-01-03 08:07:59.610 |            70.41 |           4,716 |    70.3634 |       70.355 |     70.375 |         0.03 |         0.09 |     0.0643647 |            0.06 |          0.07 | GBX              |                281 | LSE        |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:09:00 | LSE_SAMPLE_BARS::VOD | QTE_1M      |        0 | 2024-01-03 08:08:07.501 |             70.37 |           13,542 | 2024-01-03 08:08:07.501 |             70.41 |            4,716 | 2024-01-03 08:08:58.550 |      70.48 |           2,800 |                   70.51 |                  1,408 | 2024-01-03 08:08:07.501 |     70.41 |          4,716 |                  70.37 |             13,542 | 2024-01-03 08:08:59.397 |            70.45 |             100 | 2024-01-03 08:08:59.397 |            70.51 |           6,124 |    70.4259 |       70.46  |     70.48  |         0.01 |         0.08 |     0.0506562 |            0.06 |          0.06 | GBX              |                347 | LSE        |
| LSE_SAMPLE_BARS::VOD | 2024-01-03 08:10:00 | LSE_SAMPLE_BARS::VOD | QTE_1M      |        0 | 2024-01-03 08:09:00.182 |             70.45 |              100 | 2024-01-03 08:09:00.182 |             70.51 |            1,408 | 2024-01-03 08:09:05.551 |      70.51 |             100 |                   70.55 |                  9,800 | 2024-01-03 08:09:05.539 |     70.49 |          1,055 |                  70.46 |                100 | 2024-01-03 08:09:55.303 |            70.48 |           4,251 | 2024-01-03 08:09:55.303 |            70.52 |           4,716 |    70.5049 |       70.505 |     70.5   |         0.03 |         0.08 |     0.0642581 |            0.06 |          0.04 | GBX              |                269 | LSE        |



## Futures Continuous Contracts

