# Nasdaq Nordic (Stockholm, Copenhagen, Helsinki, Iceland) - Equities Enumerations

Nasdaq Nordic operates the stock exchanges in Stockholm, Copenhagen, Helsinki and Iceland facilitating trading in Nordic equities.

The following fields have Enumerations:


* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue


* MMT_ALGO_IND - Identifies whether a trade involved an algorithmic order.


* MMT_BENCHMARK_IND - Identifies whether a trade was priced according to a defined benchmark (e.g. VWAP) or reference price (e.g. midpoint of the primary market BBO), or whether it was part of a trade in multiple instruments (contingent trade or portfolio trade).


* MMT_CROSS_IND - Identifies agency cross trades, where a broker crossed two client orders outside the order book.


* MMT_DEFERRAL_TYPE - Type of publication deferral or subsequent enrichment applied to a trade report.


* MMT_DUP_IND - Identifies trades reported to more than one Approved Publication Arrangement.


* MMT_MKT_MECH - Market mechanism through which a trade was executed.


* MMT_MOD_IND - Identifies trade cancellations, or amendments of a previous trade.


* MMT_NEGOTIATED_IND - Indicates privately negotiated trades, or Systematic Internaliser trades exempt from pre-trade transparency.


* MMT_OFF_BOOK_AUTO_IND - Identifies whether an off-book trade report was executed via a manual or automated process.


* MMT_PRICE_FORMING_IND - Identifies whether a trade is price-forming, or contributes to the price discovery process.


* MMT_PUB_MODE - Identifies whether a trade was subject to delayed publication, and the reason for the deferral.


* MMT_TRANS_CAT - Identifies various special categories of trade.


* MMT_TRD_MODE - Trading period during which an on-book trade was executed, or origin of an off-book trade report (on-exchange / off-exchange / SI).


* ORDER_TYPE - Type of order.


* REASON_CODE - Reason for an instrument status update


* TRADE_PERIOD - Market period during which a trade was executed.


* TRADE_TYPE - Type of trade


* UPDATE_TYPE - Type of update

# AGGRESSOR_SIDE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
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
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| 9

                             | Off-exchange

                                                                                                                               |
# MKT_PHASE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| 10

                            | Extended trading [until 20190719]

                                                                                                          |
| 11

                            | Mid-price auction [until 20190719]

                                                                                                         |
| 14

                            | End of trading [until 20190719]

                                                                                                            |
| 15

                            | Statistics [until 20190719]

                                                                                                                |
| 16

                            | Order expiry [until 20190719]

                                                                                                              |
| 18

                            | Suspended [until 20190719]

                                                                                                                 |
| 19

                            | Technical halt [until 20190719]

                                                                                                            |
| 22

                            | Trading at closing price

                                                                                                                   |
| 4

                             | Terminating

                                                                                                                                |
| A

                             | Trading at closing price

                                                                                                                   |
| C

                             | Closed

                                                                                                                                     |
| H

                             | Halted

                                                                                                                                     |
| I

                             | Scheduled intraday auction

                                                                                                                 |
| L

                             | Closing auction

                                                                                                                            |
| O

                             | Opening auction

                                                                                                                            |
| P

                             | Pre-trading

                                                                                                                                |
| Q

                             | Unscheduled intraday auction

                                                                                                               |
| S

                             | Post-trading

                                                                                                                               |
| T

                             | Continuous trading

                                                                                                                         |
# MMT_ALGO_IND - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                             | Not applicable

                                                                                                                             |
| 1

                             | Benchmark trade executed at the closing price

                                                                                              |
| 2

                             | Portfolio trade + benchmark trade executed at the closing price

                                                                            |
| 3

                             | Contingent trade + benchmark trade executed at the closing price

                                                                           |
| 4

                             | Contingent trade + portfolio trade + benchmark trade executed at the closing price

                                                         |
| B

                             | Benchmark trade

                                                                                                                            |
| C

                             | Contingent trade

                                                                                                                           |
| M

                             | Benchmark trade + contingent trade

                                                                                                         |
| N

                             | Contingent trade + portfolio trade

                                                                                                         |
| O

                             | Benchmark trade + contingent trade + portfolio trade

                                                                                       |
| P

                             | Portfolio trade

                                                                                                                            |
| S

                             | Reference price trade

                                                                                                                      |
| Y

                             | Benchmark trade + portfolio trade

                                                                                                          |
# MMT_CROSS_IND - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
# MMT_DUP_IND - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                             | Unique trade report

                                                                                                                        |
| 1

                             | Duplicative trade reported to more than one APA

                                                                                            |
| 2

                             | Intra-group trade

                                                                                                                          |
| 3

                             | Duplicative intra-group trade report

                                                                                                       |
| 4

                             | Cross-border duplicative trade report

                                                                                                      |
