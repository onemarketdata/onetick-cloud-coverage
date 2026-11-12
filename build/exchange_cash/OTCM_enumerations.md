# OTC Markets (US OTC Quotes) Enumerations

Quotes, trades, bars and book depth from OTC Markets Group’s OTC Link ATS, an SEC-registered alternative trading system, with history from July 2018, covering about 12,000 US and international securities on the OTCQX, OTCQB, OTCID and Pink markets. It is the main source for US OTC quotes, including many ADRs and foreign ordinary shares of large non-US companies.

The following fields have Enumerations:

* IS_OPEN - Indicates whether a market maker is “open”, i.e. whether their quotes are active (1) or inactive (0)
* IS_UNSOLICITED - An unsolicited quote is a quote that a dealer was asked to post by one of their clients, generally for an illiquid / distressed security that would not normally be quoted.
* UPDATE_TYPE - Type of update
* QUOTE_COND - Indicates any special conditions applicable to a quote

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

#### QUOTE_COND - Enumeration

| Enumeration ID   | Enumeration Description                                                            |
|------------------|------------------------------------------------------------------------------------|
| ‘””’             | Regular quote                                                                      |
| S                | Saturated quote [participant is unresponsive, quote excluded from the overall BBO] |

