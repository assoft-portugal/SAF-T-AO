# SAF-T AO

[![GitHub All Releases](https://img.shields.io/github/downloads/assoft-portugal/SAF-T-AO/total)](https://github.com/assoft-portugal/SAF-T-AO/releases)
[![GitHub issues](https://img.shields.io/github/issues-raw/assoft-portugal/SAF-T-AO)](https://github.com/assoft-portugal/SAF-T-AO/issues)
[![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/assoft-portugal/SAF-T-AO)](https://github.com/assoft-portugal/SAF-T-AO/releases)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/assoft-portugal/SAF-T-AO/blob/master/LICENSE)
[![Discussion](https://img.shields.io/badge/discussion-yammer-blue.svg)](https://www.yammer.com/assoft-members/#/threads/inGroup?type=in_group&feedId=17835940&view=all)

Official XSD from the Government of Angola for use in SAF-T AO.

> The Standard Audit File for Tax Purposes (SAF-T) is a standardized XML file used for exporting the accounting information of a company to the tax authorities. The file contains accounting data that can be exported from an original accounting system for a specific time period.
>
> The SAF-T file is based on a directive by the Organization for Economic Co-operation and Development (OECD).
>
> [Oracle, JD Edwards EnterpriseOne Applications OECD Standard Audit File for Tax Purposes (SAF-T) Localizations Implementation Guide](https://docs.oracle.com/cd/E16582_01/doc.91/e97460/ch_eu_saft_xml.htm#EOAST109).

## VAT implementation in Angola

The of VAT legislation will take effect starting in October 2019. This deadline applies to software billing solutions, SAF-T file, and invoicing rules:

- Software solutions must be compliance with the requirements of the new legal system in order to process sales documents, invoices and other fiscal documents in accord to the legal framework. This rule applies to all the subjects of the VAT scheme.
- Software creators must apply to a software certification program by the government which is mandatory.
- Starting from **1 January 2020** it will be mandatory to produce a monthly SAF-T file and send it to the government tax authorities.
- From 1 January 2020, all taxpayers with an annual turnover of more than AKZ 50,000,000 will be required to produce the above referred SAF-T files and use certified software.

## XML Validation

Unix users can use `xmllint` for validation.  Windows users can use a simple tool like [XmlPad](https://xmlpad-mobile.com/), although the command line xmllint can also be used.

### Installing xmllint

```bash
sudo apt install libxml2-utils
```

### XML validation against XSD

```bash
xmllint -schema schema.xsd file.xml --noout
```
