# FragmentInference
This project infers past application activity given an image of a hard drive. The code relies on a pre-built catalog of artifact fragments (actually sector hashes) that are associated with one or more applications. This catalog is included under the Hashdb section. See the Docs for more information on applications in the catalog.

# Requirements
The code was developed and tested under Ubuntu 12.04.3 LTS and requires the following:
  - hashdb v1.0.0-beta2
  - hashdb v1.1.2
  - md5deep v4.4
  - Python 3.x
 
# Usage
$ python3 process_img.py option image_base
  where image_base is the original img filename (without extension)
  and options are:
    -i: start with a raw img file (dd format or similar)
    -m: start with a raw md5 hashes file (produced by md5deep)
    -d: start with an md5 DFXML file (produced by md5deep -d)
    -p: start with a .matches file (produced by hashdb)
  Starting with -i implies all subsequent steps (-m, -d, and -p), starting with -m implies -d and -p as well, etc.

# Acknowledgement and Disclaimer
This work results from research supported by the Naval Postgraduate School Assistance Grant/Agreement No. N00244-13-1-0034 awarded by the NAVSUP Fleet Logistics Center San Diego (NAVSUP FLC San Diego). The views expressed in written materials or publications, and/or made by speakers, moderators, and presenters, do not necessarily reflect the official policies of the Naval Postgraduate School or the National Institute of Standards and Technology, nor does mention of trade names, commercial practices, or organizations imply endorsement by the U.S. Government.

