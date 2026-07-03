# Korea Consolidated Equities Enumerations

Consolidated data from all Korean equities exchanges.

The following fields have Enumerations:


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* CALL_PUT_IND - “C” - Call option, “P” - Put option


* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.


* QUOTE_VENUE - Venue (MIC) from which a quote originates


* TRADE_PERIOD - Market period during which a trade was executed.


* TRADE_TYPE - Type of trade


* TRADE_VENUE - Identifies the venue where a trade was executed.   Typically a MIC, with the special values “XOFF” for off-exchange and “SINT” for Systematic Internaliser trades.

# BOOK_TYPE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 0

                           | Lit order book

                                                                                                                    |
| 1

                           | Off-book

                                                                                                                          |
| 2

                           | Dark book

                                                                                                                         |
# CALL_PUT_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| C

                           | Call option

                                                                                                                       |
| P

                           | Put option

                                                                                                                        |
# OMD_STATUS - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| A

                           | Auction

                                                                                                                           |
| B

                           | Break / Pause

                                                                                                                     |
| C

                           | Closing auction

                                                                                                                   |
| D

                           | Delisted / Pending deletion

                                                                                                       |
| H

                           | Halted

                                                                                                                            |
| I

                           | Scheduled intraday auction

                                                                                                        |
| M

                           | Mandatory quoting period

                                                                                                          |
| N

                           | New instrument / Pre-listing

                                                                                                      |
| O

                           | Opening auction

                                                                                                                   |
| P

                           | Pre-market

                                                                                                                        |
| Q

                           | Indicative quoting period

                                                                                                         |
| R

                           | Off-book trade reporting

                                                                                                          |
| S

                           | Suspended

                                                                                                                         |
| T

                           | Continuous trading

                                                                                                                |
| U

                           | Unscheduled auction

                                                                                                               |
| c

                           | Closed

                                                                                                                            |
| i

                           | IPO / Public offering auction

                                                                                                     |
| n

                           | No market phase / Unspecified

                                                                                                     |
| o

                           | Order management

                                                                                                                  |
| p

                           | Post-market

                                                                                                                       |
| t

                           | Trading at last price

                                                                                                             |
# QUOTE_VENUE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| XKOS

                        | Kosdaq

                                                                                                                            |
| XKRX

                        | Korea Exchange

                                                                                                                    |
# TRADE_PERIOD - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| -

                           | Regular trading

                                                                                                                   |
| C

                           | Closing auction

                                                                                                                   |
| E

                           | Outside hours (Early session)

                                                                                                     |
| L

                           | Outside hours (Late session)

                                                                                                      |
| O

                           | Opening auction

                                                                                                                   |
| T

                           | Trading at closing price

                                                                                                          |
| U

                           | Unscheduled auction

                                                                                                               |
# TRADE_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| 1

                           | Regular trade

                                                                                                                     |
| 10

                          | Pre-opening basket trade

                                                                                                          |
| 11

                          | K-Blox block trade

                                                                                                                |
| 12

                          | Basket trade

                                                                                                                      |
| 13

                          | Single price post-market trade

                                                                                                    |
| 14

                          | Quote without trade (valuation price)

                                                                                             |
| 15

                          | Pre-open A-Blox block trade

                                                                                                       |
| 16

                          | A-Blox block trade

                                                                                                                |
| 17

                          | Buy-in trade

                                                                                                                      |
| 18

                          | Auction trade (volatility auction)

                                                                                                |
| 19

                          | Auction trade (extended volatility auction)

                                                                                       |
| 2

                           | Pre-opening trade (at previous close)

                                                                                             |
| 20

                          | Auction trade (off-hours volatility auction)

                                                                                      |
| 21

                          | Auction trade (extended off-hours volatility auction)

                                                                             |
| 3

                           | After-hours block trade

                                                                                                           |
| 32

                          | Block trade

                                                                                                                       |
| 33

                          | Block trade (pre-market)

                                                                                                          |
| 34

                          | Block trade (post-market)

                                                                                                         |
| 4

                           | After-hours trade at closing price

                                                                                                |
| 5

                           | Pre-opening block trade

                                                                                                           |
| 6

                           | After-hours K-Blox block trade

                                                                                                    |
| 7

                           | After-hours basket trade

                                                                                                          |
| 8

                           | Single price auction trade

                                                                                                        |
| 9

                           | Pre-opening K-Blox block trade

                                                                                                    |
# TRADE_VENUE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| XKOS

                        | Kosdaq

                                                                                                                            |
| XKRX

                        | Korea Exchange

