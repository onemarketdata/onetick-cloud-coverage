# FINRA TRACE - Corporates, Agencies, MBS, ABS, CMO Enumerations

The Trade Reporting and Compliance Engine (TRACE) is the FINRA-developed vehicle that facilitates the mandatory reporting of over-the-counter transactions in eligible fixed income securities. All broker-dealers who are FINRA member firms have an obligation to report transactions in TRACE-eligible securities under an SEC-approved set of rules.

The following fields have Enumerations:

* PRICE_COND - Identifies trade prices that are special / unconfirmed / potentially suspect / notable for other reasons
* SIZE_TYPE - Indicates any special conditions applicable to the SIZE field
* TRADE_TYPE - Type of trade
* LATE_REPORTED - Indicates whether a trade was reported late and/or outside normal trading hours
* TRADE_PERIOD - Market period during which a trade was executed.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* REPORTING_PARTY_SIDE - Indicates whether the trade was reported by the buyer or the seller (“B” - Buyer, “S” - Seller, “” - Unspecified)
* REPORTING_PARTY_TYPE - Type of participant that reported the trade
* CONTRA_PARTY_TYPE - Type of participant that the trade was executed against (on the other side from the reporting party)
* ATS_INDICATOR - Indicates whether an ATS was involved in the execution or publication of the trade (“Y” - Yes, “” - No / Unspecified)

#### PRICE_COND - Enumeration

| Enumeration ID   | Enumeration Description              |
|------------------|--------------------------------------|
| C                | Trade price includes commission      |
| M                | Trade price includes markup/markdown |
| S                | Special price                        |
| ‘””’             | No condition                         |

#### SIZE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| E                | Estimated size            |
| ‘””’             | Actual size               |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description         |
|------------------|---------------------------------|
| D                | Dollar roll without stipulation |
| L                | Dollar roll with stipulation    |
| N                | Stipulation                     |
| O                | Specified pool transaction      |
| P                | Portfolio trade                 |
| W                | Weighted average price          |
| ‘””’             | No condition                    |

#### LATE_REPORTED - Enumeration

| Enumeration ID   | Enumeration Description              |
|------------------|--------------------------------------|
| A                | Trade reported late on an As-Of basi |
| R                | Reversal of an earlier trade         |
| T                | Outside hours                        |
| U                | Out of sequence and outside hours    |
| Z                | Out of sequence                      |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| e                | Extended hours            |
| -                | Regular trading           |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                9 | Off-exchange              |

#### REPORTING_PARTY_SIDE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| B                | Reported by the buyer     |
| S                | Reported by the seller    |

#### REPORTING_PARTY_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| D                | Broker/dealer             |
| T                | ATS                       |

#### CONTRA_PARTY_TYPE - Enumeration

| Enumeration ID   | Enumeration Description    |
|------------------|----------------------------|
| A                | Non-FINRA member affiliate |
| C                | Customer                   |
| D                | Broker/dealer              |
| T                | ATS                        |

#### ATS_INDICATOR - Enumeration

| Enumeration ID   | Enumeration Description                                            |
|------------------|--------------------------------------------------------------------|
| Y                | An ATS was involved in either executing or reporting the trade     |
| ‘””’             | An ATS was not involved in either executing or reporting the trade |

