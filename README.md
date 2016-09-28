# IonTorrentReport


This is a work in progress repository.

## 1) Description

Currently, Safir_report is at its 2.4 release.

ParseTab and ParseTabAlt are python modules that are providing some interface that won't care about the file being TSV or XLS.

LRT_database.py is a working script that helped me to import data to create a flat file variant database in order to classify automatically variants
The format of this database is the following:

old_versions speaks for itself

## 2) Files

Before doing anything, you need to edit Safir_report python program and provide path at the beggining of the file. 
You will need SnpSift, Snpeff ( snpeff.sourceforge.net ), dbNSFP, dbSNP, ESP, 1000Genome, and a tabix-indexed custom database file (if you do not have any, you should either index some empty file, or remove all references in code)

The custom database has the following scheme: 
	`<chromosome>TAB<position>TAB<refNuc>TAB<altNuc>TAB<Panel>TAB<BiologistName>TAB<ClinicalAnnotation>TAB<LastUpdate>`

If you are having trouble with this, just let me know and I will forge a file (I cannot give you the original file since this is sensitive data)

## 3) Usage

XML files are designed for Galaxy. 

Biologist uploads its variant xls file into galaxy. It gets annotated. He/She reviews it and annotated the variants. Annotated file (3rd column) is reuploaded into "Update clinical annotation database for Safir report" tool.
DB is updated. Next time all variants that have been annotated will get annotated again.

As for now, at Gustave Roussy, we use Safir_Report-2.4.py in combination with LRT_database.py.

## 4) Names

Please note that LRT stands for Laboratoire de Recherche Translationelle. Also, SAFIR is the name of the clinical trial the tool has been developped for. We do not have a fixed idea on the name right now, so you may call it however you'd like to, but keep in mind it may change.

## 5) Evolution

Please tell me what you would like the application to be, and I will try to arrange that for you. Pull Requests are welcomed ! 

## 6) Author

Yannick Boursin ( yannick.boursin@gustaveroussy.fr )
Engineer at the Bioinformatics core at Gustave Roussy (BiGR)
