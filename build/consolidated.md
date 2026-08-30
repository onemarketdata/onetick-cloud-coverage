# Consolidated Fragmented Liquidity

Fragmented liquidity from multiple markets are combined into a single databased per region.
For the US Market the content is sourced from the US Consolidated Tape, the US SIP (CTA + UTP).
This provides both the Trades and Quotes for each Exchange, plus the NBBO.
From the 1st June 2026, the data also includes additional tables for Quotes and NBBO includind Odd Lot Quotes.

Other countries / regions also have fragmented liquidity, but do not provide a consolidated tape.
OneTick creates this consolidated tape for Australia, Canada, Europe including UK, India, Japan, Korea, Mexico, and Taiwan.
This includes providing a single database to store all trades and quotes across all exchanges
and also creating a NBBO for these markets.  In the case of Canada producing the CBBO, and in the case of Europe the EBBO.
The DAY table for Consolidated databases provides both the consolidated daily Open, High, Low, Close and Volume  (OHLCV) for each symbol, and also by each exchange.

Additionally includes curated datasets, where key products are combined from multiple markets

It covers:

* `AU_COMP` - Australian Consolidated Equities
* `CA_COMP` - Canadian Consolidated Equities (all Trades, Quotes, NBBO)
* `EU_COMP` - European Consolidated Equities
* `IN_COMP` - India Consolidated Equities
* `JP_COMP` - Japan Consolidated Equities
* `KR_COMP` - Korea Consolidated Equities
* `MX_COMP` - Mexico Consolidated Equities
* `TDI_FUT` - Global Futures
* `TDI_IDX` - Global Indices
* `TW_COMP` - Taiwan Consolidated Equities
* `US_COMP` - US Consolidated Equities (exc. OTC)
* `US_SHORT_INT` - FINRA - US Equities Short Interest / Short Volume
