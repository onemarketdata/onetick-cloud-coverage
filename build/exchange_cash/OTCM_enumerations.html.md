# OTC Markets (US OTC Quotes) Enumerations

OTC Markets operates trading platforms for over 10,000 OTC securities in the US public and private markets.

The following fields have Enumerations:

* IS_OPEN - Indicates whether a market maker is “open”, i.e. whether their quotes are active (1) or inactive (0)
* IS_UNSOLICITED - An unsolicited quote is a quote that a dealer was asked to post by one of their clients, generally for an illiquid / distressed security that would not normally be quoted.
* UPDATE_TYPE - Type of update

#### IS_OPEN - Enumeration

|   Enumeration ID | Enumeration Description              |
|------------------|--------------------------------------|
|                0 | Closed quote (market maker inactive) |
|                1 | Open quote                           |

#### IS_UNSOLICITED - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Standard quote            |
|                1 | Unsolicited quote         |

#### UPDATE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                1 | Quote deletion            |
|                2 | Quote update              |
|                3 | New quote                 |
|                4 | Start of day quote        |
|                5 | Open/Close quote          |

