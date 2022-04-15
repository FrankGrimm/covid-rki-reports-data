# machine readable COVID-19 daily reports for Germany

Some crucial information on the COVID-19 situation in Germany is only available in PDF reports by the [Robert Koch Institute](https://github.com/robert-koch-institut/), this repository is an attempt to make some of this data more easily digestible.

## daily situation reports (archives)

Data extracted from German [RKI](https://www.rki.de) daily report archives, available at:
- [2020](https://www.rki.de/DE/Content/InfAZ/N/Neuartiges_Coronavirus/Situationsberichte/Archiv_2020_tab.html) 
- [2021](https://www.rki.de/DE/Content/InfAZ/N/Neuartiges_Coronavirus/Situationsberichte/Archiv_2021_tab.html) 
- [2022](https://www.rki.de/DE/Content/InfAZ/N/Neuartiges_Coronavirus/Situationsberichte/Archiv_2022_tab.html) (as far as they were available at the time of extraction)

All folders contain [pdftotext](https://pypi.org/project/pdftotext/) results for English (`text_en.txt`) (when available) and German (`text_de.txt`) reports, as well as tables extracted with [camelot](https://pypi.org/project/camelot-py/) (using `stream` mode). **Note**: Table extraction is imperfect, it may unnecessarily split, create, and/or miss tables or rows. If you need to extract specific tables in a robust manner you might need to run and tune the extraction yourself.

## weekly reports (2022)

Data in `extracted_weekly` is extracted via `pdftotext` from PDFs available from the [RKI](https://www.rki.de/DE/Content/InfAZ/N/Neuartiges_Coronavirus/Situationsberichte/Wochenbericht/Wochenberichte_Tab.html).

*Note*: `extracted_weekly_tables` contains isolated table data from the reports **without** preprocessing. Most of these will contain some metadata (such as additional header rows) and none of them are properly aligned with the identified header rows yet. Use with caution.
