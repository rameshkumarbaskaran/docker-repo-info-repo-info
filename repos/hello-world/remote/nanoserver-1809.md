## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:ec0e69c6cb2c401c53bedc9e24ecf0437f76799681dd42445b9dd85cc4bb6184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull hello-world@sha256:a57d21c2de66bc030995bceb8cf9458278798085cddda831b1e949f2376d2908
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (100987407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed28590c49af51daf595c30af5c72b3c9ffc8581155a96c9cfc89ce4b596a17f`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 12:12:16 GMT
RUN cmd /S /C #(nop) COPY file:0afaffc2fa64462107b7178b2ae7d20404ff12f637eabe3a8046192b9d9a0338 in C: 
# Wed, 12 Aug 2020 12:12:16 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b3954eac267c66d7d0f5002fe996d748ce08680a9b2e4a87b3b0c71409edfbfd`  
		Last Modified: Wed, 12 Aug 2020 12:12:29 GMT  
		Size: 1.6 KB (1598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab721a4c44321e34880e7bfdd5ecf8905626c10dde16f6c0b8caf7ad2423c88`  
		Last Modified: Wed, 12 Aug 2020 12:12:29 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