| 5

                             | Duplicative report within jurisdiction + cross-border duplicative trade report

                                                             |
| 6

                             | Intra-group trade + duplicative within jurisdiction + cross-border duplicative trade report

                                                |
| 7

                             | Intra-group trade + cross-border duplicative trade report

                                                                                  |
# MMT_MKT_MECH - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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

                             | Periodic Auction

                                                                                                                           |
# MMT_MOD_IND - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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

                             | Negotiated trade subject to conditions other than the current market price

                                                                 |
| 7

                             | OTC trade larger than LIS brought onto a venue

                                                                                             |
| 8

                             | Negotiated trade with pre-trade transparency waiver

                                                                                        |
| 9

                             | Large in Scale OTC negotiated trade in liquid instruments brought onto a venue

                                                             |
| a

                             | Large in Scale OTC negotiated trade in illiquid instruments brought onto a venue

                                                           |
| b

                             | Large in Scale OTC negotiated trade subject to conditions other than the current market price and brought onto a venue

                     |
| c

                             | Large in Scale OTC negotiated trade with pre-trade transparency waiver brought onto a venue

                                                |
| N

                             | Negotiated trade

                                                                                                                           |
# MMT_OFF_BOOK_AUTO_IND - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| Z

                             | Price not applicable

                                                                                                                       |
# MMT_PUB_MODE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                             | Not applicable

                                                                                                                             |
| D

                             | Dark trade

                                                                                                                                 |
| G

                             | RFMD give-up trade

                                                                                                                         |
| R

                             | Received price improvement

                                                                                                                 |
| Z

                             | Package trade

                                                                                                                              |
# MMT_TRD_MODE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| 1

                             | Auction

                                                                                                                                    |
| 2

                             | Continuous trading

                                                                                                                         |
| 3

                             | Trading at market close

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
# ORDER_TYPE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| L

                             | Limit order

                                                                                                                                |
| m

                             | Market maker order

                                                                                                                         |
| M

                             | Market order

                                                                                                                               |
# REASON_CODE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| AEX

                           | Auction extension

                                                                                                                          |
| E

                             | Auction extension

                                                                                                                          |
| KO

                            | Knock-out

                                                                                                                                  |
| MH

                            | Matching halt

                                                                                                                              |
| MMM

                           | Market maker missing

                                                                                                                       |
| RES

                           | Resting

                                                                                                                                    |
| RH

                            | Regulatory halt

                                                                                                                            |
| S1

                            | Suspended due to Market abuse

                                                                                                              |
| S2

                            | Suspended due to takeover bid

                                                                                                              |
| S3

                            | Suspended due to failure of issuer to disclose information

                                                                                 |
| S7

                            | Suspended for technical / administrative reasons

                                                                                           |
| S8

                            | Suspended due to suspension on another trading venue

                                                                                       |
| S9

                            | Suspended for other reasons

                                                                                                                |
| TH

                            | Trading halt

                                                                                                                               |
| TS

                            | Trading stop

                                                                                                                               |
| UNQ

                           | Underlying not quoted

                                                                                                                      |
| VHD

                           | Volatility halt (dynamic)

                                                                                                                  |
| VHS

                           | Volatility halt (static)

                                                                                                                   |
# TRADE_PERIOD - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| p

                             | Auction initiated by market participant

                                                                                                    |
| -

                             | Regular trading

                                                                                                                            |
# TRADE_TYPE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| 0

                             | `Nordic@Mid` trade

                                                                                                                           |
| 1

                             | Automatch

                                                                                                                                  |
| 158

                           | OTC trade with standard settlement

                                                                                                         |
| 164

                           | OTC trade with non-standard settlement

                                                                                                     |
| 237

                           | SI trade with standard settlement

                                                                                                          |
| 246

                           | SI trade with non-standard settlement

                                                                                                      |
| 248

                           | Non-price forming trade

                                                                                                                    |
| 300

                           | Auction on Demand trade

                                                                                                                    |
| 301

                           | Trade at closing price

                                                                                                                     |
| 32

                            | Off-book trade [until 20100205]

                                                                                                            |
| 52

                            | Exercise Related trade [until 20231231]

                                                                                                    |
| 64

                            | Off-book trade with standard settlement

                                                                                                    |
| 65

                            | Routed trade

                                                                                                                               |
| 69

                            | Exchange Granted trade

                                                                                                                     |
| 75

                            | Contingent trade

                                                                                                                           |
| 76

                            | Beneficial ownership transfer [until 20231231]

                                                                                             |
| 80

                            | Portfolio trade

                                                                                                                            |
| 82

                            | Off-book trade with non-standard settlement

                                                                                                |
| 84

                            | Pre-opening trade

                                                                                                                          |
| 86

                            | VWAP trade

                                                                                                                                 |
# UPDATE_TYPE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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

