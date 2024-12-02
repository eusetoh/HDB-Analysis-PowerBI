PowerBI Dashboard to view trend of Singapore Housing Development Board (HDB) Prices

Steps Undertaken
1.	Loaded 5 datasets from “https://data.gov.sg/collections/189/view” into PowerBI
2.	Dataset from 1990-1999 had error in loading as Block Number was parsed as Integer but some values contain alphabets (350A)
    a.	Changed data type of column into Text format to resolve
3.	Appended all 5 tables into a single table merged
    a.	Datasets all had identical data structures and shapes
    b.	Some datasets had “lease_commence_date” column which others did not – removed this column after appending
4.	Scraped Data from “https://www.citypopulation.de/en/singapore/cities/”
    a.	Used UPPER() to make Town format consistent with HDB data
    b.	Used IF() to convert the regions of Singapore into full form
    c.	Used conditional formatting to compare the data structure of the towns in both the HDB data and Population by Area Data
    d.	Force fit the Population by Area Data structure into HDB Data structure
        i.	Kallang/Whampoa = Kallang
        ii.	Central Area = Newton + Novena + Downtown Core + Singapore River + Tanglin
        iii.	Lim Chu Kang = Scraped separately from “https://www.citypopulation.de/en/singapore/admin/lim_chu_kang/40201__lim_chu_kang/”
    e.	Name final table town_population
5.	Import table into PowerBI
6.	Create one-to-many relationship between town of town_population and town of merged

Key Highlights
1.	Close to 1 million data entries analysed
2.	Data merging 
3.	Relational Database
4.	Excel Skills like VLOOKUP, Conditional Formatting
5.	Data Scraping
6.	PowerBI Proficiency (Power Query)
