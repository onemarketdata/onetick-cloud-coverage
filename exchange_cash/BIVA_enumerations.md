# BIVA (Bolsa Institucional de Valores) Enumerations

The Institutional Stock Exchange, commonly known as BIVA, is Mexico’s second stock exchange, based in Mexico City. BIVA began operations on 25 July 2018 and trades the same instruments as the other exchange in Mexico, the Bolsa Mexicana de Valores: equities, debts, warrants and some Mexican-specific instruments such as CKDs and FIBRAs.

The following fields have Enumerations:


* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue


* REASON_CODE - Reason for an instrument status update


* TRADE_PERIOD - Market period during which a trade was executed.


* TRADE_TYPE - Type of trade


* TRADING_STATUS - Indicates whether the instrument is subject to a halt or suspension

# AGGRESSOR_SIDE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| ‘””’

                        | Undefined (e.g. auction trades, off-book trades, trades against hidden liquidity)

                                   |
| B

                           | Buy

                                                                                                                 |
| S

                           | Sell

                                                                                                                |
# BOOK_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| 0

                           | Lit order book

                                                                                                      |
| 1

                           | Off-book

                                                                                                            |
| 2

                           | Dark book

                                                                                                           |
| 8

                           | Market on close (MOC) book

                                                                                          |
# MKT_PHASE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                        | No market phase

                                                                                                     |
| E

                           | End of system hours

                                                                                                 |
| M

                           | End of market hours

                                                                                                 |
| P

                           | Post-close

                                                                                                          |
| Q

                           | Start of market hours

                                                                                               |
| S

                           | Start of system hours

                                                                                               |
| T

                           | End of post-close

                                                                                                   |
| U

                           | Scheduled auction end

                                                                                               |
| V

                           | Scheduled auction start

                                                                                             |
# REASON_CODE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                        | Not applicable

                                                                                                      |
| A

                           | Continuous auction start

                                                                                            |
| B

                           | Continuous auction end

                                                                                              |
| C

                           | Non-compliant with listing requirements

                                                                             |
| E

                           | Expired

                                                                                                             |
| H

                           | Volatility auction

                                                                                                  |
| I

                           | Start of Indication of Interest (IOA)

                                                                               |
| L

                           | Not yet available for trading

                                                                                       |
| M

                           | Suspended by Market Surveillance

                                                                                    |
| N

                           | Normal trading

                                                                                                      |
| O

                           | Suspended by market of origin

                                                                                       |
| Q

                           | News pending

                                                                                                        |
| S

                           | Static price band breach

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
| I

                           | Intraday auction

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
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| BLK

                         | Block trade

                                                                                                         |
| C

                           | Intentional cross

                                                                                                   |
| E

                           | Exceptional Cross (at VWAP/TWAP)

                                                                                    |
| I

                           | IPO cross

                                                                                                           |
| R

                           | Regular trade

                                                                                                       |
| U

                           | Unintentional cross

                                                                                                 |
# TRADING_STATUS - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                        | Active

                                                                                                              |
| V

                           | Suspended

