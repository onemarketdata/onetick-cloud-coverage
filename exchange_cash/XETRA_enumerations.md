# Xetra Exchange Enumerations

Xetra is an electronic trading system operated by Deutsche Boerse for trading equities and other securities.

The following fields have Enumerations:


* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* MKT_COND - Indicates any unusual market conditions


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


* TRADE_PERIOD - Market period during which a trade was executed.


* TRADE_TYPE - Type of trade

# AGGRESSOR_SIDE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| ‘””’

                              | Undefined (e.g. auction trades, off-book trades)

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
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| 0

                                 | Lit order book

                                                                                                                             |
| 1

                                 | Off-book

                                                                                                                                   |
| 2

                                 | Dark book

                                                                                                                                  |
| 6

                                 | Auction book

                                                                                                                               |
| R

                                 | Request for Quote

                                                                                                                          |
| ‘””’

                              | Not applicable

                                                                                                                             |
# MKT_COND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| ‘””’

                              | Unspecified

                                                                                                                                |
| CALL

                              | Continuous auction call

                                                                                                                    |
| CCALL

                             | Closing auction call [until 20170630]

                                                                                                      |
| CIRCAUC

                           | Circuit breaker auction

                                                                                                                    |
| CIRCAUCFRE

                        | Circuit breaker auction freeze

                                                                                                             |
| CLOSAUC

                           | Closing auction call

                                                                                                                       |
| CLOSAUCFRE

                        | Closing auction freeze

                                                                                                                     |
| CLOSE

                             | Closed

                                                                                                                                     |
| CONTINUOUS

                        | Continuous trading

                                                                                                                         |
| DEL

                               | Pending deletion [until 20170630]

                                                                                                          |
| ENDTR

                             | End of trading [until 20170630]

                                                                                                            |
| F

                                 | Fast market

                                                                                                                                |
| FREEZE

                            | Continous auction freeze

                                                                                                                   |
| FS

                                | Fast + stressed market

                                                                                                                     |
| HALT

                              | Halted [until 20170630]

                                                                                                                    |
| HOL

                               | Holiday [until 20170630]

                                                                                                                   |
| ICALL

                             | Intraday auction call [until 20170630]

                                                                                                     |
| IFRZ

                              | Intraday IPO auction freeze [until 20170630]

                                                                                               |
| IIPO

                              | Intraday IPO auction call [until 20170630]

                                                                                                 |
| INTRAUC

                           | Intraday auction

                                                                                                                           |
| INTRAUCFRE

                        | Intraday auction freeze

                                                                                                                    |
| IPOAUC

                            | IPO auction call

                                                                                                                           |
| IPOAUCFRE

                         | IPO auction freeze

                                                                                                                         |
| OCALL

                             | Opening auction call [until 20170630]

                                                                                                      |
| OFRZL

                             | Opening IPO auction freeze [until 20170630]

                                                                                                |
| OIPO

                              | Opening IPO auction call [until 20170630]

                                                                                                  |
| OPENAUC

                           | Opening auction call

                                                                                                                       |
| OPENAUCFRE

                        | Opening auction freeze

                                                                                                                     |
| PENDDELETE

                        | Pending deletion

                                                                                                                           |
| POSTR

                             | Post-trading [until 20170630]

                                                                                                              |
| PRECALL

                           | Continuous auction pre-call

                                                                                                                |
| PRETR

                             | Pre-trading [until 20170630]

                                                                                                               |
| PUBLISHED

                         | New instrument before its first day of trading

                                                                                             |
| RESTRICTED

                        | Trading halted, orders can only be deleted

                                                                                                 |
| S

                                 | Stressed market

                                                                                                                            |
| START

                             | Start of trading [until 20170630]

                                                                                                          |
| SUSP

                              | Suspended [until 20170630]

                                                                                                                 |
| SUSPENDED

                         | Suspended

                                                                                                                                  |
| TRADE

                             | Continuous trading [until 20170630]

                                                                                                        |
| TRADEATCLO

                        | Trading at closing price

                                                                                                                   |
| TRADHALT

                          | Halted

                                                                                                                                     |
| UNSUS

                             | Unsuspended [until 20170630]

                                                                                                               |
| VOLA

                              | Volatility auction [until 20170630]

                                                                                                        |
# MKT_PHASE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| BOOK

                              | Order management

                                                                                                                           |
