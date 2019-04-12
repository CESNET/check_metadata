# check_metadata
a nagios plugin to monitor metadata signature &amp; validity

The script is used by eduID.cz federation to monitor validity of XML signature on federation metadata and also validUntil field.

# usage
``./check_metadata -M METADATA_URL -C SIGNING_CERTIFICATE -S SUBJECT_OF_SIG_CRT -w VALIDITY_WARNING -c VALIDITY_CRITICAL``

Example
```
$ ./check_metadata -M https://mdx.eduid.cz/entities/eduid \
  -C metadata.eduid.cz.crt.pem
  -S DC=cz,DC=eduID,CN=metadata.eduID.cz -w 26 -c 22 ; echo $?
Valid until 2019-05-09T15:15:05Z
0
$
```
