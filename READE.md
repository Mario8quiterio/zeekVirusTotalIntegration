# Purpose
Check file hashes of specific mime type files with Virus Total creating a zeek log if AV hits is greater than x. 

# Installation
- Add VT folder your to equivalent opt/zeek/share/zeek/policy
- Make sure to load the two scripts on site/local.zeek
  - see local.zeek for example
- Add your virus total API to virus-total.zeek on line 20
- Change log file name created by zeek in virus-total.zeek line 36
- Change what mime types to trigger file hash checker in vt-hashing.zeek line 18; 
  - **const match_file_types =**
- Change threshold for AV hits in vt-hashing.zeek; 
  -  **const hits_to_notice = 0 &redef**
