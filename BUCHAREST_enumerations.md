# Bucharest Stock Exchange Enumerations

The Bucharest Stock Exchange is the stock exchange of Romania located in Bucharest

The following fields have Enumerations:


* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.


* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue


* MMT_ALGO_IND - Identifies whether a trade involved an algorithmic order.


* MMT_BENCHMARK_IND - Identifies whether a trade was priced according to a defined benchmark (e.g. VWAP) or reference price (e.g. midpoint of the primary market BBO), or whether it was part of a trade in multiple instruments (contingent trade or portfolio trade).


* MMT_CROSS_IND - Identifies agency cross trades, where a broker crossed two client orders outside the order book.


* MMT_DEFERRAL_TYPE - Type of publication deferral or subsequent enrichment applied to a trade report.


* MMT_DIVIDEND_IND - Identifies whether a trade includes special dividend arrangements, e.g. a trade sold cum-dividend during an ex-dividend period.


* MMT_DUP_IND - Identifies trades reported to more than one Approved Publication Arrangement.


* MMT_MKT_MECH - Market mechanism through which a trade was executed.


* MMT_MOD_IND - Identifies trade cancellations, or amendments of a previous trade.


* MMT_NEGOTIATED_IND - Indicates privately negotiated trades, or Systematic Internaliser trades exempt from pre-trade transparency.


* MMT_OFF_BOOK_AUTO_IND - Identifies whether an off-book trade report was executed via a manual or automated process.


* MMT_PRICE_FORMING_IND - Identifies whether a trade is price-forming, or contributes to the price discovery process.


* MMT_PUB_MODE - Identifies whether a trade was subject to delayed publication, and the reason for the deferral.


* MMT_TRANS_CAT - Identifies various special categories of trade.


* MMT_TRD_MODE - Trading period during which an on-book trade was executed, or origin of an off-book trade report (on-exchange / off-exchange / SI).


* TRADE_TYPE - Type of trade

# AGGRESSOR_SIDE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| ‘””’

                        | Undefined (e.g. auction trades, off-book trades)

                                                                    |
| B

                           | Buy

                                                                                                                 |
| S

                           | Sell

                                                                                                                |
# MKT_PHASE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| 0

                           | Pre-trading

                                                                                                         |
| 1

                           | Suspended

                                                                                                           |
| 10

                          | Volatility auction

                                                                                                  |
| 2

                           | Deleted

                                                                                                             |
| 3

                           | Open

                                                                                                                |
| 4

                           | Closed

                                                                                                              |
| 5

                           | Opening/closing (uncrossing)

                                                                                        |
| 6

                           | Pre-open

                                                                                                            |
| 7

                           | Pre-close

                                                                                                           |
| 8

                           | Trading at last

                                                                                                     |
# MMT_ALGO_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not an algorithmic trade

                                                                                            |
| H

                           | Algorithmic trade

                                                                                                   |
# MMT_BENCHMARK_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not applicable

                                                                                                      |
# MMT_CROSS_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not applicable

                                                                                                      |
| X

                           | Cross trade

                                                                                                         |
# MMT_DEFERRAL_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | No deferral / unspecified

                                                                                           |
# MMT_DIVIDEND_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not applicable

                                                                                                      |
# MMT_DUP_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Unique trade report

                                                                                                 |
# MMT_MKT_MECH - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| 1

                           | Central Limit Order Book

                                                                                            |
| 4

                           | Off Book

                                                                                                            |
# MMT_MOD_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | New trade

                                                                                                           |
| A

                           | Amended trade

                                                                                                       |
| C

                           | Trade cancellation

                                                                                                  |
# MMT_NEGOTIATED_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not applicable

                                                                                                      |
| N

                           | Negotiated trade

                                                                                                    |
# MMT_OFF_BOOK_AUTO_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not applicable

                                                                                                      |
# MMT_PRICE_FORMING_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| P

                           | Plain vanilla (price-forming) trade

                                                                                 |
# MMT_PUB_MODE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Immediate publication

                                                                                               |
# MMT_TRANS_CAT - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not applicable

                                                                                                      |
# MMT_TRD_MODE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not applicable

                                                                                                      |
| 2

                           | Continuous trading

                                                                                                  |
| 3

                           | At Market Close trading

                                                                                             |
| 5

                           | Trade reporting (on-exchange)

                                                                                       |
| 6

                           | Trade reporting (off-exchange)

                                                                                      |
| 7

                           | Trade reporting (Systematic Internaliser)

                                                                           |
| I

                           | Intraday auction

                                                                                                    |
| K

                           | Closing auction

                                                                                                     |
| O

                           | Opening auction

                                                                                                     |
| U

                           | Unscheduled auction

                                                                                                 |
# TRADE_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| 01

                          | On-book - Buy-side aggressor

                                                                                        |
| 02

                          | On-book - Sell-side aggressor

                                                                                       |
| 03

                          | On-book - Routed trade

                                                                                              |
| 04

                          | On-book - Auction trade

                                                                                             |
| 05

                          | On-book - Cross trade

                                                                                               |
| 11

                          | Off-book - Buy-side aggressor

                                                                                       |
| 12

                          | Off-book - Sell-side aggressor

                                                                                      |
| 13

                          | Off-book - Routed trade

                                                                                             |
| 14

                          | Off-book- Auction trade

                                                                                             |
| 15

                          | Off-book - Cross trade

                                                                                              |
| 21

                          | Special auction (public offering / tender offer / redemption) - Buy-side aggressor

                                  |
| 22

                          | Special auction (public offering / tender offer / redemption) - Sell-side aggressor

                                 |
| 23

                          | Special auction (public offering / tender offer / redemption) - Routed trade

                                        |
| 24

                          | Special auction (public offering / tender offer / redemption) - Auction trade

                                       |
| 25

                          | Special auction (public offering / tender offer / redemption) - Cross trade