| CALL

                              | Continuous auction call

                                                                                                                    |
| CCALL

                             | Closing auction call [until 20170630]

                                                                                                      |
| CIRCAUC

                           | Circuit breaker auction

                                                                                                                    |
| CIRCAUCFRE

                        | Circuit breaker auction freeze

                                                                                                             |
| CLOSAUC

                           | Closing auction call

                                                                                                                       |
| CLOSAUCFRE

                        | Closing auction freeze

                                                                                                                     |
| CLOSE

                             | Closed

                                                                                                                                     |
| CONTINUOUS

                        | Continuous trading

                                                                                                                         |
| DEL

                               | Pending deletion [until 20170630]

                                                                                                          |
| ENDTR

                             | End of trading [until 20170630]

                                                                                                            |
| FREEZE

                            | Continous auction freeze

                                                                                                                   |
| HALT

                              | Halted [until 20170630]

                                                                                                                    |
| HOL

                               | Holiday [until 20170630]

                                                                                                                   |
| ICALL

                             | Intraday auction call [until 20170630]

                                                                                                     |
| IFRZ

                              | Intraday IPO auction freeze [until 20170630]

                                                                                               |
| IIPO

                              | Intraday IPO auction call [until 20170630]

                                                                                                 |
| INTRAUC

                           | Intraday auction

                                                                                                                           |
| INTRAUCFRE

                        | Intraday auction freeze

                                                                                                                    |
| IPOAUC

                            | IPO auction call

                                                                                                                           |
| IPOAUCFRE

                         | IPO auction freeze

                                                                                                                         |
| OCALL

                             | Opening auction call [until 20170630]

                                                                                                      |
| OFRZL

                             | Opening IPO auction freeze [until 20170630]

                                                                                                |
| OIPO

                              | Opening IPO auction call [until 20170630]

                                                                                                  |
| OPENAUC

                           | Opening auction call

                                                                                                                       |
| OPENAUCFRE

                        | Opening auction freeze

                                                                                                                     |
| PENDDELETE

                        | Pending deletion

                                                                                                                           |
| POSTR

                             | Post-trading [until 20170630]

                                                                                                              |
| PRECALL

                           | Continuous auction pre-call

                                                                                                                |
| PRETR

                             | Pre-trading [until 20170630]

                                                                                                               |
| PUBLISHED

                         | New instrument before its first day of trading

                                                                                             |
| RESTRICTED

                        | Trading halted, orders can only be deleted

                                                                                                 |
| RETCALL

                           | Retail auction call

                                                                                                                        |
| RETPRECALL

                        | Retail auction pre-call

                                                                                                                    |
| START

                             | Start of trading [until 20170630]

                                                                                                          |
| SUSP

                              | Suspended [until 20170630]

                                                                                                                 |
| SUSPENDED

                         | Suspended

                                                                                                                                  |
| TRADE

                             | Continuous trading [until 20170630]

                                                                                                        |
| TRADEATCLO

                        | Trading at closing price

                                                                                                                   |
| TRADHALT

                          | Halted

                                                                                                                                     |
| UNSUS

                             | Unsuspended [until 20170630]

                                                                                                               |
| VOLA

                              | Volatility auction [until 20170630]

                                                                                                        |
# MMT_ALGO_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not a benchmark trade

                                                                                                                      |
| B

                                 | Benchmark trade

                                                                                                                            |
| S

                                 | Reference price trade

                                                                                                                      |
# MMT_CROSS_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not a cross trade

                                                                                                                          |
| X

                                 | Agency cross trade

                                                                                                                         |
# MMT_DEFERRAL_TYPE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | No deferral / unspecified

                                                                                                                  |
| 1

                                 | Limited details

                                                                                                                            |
| 2

                                 | Daily aggregated trade

                                                                                                                     |
| 3

                                 | Volume omission trade

                                                                                                                      |
| 4

                                 | 4 weeks aggregated trade

                                                                                                                   |
| 5

                                 | Indefinite aggregated trade

                                                                                                                |
| 6

                                 | Volume omission trade eligible for enrichment in aggregated form

                                                                           |
| 7

                                 | Full details of earlier Limited Details trade

                                                                                              |
| 8

                                 | Full details of earlier Daily Aggregated trade

                                                                                             |
| 9

                                 | Full details of earlier Volume Omission trade

                                                                                              |
