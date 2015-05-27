# Introduction #

Database schema matching is the process of establishing correspondences between the attributes of schemas, for the purpose of data integration. Various commercial and academic schema matching tools have been developed to support this task. These tools achieve impressive performance on some datasets. However, as the matching is inherently uncertain, the developed heuristic techniques yield to results that are not completely correct. In practice, therefore, there is a reconciliation process in which post-matching human effort is needed to obtain a correct set of attribute correspondences. We study this reconciliation phase, and develop techniques to reduce the necessary user interactions in this reconciliation process, by exploiting the network context in which the schema is embedded. In particular, we demonstrate how to express network-level matching constraints in a declarative formalism, in Answer Set Programming, and we propose techniques that support and guide human users in the reconciliation process. Our experiments show that in this way we can indeed reduce the necessary efforts in terms of user interaction steps.


# Data Sets #

# [Business Partner](http://lsirwww.epfl.ch/schema_matching/download/bp_schemata.zip): The Business Partner dataset is a catalogue of Web services available in SAP Enterprize Resource Planing (ERP) system, [SAP ESW](http://esworkplace.sap.com/) and the service inputs/outputs parameters are defined using Global Data Types (GDTs) of SAP. This dataset consists of 3 schemas, where each schema has around 80 attributes and 3 levels of hierarchy.

# [Purchase Order](http://lsirwww.epfl.ch/schema_matching/download/po_schemata.zip): We collected, extracted and normalized purchase order e-business documents from various resources, including [COMA](http://dbs.uni-leipzig.de/Research/coma.html) evaluations, [openTRANS](http://www.opentrans.de), [xCBL](http://www.xcbl.org/), [RosettaNet](http://www.rosettanet.org/), etc.

# [University Application Forms](http://lsirwww.epfl.ch/schema_matching/download/uaf_schemata.zip): We collected and extracted XML schemas representing the web interface of American universities' application forms.
Although we visited around 50 university websites, we obtained only 15 schemas since most of them use the same platforms ([CommonApp](https://www.commonapp.org)}, [UniversalApp](https://www.universalcollegeapp.com), [Embark](http://www.embark.com), and [CollegeNet](http://www.collegenet.com/elect/app/app).

# [Web Forms](http://lsirwww.epfl.ch/schema_matching/download/webform_data.zip): The schemas for this dataset have been automatically extracted from Web forms using [OntoBuilder](http://ontobuilder.bitbucket.org). They cover seven different domains (e.g., betting and book shops).

# [Google Fusion Tables](http://lsirwww.epfl.ch/schema_matching/download/gtf_data.zip): extracted from [Google Fusion Tables homepage](http://www.google.com/drive/apps.html#fusiontables)