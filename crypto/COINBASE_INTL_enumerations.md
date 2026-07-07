# Coinbase - International Exchange Enumerations

Coinbase International Exchange is a platform launched in May 2023 for non-US institutional users to trade perpetual futures. It offers regulated, high-volume trading of crypto derivatives to eligible international users, supporting bitcoin and ether perpetuals. It was established to expand crypto derivatives globally outside the U.S.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* TRADE_VENUE - Identifies the venue where a trade was executed.   Typically a MIC, with the special values “XOFF” for off-exchange and “SINT” for Systematic Internaliser trades.

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| B                | Buy                       |
| S                | Sell                      |

#### TRADE_VENUE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| COINBASEINTL     | COINBASE International    |

