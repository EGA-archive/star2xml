# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]


## [1.0.0] - 21-11-05
### Added
- [README.md](README.md) - README of the project, containing all the information related to the star2xml tool (usage, prerequisites, scripts...).
- LICENSE - License applied to the [star2xml](https://github.com/EGA-archive/star2xml) project.
- [star2xml.py](star2xml/star2xml.py) - Main wrapper (Python script) to call the project. Can either generate XMLs based on a given tabular input, or both create them and call the secondary wrapper [validateXML.py](star2xml/validateXML.py) to validate them.
- [validateXML.py](star2xml/validateXML.py) - Secondary wrapper (Python script) of the project. Will validate the given XMLs against the given XML schemas (.xsd files). 
- [requirements.txt](star2xml/requirements.txt) - Text file containing all required packages (with their teste versions) to run the project.
- [input_configuration.yaml](star2xml/configuration_files/input_configuration.yaml) - Configuration file (Yaml) containing the required fields (column names) that shall appear in the input file.
- [xml_schema.yaml](star2xml/configuration_files/xml_schema.yaml) - Configuration file (Yaml) containing general information about the project (e.g. ENA's GitHub) and the structure of each metadata object's XML, upon which [XML_creator.py](star2xml/XML_creator.py) will iterate to construct XMLs. 
- [Input_reader.py](star2xml/Input_reader.py) - Python script to transform given input file into a dataframe.
- [XML_creator.py](star2xml/XML_creator.py) - Python script to construct an XML based on the given input dataframe and the XML structure from [xml_schemas.yaml](star2xml/configuration_files/xml_schema.yaml). 
- [ftp_downloader.py](star2xml/ftp_downloader.py) - Python script with the required tools to download ENA's XML schemas (.xsd files) from their [FTP server](http://ftp.ebi.ac.uk/pub/databases/ena/doc/xsd/sra_1_6/).
- [git_downloader.py](star2xml/git_downloader.py) - Python script with the required tools to download ENA's XML schemas (.xsd files) from their [GitHub repository](https://github.com/enasequence/schema/tree/master/src/main/resources/uk/ac/ebi/ena/sra/schema).
- [scripts_for_validation.py](star2xml/scripts_for_validation.py) - Python script with the required tools to validate an XML against a given XML schema (.xsd file).
- [utils.py](star2xml/utils.py) - Python script with diverse functions used by other scripts (e.g. ``report_error_messages()``)
- Several images within [miscellaneous/](star2xml/miscellaneous/) to be referenced by star2xml's [README](star2xml/README.md).
- Two mock example XMLs ([``test_run.xml``](star2xml/test_data/XML_examples/test_run.xml) and [``test_sample.xml``](star2xml/test_data/XML_examples/test_sample.xml)) to check what the output of the tool could be.
