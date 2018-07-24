# Pakistan 2018 General Elections Candidate Registry

This repository hosts manually-transcribed final candidate lists for Pakistan's 2018 general elections in a machine-readable csv format. Following initial candidate filings and a process of scrutiny, disqualifiation, and candidate withdrawals, the Election Commission of Pakistan [released final candidate lists for national and provincial assembly constituencies](https://www.ecp.gov.pk/frmGenericPage.aspx?PageID=3160) on July 4, 2018. The following day the ECP amended those lists to include some missing Punjab constituency lists that were initially described as having been withheld due to pending legal cases.

The [data folder](https://github.com/colincookman/pakistan_candidate_registry_18/tree/master/data) contains the original raw pdfs released by the ECP; these have been renamed for identification purposes but are otherwise unchanged.

As of the initial commit we have only processed the national assembly constituencies and have not completed work on provincial assembly lists. These will be updated as we are able to, or otherwise generated from final results lists.

For questions, suggestions, or to contribute, please leave an issue here or contact the contributors, Colin Cookman and Mohammad Zohaib.

## File descriptions

* [pk_candidate_registry_2018.csv](https://github.com/colincookman/pakistan_candidate_registry_18/blob/master/pk_candidate_registry_2018.csv) is the transcribed final candidate lists (currently national assembly only).
* [pk_constituency_candidate_count_2018.csv](https://github.com/colincookman/pakistan_candidate_registry_18/blob/master/pk_constituency_candidate_count_2018.csv) is a count of the number of candidates per constituency.
* [pk_party_candidate_count_2018.csv](https://github.com/colincookman/pakistan_candidate_registry_18/blob/master/pk_party_candidate_count_2018.csv) is a count of the number of candidates per party, per province.
* [pk_party_list_2018.csv](https://github.com/colincookman/pakistan_candidate_registry_18/blob/master/pk_party_list_2018.csv) is a reference key file generated from the [ECP's list of registered parties and election symbols](https://www.ecp.gov.pk/frmGenericPage.aspx?PageID=3090).

## Caveats and gaps in the data

The [ECP's own totals for the aggregate final number of contesting candidates](https://www.ecp.gov.pk/PrintDocument.aspx?PressId=55349&type=Image), released on July 2 2018, do not match our own total count. In the absence of other final lists below the provincial aggregate level, we cannot currently account for the discrepancy.

| Province                    	| ECP NA General Seat Count 	| Transcribed Count 	| Difference 	|
|-----------------------------	|---------------------------	|-------------------	|------------	|
| Balochistan                 	| 287                       	| 288               	| 1          	|
| KPK                         	| 725                       	| 709               	| -16        	|
| Punjab (includes Islamabad) 	| 1623                      	| 1634              	| 11         	|
| Sindh                       	| 824                       	| 822               	| -2         	|

Although nominally "final", higher appeals courts continue to hear challenges to candidate eligibility and as of July 13 the ECP [had halted the finalization of ballot printing](https://tribune.com.pk/story/1756643/1-ballot-papers-108-seats-not-yet-printed/) for at least 108 constituencies (national and provincial) pending the resolution of those challenges. Some candidates also continue to withdraw, and in at least two cases candidates have been killed in pre-election violence. Thus actual final candidate lists, when released as part of final results reporting after election day, may vary from this list.

Note that because Pakistani election law allows candidates to contest multiple constituencies simultaneously (albeit only serving from one), candidate names and serial number rankings are not unique identifiers across the entire dataset. Per the ECP forms, candidates are meant to be listed within each constituency in Urdu alphabetical order, although we cannot verify the consistent application of that sorting.

Due to poor quality scans of the raw pdfs, 18 candidate names were illegible and could not be transcribed; several addresses were also illegible, and 19 party affiliations could not be ascertained. Some names were not transliterated from Urdu to English on the ECP pdfs, which we converted as part of the transcription process; these may not match final ECP renderings of those names in English, however. One page of data for the NA-47 constituency (covering candidate serial numbers 14-26) was missing from the scanned pdfs released by ECP.

Candidate address formats are not standardized across constituencies, and in most cases do not appear to represent unique residences; they are included here to allow for possible visual checks to evaluate candidate unique IDs across constituencies, although we cannot guarantee that candidate addresses for candidates contesting in multiple constituencies match precisely. Our transcription of the address data is also in most cases not precise to the ECP original.

## Additional data and plans for expansion

This dataset is a work in progress and caution is advised when using it. Corrections of errors or contributions to the provincial assembly lists are greatly appreciated.

The [Pakistan 2018 General Elections Candidate Scrutiny Forms](https://github.com/colincookman/pakistan_candidate_scrutiny_18) repository collects initial candidate filing and scrutiny data, as well as 2016 incumbency status. Joining this data with the final list here should allow for tracking candidate withdrawals and disqualifications prior to the elections, but may require manual matching due to non-standardized Urdu name transliterations and the absence of other unique identifiers.

