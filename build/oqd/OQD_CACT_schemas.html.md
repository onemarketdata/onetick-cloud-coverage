# Global Corporate Actions History Schemas

Global Corporate Actions History




## OQD_CACT

Database includes the following tick types:

* CACS - Corporate Actions for Security
* CACT - Corporate Actions for All Securities



### OQD_CACT - CACS

Corporate Actions for Security

#### OQD_CACT - CACS Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTION_ADJUST    | double      | Corporate Action Adjustment Factor                                                                                                                                                                                                     |
| ACTION_CURRENCY  | string[4]   | Currency for Corporate Action Payment                                                                                                                                                                                                  |
| ACTION_ID        | int         | Corporate Action Identifier                                                                                                                                                                                                            |
| ACTION_STATUS    | string[20]  | Corporate Action Status                                                                                                                                                                                                                |
| ACTION_TYPE      | string[20]  | Corporate Action Type                                                                                                                                                                                                                  |
| ANN_DATE         | int         | Corporate Action Annoucement Date                                                                                                                                                                                                      |
| DELETED_TIME     | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| EX_DATE          | int         | Corporate Action Ex Date                                                                                                                                                                                                               |
| OID              | string[14]  | OneMarketData ID                                                                                                                                                                                                                       |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PAY_DATE         | int         | Corporate Action Payment Date                                                                                                                                                                                                          |
| REC_DATE         | int         | Corporate Action Record Date                                                                                                                                                                                                           |
| TERM_NOTE        | string[99]  | Description of Payment Terms                                                                                                                                                                                                           |
| TERM_RECORD_TYPE | string[10]  | Term Record Type                                                                                                                                                                                                                       |
| TICK_STATUS      | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |

### OQD_CACT - CACT

Corporate Actions for All Securities

#### OQD_CACT - CACT Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTION_ADJUST   | double      | Corporate Action Adjustment Factor                                                                                                                                                                                                     |
| ACTION_CURRENCY | string[4]   | Currency for Corporate Action Payment                                                                                                                                                                                                  |
| ACTION_DATE     | int         | Corporate Action End Date                                                                                                                                                                                                              |
| ACTION_ID       | int         | Corporate Action Identifier                                                                                                                                                                                                            |
| ACTION_TYPE     | string[20]  | Corporate Action Type                                                                                                                                                                                                                  |
| DELETED_TIME    | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| OID             | string[14]  | OneMarketData ID                                                                                                                                                                                                                       |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| TICK_STATUS     | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
