## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:60368543a0dae6a4cfc017eeb5f414eb7f9b9ba0a1ab256a2f81707ca0e37dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull hello-world@sha256:63c287625c2b0b72900e562de73c0e381472a83b1b39217aef3856cd398eca0b
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101148429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5d255ea81f83c8c38a982a6d29a6f2198427d258aea5f166e49856896b2da6`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 16 Feb 2020 01:25:57 GMT
RUN Apply image 1809-amd64
# Thu, 20 Feb 2020 00:41:38 GMT
RUN cmd /S /C #(nop) COPY file:0afaffc2fa64462107b7178b2ae7d20404ff12f637eabe3a8046192b9d9a0338 in C: 
# Thu, 20 Feb 2020 00:41:40 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:a35da61c356213336e646756218539950461ff2bf096badf307a23add6e70053`  
		Size: 101.1 MB (101145811 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:be21f08f670160cbae227e3053205b91d6bfa3de750b90c7e00bd2c511ccb63a`  
		Last Modified: Thu, 20 Feb 2020 00:42:02 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d1439be4eb8819987ec2e9c140d44d74d6b42a823d57fe1953bd99948e1bc0`  
		Last Modified: Thu, 20 Feb 2020 00:42:02 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
