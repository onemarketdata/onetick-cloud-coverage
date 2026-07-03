# Luxembourg Stock Exchange Enumerations

The Luxembourg Stock Exchange specializes in the listing of international securities like bonds and funds.

The following fields have Enumerations:


* CALL_PUT_IND - “C” - Call option, “P” - Put option


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


* REASON_CODE - Reason for an instrument status update


* TRADE_TYPE - Type of trade

# CALL_PUT_IND - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| C

                           | Call option

                                                                                                                       |
| P

                           | Put option

                                                                                                                        |
# MKT_PHASE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| 1

                           | Auction

                                                                                                                           |
| 10

                          | Halted

                                                                                                                            |
| 201

                         | Closed (pre-trading)

                                                                                                              |
| 202

                         | Auction call

                                                                                                                      |
| 203

                         | Auction uncrossing

                                                                                                                |
| 204

                         | Continuous trading

                                                                                                                |
| 205

                         | Closing auction call

                                                                                                              |
| 206

                         | Closing auction uncrossing

                                                                                                        |
| 207

                         | Trading at last

                                                                                                                   |
| 209

                         | Closed (post-trading)

                                                                                                             |
| 211

                         | Inaccessible

                                                                                                                      |
| 8

                           | Suspended

                                                                                                                         |
| 9

                           | Reserved

                                                                                                                          |
# MMT_ALGO_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not applicable

                                                                                                                    |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not applicable

                                                                                                                    |
# MMT_TRD_MODE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
# REASON_CODE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                        | Unspecified

                                                                                                                       |
| 0

                           | Scheduled transition

                                                                                                              |
| 11

                          | Knock-in by the issuer

                                                                                                            |
| 12

                          | Knock-out by the exchange

                                                                                                         |
| 13

                          | Knock-out by the issuer

                                                                                                           |
| 15

                          | Action by Market Operations

                                                                                                       |
| 20

                          | New listing

                                                                                                                       |
| 21

                          | Status change in the underlying security

                                                                                          |
| 22

                          | Trade price outside the Liquidity Provider quote

                                                                                  |
| 23

                          | Technical halt

                                                                                                                    |
| 4

                           | Collars breached

                                                                                                                  |
| 7

                           | Automatic re-opening

                                                                                                              |
| 8

                           | No liquidity provider quote

                                                                                                       |
# TRADE_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                        | Unspecified

                                                                                                                       |
| 1

                           | Standard trade

                                                                                                                    |
| 24

                          | Trade cancellation

                                                                                                                |
| 25

                          | Off-market trade

                                                                                                                  |
| 27

                          | VWAP trade

                                                                                                                        |
| 32

                          | OTC trade

                                                                                                                         |
| 33

                          | Dark trade

                                                                                                                        |
| 5

                           | Guaranteed Cross

