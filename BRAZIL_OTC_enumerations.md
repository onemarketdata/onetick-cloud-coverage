# B3 (Bovespa) - OTC Market Enumerations

The São Paulo Stock, Commodities and Futures Exchange (known as B3 S.A. - Brasil, Bolsa,balcão) currently has several different trading market segments: the traditional stock exchange and over-the-counter markets, and the special trading segments Level 1, Level 2 and New Market (Novo Mercado), Bovespa Mais and Bovespa Mais Level 2, which allow the trading of securities of listed companies adopting a special level of corporate governance.

The following fields have Enumerations:


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* TRADE_PERIOD - Market period during which a trade was executed.


* TRADE_TYPE - Type of trade

# BOOK_TYPE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
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
| C

                           | Closing auction

                                                                                                     |
| L

                           | Outside hours (Late session)

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

                           | Cross trade

                                                                                                         |
| 24

                          | After-market trade

                                                                                                  |
| 26

                          | Out of sequence trade

