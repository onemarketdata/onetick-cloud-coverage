# Nasdaq Auction Imbalance Data Enumerations

Opening and closing cross imbalance data (Net Order Imbalance Indicator, NOII) for the Nasdaq Stock Market, with history from January 2020 and real-time data available. Messages report paired shares, imbalance quantity and side, and near and far indicative clearing prices ahead of the Nasdaq Opening and Closing Crosses, which set official opening and closing prices for Nasdaq-listed stocks.

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


