# Exiftool

% exiftool, forensics, cpts

## Exiftool - Exiftool - Exiftool - Exiftool - xss
#cat/POSTEXPLOIT #cpts
Many file types may allow us to introduce a `Stored XSS` vulnerability to the web application by uploading maliciously crafted versions of them. The most basic example is when a web application allows us to upload `HTML`

```
exiftool -Comment=' ">' HTB.jpg
```

## Exiftool - Exiftool - Exiftool - Exiftool - xss-2
#cat/POSTEXPLOIT #cpts
Many file types may allow us to introduce a `Stored XSS` vulnerability to the web application by uploading maliciously crafted versions of them. The most basic example is when a web application allows us to upload `HTML`

```
exiftool HTB.jpg
```

## Exiftool - Exiftool - Exiftool - Exiftool - rce
#cat/POSTEXPLOIT #cpts
```
exiftool -Comment="" image.jpg -o polyglot.php
```

