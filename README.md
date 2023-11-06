# findmyhash
Hash cracking tool

Python written tool to help cracking hashes

Accepted algorithms:
MD4 - RFC 1320
MD5 - RFC 1321
SHA1 - RFC 3174 (FIPS 180-3)
SHA224 - RFC 3874 (FIPS 180-3)
SHA256 - FIPS 180-3
SHA384 - FIPS 180-3
SHA512 - FIPS 180-3
RMD160 - RFC 2857
GOST - RFC 5831
WHIRLPOOL - ISO/IEC 10118-3:2004
LM - Microsoft Windows hash
NTLM - Microsoft Windows hash
MYSQL - MySQL 3, 4, 5 hash
CISCO7 - Cisco IOS type 7 encrypted passwords
JUNIPER - Juniper Networks $9$ encrypted passwords
LDAP_MD5 - MD5 Base64 encoded
LDAP_SHA1 - SHA1 Base64 encoded


Valid options for usage

-h hash_value: If you only want to crack one hash, specify its value with this option.

-f file: If you have several hashes, you can specify a file with one hash per line.

NOTE: All of them have to be the same type.

-g: If your hash cannot be cracked, search it in Google and show all the results.

NOTE: This option ONLY works with -h (one hash input) option.


Some examples

Try to crack only one hash. python findmyhash.py MD5 -h "098f6bcd4621d373cade4e832627b4f6"

If the hash cannot be cracked, it will be searched in Google. python findmyhash.py SHA1 -h "A94A8FE5CCB19BA61C4C0873D391E987982FBBD3" -g

Try to crack all the hashes of a file (one hash per line). python findmyhash.py MYSQL -f mysqlhashesfile.txt

Note: This is copy of Google's hash cracking algorithm.
