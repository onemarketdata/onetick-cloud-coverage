# Cboe EDGX Enumerations

he Cboe EDGX Exchange is a prominent U.S. equities and options market operated by Cboe Global Markets. It is distinguished by its extended trading hours —opening at 4:00 AM ET—its patent-pending Retail Priority allocation model, and a comprehensive depth-of-book feed for market participants

The following fields have Enumerations:


* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.


* TRADE_TYPE - Type of trade


* TRADE_TYPE_EXT - Extended trade type code


* ODD_LOT - Indicates whether a trade was an odd lot


* TRADE_PERIOD - Market period during which a trade was executed.


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* RPI - Indicates the presence of Retail Price Improvement interest on bid and/or ask side


* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue


* UPDATE_TYPE - Type of update


* ORDER_TYPE - Type of order.

# AGGRESSOR_SIDE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| ‘””’

                          | Undefined (e.g. auction trades, trades against hidden liquidity)

                                                       |
| B

                             | Buy

                                                                                                                    |
| S

                             | Sell

                                                                                                                   |
# TRADE_TYPE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                          | Regular trade

                                                                                                          |
| H

                             | Regular trade against hidden liquidity

                                                                                 |
| R

                             | Routed trade

                                                                                                           |
| T

                             | Regular trade against retail liquidity

                                                                                 |
# TRADE_TYPE_EXT - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                          | Unspecified [for future use]

                                                                                           |
# ODD_LOT - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                          | Unspecified [for future use]

                                                                                           |
# TRADE_PERIOD - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| -

                             | Regular trading

                                                                                                        |
| E

                             | Extended hours (Early session)

                                                                                         |
| L

                             | Extended hours (Late session)

                                                                                          |
# BOOK_TYPE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| 0

                             | Lit order book

                                                                                                         |
| 9

                             | Off-exchange

                                                                                                           |
# RPI - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                          | No retail interest

                                                                                                     |
| A

                             | Retail interest on bid side

                                                                                            |
| B

                             | Retail interest on ask side

                                                                                            |
| C

                             | Retail interest on bid and ask side

                                                                                    |
# MKT_PHASE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| A

                             | Accepting order for queuing

                                                                                            |
| H

                             | Halted

                                                                                                                 |
| Q

                             | Quote only

                                                                                                             |
| S

                             | Closed

                                                                                                                 |
| T

                             | Trading

                                                                                                                |
# UPDATE_TYPE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| A

                             | Add

                                                                                                                    |
| D

                             | Delete

                                                                                                                 |
| F

                             | Fill

                                                                                                                   |
| M

                             | Modify

                                                                                                                 |
| P

                             | Partial fill

                                                                                                           |
# ORDER_TYPE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| L

                             | Limit order

                                                                                                            |
| R

                             | Retail Priority order

