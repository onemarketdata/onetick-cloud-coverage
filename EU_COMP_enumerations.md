# European Consolidated Equities Enumerations

This is a consolidated feed providing trade data and best bid/offer across European equity markets, giving a unified view of the European equity landscape.

The following fields have Enumerations:


* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* MMT_ALGO_IND - Identifies whether a trade involved an algorithmic order.


* MMT_BENCHMARK_IND - Identifies whether a trade was priced according to a defined benchmark (e.g. VWAP) or reference price (e.g. midpoint of the primary market BBO), or whether it was part of a trade in multiple instruments (contingent trade or portfolio trade).


* MMT_CROSS_IND - Identifies agency cross trades, where a broker crossed two client orders outside the order book.


* MMT_DEFERRAL_TYPE - Type of publication deferral or subsequent enrichment applied to a trade report.


* MMT_DIVIDEND_IND - Identifies whether a trade includes special dividend arrangements, e.g. a trade sold cum-dividend during an ex-dividend period.


* MMT_DUP_IND - Identifies trades reported to more than one Approved Publication Arrangement.


* MMT_MKT_MECH - Market mechanism through which a trade was executed.


* MMT_MOD_IND - Identifies trade cancellations, or amendments of a previous trade.


* MMT_NEGOTIATED_IND - Indicates privately negotiated trades, or Systematic Internaliser trades exempt from pre-trade transparency.


* MMT_PRICE_FORMING_IND - Identifies whether a trade is price-forming, or contributes to the price discovery process.


* MMT_PUB_MODE - Identifies whether a trade was subject to delayed publication, and the reason for the deferral.


* MMT_TRANS_CAT - Identifies various special categories of trade.


* MMT_TRD_MODE - Trading period during which an on-book trade was executed, or origin of an off-book trade report (on-exchange / off-exchange / SI).


* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.


* TRADE_PERIOD - Market period during which a trade was executed.


* TRADE_TYPE - Type of trade

# AGGRESSOR_SIDE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| 0

                           | Lit order book

                                                                                                                    |
| 1

                           | Off-book

                                                                                                                          |
| 2

                           | Dark book

                                                                                                                         |
| 5

                           | Buy-in / Sell-out book

                                                                                                            |
| 6

                           | Auction book

                                                                                                                      |
| 9

                           | Off-exchange

                                                                                                                      |
| Q

                           | Quote-driven trading

                                                                                                              |
| R

                           | Request for Quote

                                                                                                                 |
| ‘””’

                        | Not applicable

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
| 6

                           | Reference price trade executed at the closing price

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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not a cross trade

                                                                                                                 |
| X

                           | Agency cross trade

                                                                                                                |
| M

                           | Matched principal trade

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
| J

                           | Volume omission trade for sovereign bonds

                                                                                         |
| K

                           | 4 weeks aggregated trade for sovereign bonds

                                                                                      |
| L

                           | Full details of earlier Volume Omission sovereign bond trade

                                                                      |
| M

                           | Full details of earlier Aggregated sovereign bond trade

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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| 5

                           | Periodic Auction

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
| 9

                           | Other

                                                                                                                             |
| -

                           | Not applicable (e.g. valuation trades)

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
| 7

                           | Large in Scale OTC trade brought onto a venue

                                                                                     |
| 8

                           | Negotiated trade with pre-trade transparency waiver

                                                                               |
| 9

                           | Large in Scale OTC trade in liquid instruments brought onto a venue

                                                               |
| a

                           | Large in Scale OTC trade in illiquid instruments brought onto a venue

                                                             |
| b

                           | Large in Scale OTC trade subject to conditions other than the current market price and brought onto a venue

                       |
| c

                           | Large in Scale OTC trade with pre-trade transparency waiver brought onto a venue

                                                  |
| N

                           | Negotiated trade

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
| Z

                           | Price is not applicable

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
| A

                           | Deferred publication (medium size liquid market)

                                                                                  |
| B

                           | Deferred publication (medium size illiquid market)

                                                                                |
| C

                           | Deferred publication (large size liquid market)

                                                                                   |
| D

                           | Deferred publication (large size illiquid market)

                                                                                 |
| E

                           | Deferred publication (very large size liquid market)

                                                                              |
| F

                           | Deferred publication (very large size illiquid market)

                                                                            |
| G

                           | Deferral for ETCs / ETNs / SFPs / emission allowances

                                                                             |
# MMT_TRANS_CAT - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not applicable

                                                                                                                    |
| D

                           | Dark trade

                                                                                                                        |
| G

                           | RFMD give-up trade

                                                                                                                |
| H

                           | Exchange for physical + RFMD give-up trade

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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| 1

                           | Auction

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
| 8

                           | Other

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

                           | On Demand auction

                                                                                                                 |
| U

                           | Unscheduled auction

                                                                                                               |
| -

                           | Not applicable

                                                                                                                    |
# OMD_STATUS - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| A

                           | Auction

                                                                                                                           |
| B

                           | Break / Pause

                                                                                                                     |
| C

                           | Closing auction

                                                                                                                   |
| D

                           | Delisted / Pending deletion

                                                                                                       |
| H

                           | Halted

                                                                                                                            |
| I

                           | Scheduled intraday auction

                                                                                                        |
| M

                           | Mandatory quoting period

                                                                                                          |
| N

                           | New instrument / Pre-listing

                                                                                                      |
| O

                           | Opening auction

                                                                                                                   |
| P

                           | Pre-market

                                                                                                                        |
| Q

                           | Indicative quoting period

                                                                                                         |
| R

                           | Off-book trade reporting

                                                                                                          |
| S

                           | Suspended

                                                                                                                         |
| T

                           | Continuous trading

                                                                                                                |
| U

                           | Unscheduled auction

                                                                                                               |
| c

                           | Closed

                                                                                                                            |
| i

                           | IPO / Public offering auction

                                                                                                     |
| n

                           | No market phase / Unspecified

                                                                                                     |
| o

                           | Order management

                                                                                                                  |
| p

                           | Post-market

                                                                                                                       |
| t

                           | Trading at last price

                                                                                                             |
# TRADE_PERIOD - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| A

                           | Auction

                                                                                                                           |
| C

                           | Closing Auction

                                                                                                                   |
| E

                           | Extended hours (early session)

                                                                                                    |
| I

                           | Intraday Auction

                                                                                                                  |
| L

                           | Extended hours (late session)

                                                                                                     |
| O

                           | Opening Auction

                                                                                                                   |
| P

                           | Public offering / buyback auction

                                                                                                 |
| T

                           | Trading at last price

                                                                                                             |
| U

                           | Unscheduled Auction

                                                                                                               |
| c

                           | Post-close auction

                                                                                                                |
| e

                           | Extended hours

                                                                                                                    |
| o

                           | Opening auction (extended hours)

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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                        | As for underlying venues

