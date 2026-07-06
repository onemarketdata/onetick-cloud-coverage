# Cboe Australia (CXA) Enumerations

Cboe Australia, formerly Chi-X Australia, is an alternative trading system providing trading in Australian equities, ETFs, and other listed securities.

The following fields have Enumerations:


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* TRADE_PERIOD - Market period during which a trade was executed.


* TRADE_TYPE - Type of trade

# BOOK_TYPE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 0

                             | Lit order book

                                                                                                         |
| 1

                             | Off-book

                                                                                                               |
| 2

                             | Dark book

                                                                                                              |
# TRADE_PERIOD - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| -

                             | Regular trading

                                                                                                        |
| T

                             | Trading at closing price

                                                                                               |
# TRADE_TYPE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| 0

                             | Regular trade

                                                                                                          |
| 112

                           | Portfolio trade (delayed)

                                                                                              |
| 116

                           | Large principal trade (delayed)

                                                                                        |
| 66

                            | Block trade

                                                                                                            |
| 67

                            | Broker preferenced trade

                                                                                               |
| 69

                            | Out of hours trade

                                                                                                     |
| 70

                            | ETF unit creation / redemption

                                                                                         |
| 76

                            | Permitted trade during post-trading

                                                                                    |
| 77

                            | Permitted trade during pre-trading

                                                                                     |
| 80

                            | Portfolio trade

                                                                                                        |
| 83

                            | Trade with price improvement

                                                                                           |
| 84

                            | Large principal trade

                                                                                                  |
| B

                             | BIDS Block trade

                                                                                                       |
| C

                             | Regular trade against hidden limit order

                                                                               |
| F

                             | Far point trade

                                                                                                        |
| FB

                            | Far point trade with broker preferencing

                                                                               |
| I

                             | BIDS Price Improved trade

                                                                                              |
| M

                             | MOC trade

                                                                                                              |
| MB

                            | MOC trade with broker preferencing

                                                                                     |
| N

                             | Near point trade

                                                                                                       |
| NB

                            | Near point trade with broker preferencing

                                                                              |
| P

                             | Midpoint trade

                                                                                                         |
| PB

                            | Midpoint trade with broker preferencing

