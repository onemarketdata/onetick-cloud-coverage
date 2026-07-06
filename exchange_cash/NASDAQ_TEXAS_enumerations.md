# Nasdaq Texas Enumerations

Nasdaq Texas is a U.S. national securities exchange and dual-listing venue headquartered in Dallas. Operated by Nasdaq, Inc., it allows publicly traded companies to maintain a concurrent listing on a Texas-domiciled exchange while trading under their existing ticker symbol, with no new compliance burdens

The following fields have Enumerations:


* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.


* TRADE_TYPE - Type of trade


* TRADE_TYPE_EXT - Extended trade type code


* ODD_LOT - Indicates whether a trade was an odd lot


* TRADE_PERIOD - Market period during which a trade was executed.


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* RPI - Indicates the presence of Retail Price Improvement interest on bid and/or ask side


* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue


* REASON_CODE - Reason for an instrument status update


* SHORT_SALE_RESTRICTION - Indicates whether short selling is permitted


* PART_TYPE - Indicates the type of market participant identified by PART_ID


* FINANCIAL_STATUS - Indicates the regulatory status of a security or its issuer


* UPDATE_TYPE - Type of update


* ORDER_TYPE - Type of order.

# AGGRESSOR_SIDE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
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
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| ‘””’

                          | Regular trade

                                                                                                                              |
| H

                             | Regular trade against hidden liquidity

                                                                                                     |
# TRADE_TYPE_EXT - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| ‘””’

                          | Unspecified [for future use]

                                                                                                               |
# ODD_LOT - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Y

                             | Odd lot

                                                                                                                                    |
| ‘””’

                          | Round lot

                                                                                                                                  |
# TRADE_PERIOD - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| 0

                             | Lit order book

                                                                                                                             |
# RPI - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| C

                             | End of day

                                                                                                                                 |
| E

                             | End of system hours

                                                                                                                        |
| H

                             | Halted

                                                                                                                                     |
| O

                             | Start of day

                                                                                                                               |
| T

                             | Trading

                                                                                                                                    |
# REASON_CODE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| ‘””’

                          | Unspecified

                                                                                                                                |
| C3

                            | Issuer news not forthcoming, quotation / trading to resume

                                                                                 |
| C4

                            | Listing requirements met, quotation / trading to resume

                                                                                    |
| C9

                            | Filings met, quotation / trading to resume

                                                                                                 |
| C11

                           | Halt concluded by other regulatory authority, quotation / trading to resume

                                                                |
| H4

                            | Non-compliance with listing requirements

                                                                                                   |
| H9

                            | Filings not current

                                                                                                                        |
| H10

                           | SEC trading suspension

                                                                                                                     |
| H11

                           | Regulatory concern

                                                                                                                         |
| IPO1

                          | IPO issue not yet trading

                                                                                                                  |
| IPOE

                          | Positioning window extension for IPO security

                                                                                              |
| IPOQ

                          | IPO security released for quotation

                                                                                                        |
| LUDP

                          | Volatility trading pause

                                                                                                                   |
| LUDS

                          | Volatility trading pause (straddle condition)

                                                                                              |
| M1

                            | Corporate action

                                                                                                                           |
| M2

                            | Quotation not available

                                                                                                                    |
| MWC0

                          | Market-wide circuit breaker (MWCB) carried over from previous day

                                                                          |
| MWC1

                          | MWCB level 1 breached

                                                                                                                      |
| MWC2

                          | MWCB level 2 breached

                                                                                                                      |
| MWC3

                          | MWCB level 3 breached

                                                                                                                      |
| MWCQ

                          | MWCB resumption

                                                                                                                            |
| O1

                            | Halted by Market Operations

                                                                                                                |
| R1

                            | New issue available

                                                                                                                        |
| R2

                            | Issue available

                                                                                                                            |
| R4

                            | Qualification issues reviewed / resolved, quotation / trading to resume

                                                                    |
| R9

                            | Filing requirements satisfied / resolved, quotation / trading to resume

                                                                    |
| T1

                            | News pending

                                                                                                                               |
| T2

                            | News disseminated

                                                                                                                          |
| T3

                            | News disseminated, quotation / trading to resume

                                                                                           |
| T5

                            | Trading pause

                                                                                                                              |
| T6

                            | Extraordinary market activity

                                                                                                              |
| T7

                            | Quotation only period

                                                                                                                      |
| T8

                            | ETF halt

                                                                                                                                   |
| T12

                           | Information requested by Nasdaq

                                                                                                            |
# SHORT_SALE_RESTRICTION - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| ‘””’

                          | Unspecified

                                                                                                                                |
| 0

                             | No short selling restriction

                                                                                                               |
| 1

                             | Short selling restriction in effect

                                                                                                        |
# PART_TYPE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| L

                             | Penalty

                                                                                                                                    |
| N

                             | Normal

                                                                                                                                     |
| P

                             | Passive

                                                                                                                                    |
| R

                             | Pre-syndicate

                                                                                                                              |
| S

                             | Syndicate

                                                                                                                                  |
# FINANCIAL_STATUS - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| ‘””’

                          | Unspecified

                                                                                                                                |
| C

                             | Creation / redemption suspended (ETPs)

                                                                                                     |
| D

                             | Deficient

                                                                                                                                  |
| E

                             | Delinquent

                                                                                                                                 |
| G

                             | Deficient + bankrupt

                                                                                                                       |
| H

                             | Deficient + delinquent

                                                                                                                     |
| J

                             | Delinquent + bankrupt

                                                                                                                      |
| K

                             | Deficient + delinquent + bankrupt

                                                                                                          |
| N

                             | Normal

                                                                                                                                     |
| Q

                             | Bankrupt

                                                                                                                                   |
| S

                             | Suspended

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

                                                                                                                               |
# ORDER_TYPE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| L

                             | Limit order

