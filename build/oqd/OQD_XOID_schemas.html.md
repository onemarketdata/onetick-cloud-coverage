# Instrument Symbology Cross Reference from OID Schemas

Instrument Symbology Cross Reference from OID to Available Symbologies




## OQD_XOID

Database includes the following tick types:

* XREF - Symbology Mapping



### OQD_XOID - XREF

Symbology Mapping

#### OQD_XOID - XREF Table Schema

| Field        | Data Type   | Description                                                                                                 |
|--------------|-------------|-------------------------------------------------------------------------------------------------------------|
| DELETED_TIME | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).            |
| END_DATE     | msectime    | Calendar Event End Date, or Last Valid Date                                                                 |
| EXCH         | string[10]  | Exchange from which the update originates (Country Code + [MIC or PRIM for Primary, or COMP for Composite]) |
| ID_SYMBOL    | string[32]  | Symbology Code                                                                                              |
| ID_TYPE      | string[5]   | XREF                                                                                                        |
| TICK_STATUS  | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                |