| V

                                 | Full details of 4 Weeks Aggregated trade

                                                                                                   |
| W

                                 | Full details of Volume Omission trade eligible for enrichment in aggregated form

                                                           |
# MMT_DIVIDEND_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
| E

                                 | Ex-/cum-dividend

                                                                                                                           |
# MMT_DUP_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Unique trade report

                                                                                                                        |
| 1

                                 | Duplicative trade reported to more than one APA

                                                                                            |
# MMT_MKT_MECH - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
| 1

                                 | Central Limit Order Book

                                                                                                                   |
| 2

                                 | Quote-Driven Market

                                                                                                                        |
| 3

                                 | Dark Book

                                                                                                                                  |
| 4

                                 | Off Book

                                                                                                                                   |
| 6

                                 | Request for Quote

                                                                                                                          |
| 7

                                 | Hybrid / Other

                                                                                                                             |
| 8

                                 | Hybrid

                                                                                                                                     |
# MMT_MOD_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
| 1

                                 | Negotiated trade in liquid instruments

                                                                                                     |
| 2

                                 | Negotiated trade in illiquid instruments

                                                                                                   |
| 3

                                 | Negotiated trade subject to conditions other than the market price

                                                                         |
| 4

                                 | Pre-trade transparency waiver for illiquid instrument on an SI

                                                                             |
| 5

                                 | Pre-trade transparency waiver for trade larger than Standard Market Size on an SI

                                                          |
| 6

                                 | Pre-trade transparency waivers for trade larger than Standard Market Size on an SI and illiquid instrument on an SI

                        |
| N

                                 | Negotiated trade

                                                                                                                           |
# MMT_OFF_BOOK_AUTO_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
| M

                                 | Off-book manual

                                                                                                                            |
| Q

                                 | Off-book automated

                                                                                                                         |
# MMT_PRICE_FORMING_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| J

                                 | Trade not contributing to the price discovery process

                                                                                      |
| N

                                 | Price not available but pending

                                                                                                            |
| P

                                 | Plain vanilla (price-forming) trade

                                                                                                        |
| T

                                 | Non-price forming (technical) trade

                                                                                                        |
# MMT_PUB_MODE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Immediate publication

                                                                                                                      |
| 1

                                 | Delayed publication / late reported

                                                                                                        |
| 2

                                 | Deferred publication (Large in Scale)

                                                                                                      |
| 3

                                 | Deferred publication (illiquid instrument)

                                                                                                 |
| 4

                                 | Deferred publication (size specific to instrument)

                                                                                         |
| 5

                                 | Deferred publication (illiquid instrument and size specific to instrument)

                                                                 |
| 6

                                 | Deferred publication (illiquid instrument and Large in Scale)

                                                                              |
# MMT_TRANS_CAT - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
| D

                                 | Dark trade

                                                                                                                                 |
# MMT_TRD_MODE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| P

                                 | On demand auction

                                                                                                                          |
| U

                                 | Unscheduled auction

                                                                                                                        |
# TRADE_PERIOD - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| A

                                 | Other auction [e.g. after-hours odd lot auction]

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
| p

                                 | Auction initiated by market participant

                                                                                                    |
| u

                                 | Unscheduled auction (extended hours)

                                                                                                       |
| -

                                 | Regular trading

                                                                                                                            |
| ‘””’

                              | Not applicable

                                                                                                                             |
# TRADE_TYPE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Regular trade

                                                                                                                              |
| 0

                                 | Opening auction trade

                                                                                                                      |
| 1

                                 | Intraday auction trade

                                                                                                                     |
| 2

                                 | Volatility auction trade

                                                                                                                   |
| 3

                                 | Closing auction trade

                                                                                                                      |
| 5

                                 | IPO auction trade

                                                                                                                          |
| e

                                 | Retail trade

                                                                                                                               |
| m

                                 | Midpoint trade

                                                                                                                             |
| I

                                 | EnLight trade

                                                                                                                              |
| OTC

                               | OTC trade [until 20170630]

                                                                                                                 |
| P

                                 | Xetra Midpoint trade [until 20170630]

                                                                                                      |
| S

                                 | Xetra Best trade [until 20201120]

                                                                                                          |
| VAL

                               | Price without turnover (valuation price) [until 20170630]

                                                                                  |
| X

                                 | Regular trade [until 20170630]

