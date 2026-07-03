# ASX 24 (Sydney Futures Exchange) Enumerations

ASX 24, formerly the Sydney Futures Exchange, offers trading in futures and options on interest rates, equities, commodities, and currencies.

The following fields have Enumerations:


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* TRADE_PERIOD - Market period during which a trade was executed.


* TRADE_TYPE - Type of trade

# BOOK_TYPE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 0

                           | Lit order book

                                                                                                      |
| 1

                           | Off-book

                                                                                                            |
# TRADE_PERIOD - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Regular trading

                                                                                                     |
| I

                           | Intraday auction

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
| 0

                           | Regular trade

                                                                                                       |
| 1

                           | Auction trade [prior to 20170319: Sweeping trade]

                                                                   |
| 2

                           | Levelling trade [until 20170320]

                                                                                    |
| 3

                           | Spread to underlying trade

                                                                                          |
| 4

                           | Spread to spread trade

                                                                                              |
| 5

                           | Inter-product spread trade

                                                                                          |
| 6

                           | Strip to strip trade

                                                                                                |
| 7

                           | Strip to outright trade

