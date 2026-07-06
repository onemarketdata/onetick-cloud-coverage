# Madrid Stock Exchange (SIBE) Enumerations

The Madrid Stock Exchange is one of four regional stock exchanges in Spain that make up the overall Spanish stock market.

The following fields have Enumerations:


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


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


* TRADE_TYPE [until 20221111] -

# BOOK_TYPE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 0

                             | Lit order book

                                                                                                         |
| 1

                             | Off-book

                                                                                                               |
| 2

                             | Dark book

                                                                                                              |
| 9

                             | Off-exchange

                                                                                                           |
| R

                             | Request for Quote

                                                                                                      |
# MKT_PHASE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| -

                             | Inactive [until 20221111]

                                                                                              |
| 1

                             | Pre-trading

                                                                                                            |
| 100

                           | Trading at last price

                                                                                                  |
| 101

                           | End of closing auction

                                                                                                 |
| 102

                           | Closing price calculation

                                                                                              |
| 2

                             | Opening auction

                                                                                                        |
| 3

                             | Continuous trading

                                                                                                     |
| 4

                             | Closing auction

                                                                                                        |
| 5

                             | Post-trading

                                                                                                           |
| 6

                             | Intraday auction

                                                                                                       |
| 9

                             | Unscheduled auction

                                                                                                    |
| A

                             | Accepting orders

                                                                                                       |
| a

                             | Auction

                                                                                                                |
| B

                             | Break

                                                                                                                  |
| C

                             | Closed

                                                                                                                 |
| c

                             | Extended closing auction

                                                                                               |
| E

                             | Post-trading

                                                                                                           |
| H

                             | Halted

                                                                                                                 |
| H100

                          | Regulatory halt [until 20221111]

                                                                                       |
| H101

                          | Halted by Market Surveillance [until 20221111]

                                                                         |
| H102

                          | Knocked out [until 20221111]

                                                                                           |
| H103

                          | Knock-in pending [until 20221111]

                                                                                      |
| I

                             | Intraday auction

                                                                                                       |
| k

                             | Knocked out

                                                                                                            |
| L

                             | Closing auction

                                                                                                        |
| m

                             | Manual auction

                                                                                                         |
| M

                             | Pre-trading

                                                                                                            |
| n

                             | Not tradable

                                                                                                           |
| N

                             | Unscheduled auction [until 20221111]

                                                                                   |
| N100

                          | Manual auction [until 20221111]

                                                                                        |
| N101

                          | Opening auction extension [until 20221111]

                                                                             |
| N102

                          | Closing auction extension [until 20221111]

                                                                             |
| N103

                          | Volatility auction [until 20221111]

                                                                                    |
| o

                             | Extended opening auction

                                                                                               |
| r

                             | Regulatory halt

                                                                                                        |
| s

                             | Halted by Market Surveillance

                                                                                          |
| T

                             | Continuous trading

                                                                                                     |
| U

                             | Underlying halted

                                                                                                      |
| V

                             | Suspended

                                                                                                              |
| v

                             | Volatility auction

                                                                                                     |
| X

                             | Extraordinary market conditions [until 20221111]

                                                                       |
| Z

                             | Trading at last price

                                                                                                  |
# MMT_ALGO_IND - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| 1

                             | Central Limit Order Book

                                                                                               |
| 3

                             | Dark Book

                                                                                                              |
| 4

                             | Off Book

                                                                                                               |
| 5

                             | Periodic auction

                                                                                                       |
| 6

                             | Request for Quotes

                                                                                                     |
# MMT_MOD_IND - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| -

                             | Not applicable

                                                                                                         |
| D

                             | Dark trade

                                                                                                             |
| R

                             | Trade receiving price improvement

                                                                                      |
| Y

                             | Exchange for physical

                                                                                                  |
| Z

                             | Package trade

                                                                                                          |
# MMT_TRD_MODE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| 2

                             | Continuous trading

                                                                                                     |
| 3

                             | Trading at closing price

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
# TRADE_PERIOD - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| A

                             | Auction

                                                                                                                |
| C

                             | Closing Auction

                                                                                                        |
| I

                             | Intraday Auction

                                                                                                       |
| O

                             | Opening Auction

                                                                                                        |
| T

                             | Trading at last price

                                                                                                  |
| U

                             | Unscheduled Auction

                                                                                                    |
| -

                             | Regular trading

                                                                                                        |
# TRADE_TYPE [until 20221111] - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| 1001

                          | Communicated application

                                                                                               |
| 1002

                          | Authorised application (volume)

                                                                                        |
| 1003

                          | Authorised application (corporate interest)

                                                                            |
| 1004

                          | Authorised application (execution of contracts)

                                                                        |
| 1005

                          | Authorised application (other reasons)

                                                                                 |
| 1006

                          | Validation (communicated)

                                                                                              |
| 1007

                          | Authorised validation (volume)

                                                                                         |
| 1008

                          | Authorised validation (corporate interest)

                                                                             |
| 1009

                          | Authorised validation (execution of contracts)

                                                                         |
| 1010

                          | Authorised validation (other reasons)

                                                                                  |
| 1011

                          | Transaction between members (communicated)

                                                                             |
| 1012

                          | Transaction between members (authorised)

                                                                               |
| 1013

                          | Transaction between members (volume)

                                                                                   |
| 1014

                          | Transaction between members (corporate interest)

                                                                       |
| 1015

                          | Transaction between members (execution of contracts)

                                                                   |
| 1016

                          | Transaction between members (other reasons)

                                                                            |
| 1017

                          | Application to cater for a linked position

                                                                             |
| 1018

                          | Transaction to cater for a linked position

                                                                             |
| 1019

                          | Option exercise

                                                                                                        |
| 1020

                          | Block trade

                                                                                                            |
| 1021

                          | Public offer (buy)

                                                                                                     |
| 1022

                          | Public offer (sell)

                                                                                                    |
| 1023

                          | Public offer (subscription)

                                                                                            |
| 1024

                          | Special trade (Delta neutral)

                                                                                          |
| 1025

                          | Special trade (VWAP)

                                                                                                   |
| 1026

                          | Forced buying

                                                                                                          |
| 1027

                          | Forced selling

                                                                                                         |
| 1028

                          | NAV special trade T+1

                                                                                                  |
| 1029

                          | NAV special trade T+2

                                                                                                  |
| 1030

                          | NAV special trade T+3

                                                                                                  |
| 1031

                          | Transaction without CCP

                                                                                                |
| 1032

                          | Application without CCP

                                                                                                |
| 1033

                          | Investment fund T+1

                                                                                                    |
| 1034

                          | Investment fund T+2

                                                                                                    |
| 1035

                          | Investment fund T+3

                                                                                                    |
| 1036

                          | VWAP trade

                                                                                                             |
| 34

                            | Block trade

                                                                                                            |
| D

                             | Trade cancellation [until 20161230]

                                                                                    |
| I

                             | Regular trade [until 20161230]

                                                                                         |
| T1

                            | Trade from continuous trading

                                                                                          |
| T2

                            | Opening auction trade

                                                                                                  |
| T3

                            | Closing auction trade

                                                                                                  |
| T4

                            | Volatility auction trade

                                                                                               |
| T5

                            | Trade from manual auction

                                                                                              |
| T6

                            | Trade from extended opening auction

                                                                                    |
| T7

                            | Trade from extended closing auction

                                                                                    |
| T8

                            | Trade from closing price trading

