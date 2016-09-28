# IonTorrentReport


This is a work in progress repository.

ParseTab and ParseTabAlt are python modules that allows for easy parsing of either xls or tsv files.

LRT_database.py and concatenate_safir (which may be kinda the same) is my working script that helped me to import data to create a flat file variant database in order to classify automatically variants
The format of this database is the following:

chromosome TAB position TAB refNuc TAB altNuc TAB Panel TAB BiologistName TAB ClinicalAnnotation TAB LastUpdate

If you are having trouble with this, just let me know and I will forge a file (I cannot give you the original file since this is sensitive data)

xml files are designed for galaxy

Please note that LRT stands for Laboratoire de Recherche Translationelle. It also isn't a real name.


As for now, at Gustave Roussy, we use Safir_Report-2.3.py in combination with LRT_database.py. 

Biologist uploads its variant xls file into galaxy. It gets annotated. He/She reviews it and annotated the variants. Annotated file (3rd column) is reuploaded into "Update clinical annotation database for Safir report" tool.
DB is updated. Next time all variants that have been annotated will get annotated again.



Please note: I am currently developping a webapp that leverages Safir_Report-2.3.py, which renders this version practically obsolete. It is kinda heavy. 



Recommandations for use:

Please tell me what you would like the application to be, and I will try to arrange that for you. Pull Requests are welcomed ! 
