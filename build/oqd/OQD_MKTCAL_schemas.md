# Historic Market Holiday Calendar and Trading Hours Schemas

Historic Market Holiday Calendar and Trading Hours




## OQD_MKTCAL

Database includes the following tick types:

* MKTCAL - Market Calendar



### OQD_MKTCAL - MKTCAL

Market Calendar

#### OQD_MKTCAL - MKTCAL Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTIVITY_NAME | string[40]  | Activity Type including Holidays and Trading Sessions                                                                                                                                                                                  |
| CALENDAR_NAME | string[40]  | Calendar Name                                                                                                                                                                                                                          |
| DELETED_TIME  | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| END_DATE      | msectime    | Calendar Event End Date, or Last Valid Date                                                                                                                                                                                            |
| END_TIME      | string[10]  | Calendar Event End Time                                                                                                                                                                                                                |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| START_DATE    | msectime    | Calendar Event Start Date                                                                                                                                                                                                              |
| START_TIME    | string[10]  | Calendar Event Start Time                                                                                                                                                                                                              |
| TICK_STATUS   | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TIME_ZONE     | string[40]  | Time Zone                                                                                                                                                                                                                              |
| WEEKDAYS      | int         |                                                                                                                                                                                                                                        |
