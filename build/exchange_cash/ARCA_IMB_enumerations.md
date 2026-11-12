# ARCA Auction Imbalance Data Enumerations

Opening and closing auction imbalance messages for NYSE Arca, with history from August 2025 and real-time data available. Each message reports paired shares, imbalance size and side and indicative match prices ahead of the auction, which matters most for ETFs because NYSE Arca is the main listing venue for US exchange-traded products.

The following fields have Enumerations:

* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
  : “A”,”Unspecified auction”
    “C”,”Closing auction”
    “I”,”Intraday auction”
    “O”,”Opening auction”
    “P”,”IPO / Public offering auction”
    “S”,”Settlement (EDSP) auction”
    “U”,”Unscheduled auction”
    “c”,”Post-close auction”
    “o”,”Opening auction (extended hours)”
    “p”,”Auction initiated by market participant”
    “u”,”Unscheduled auction (extended hours)”


