## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:8d4b74a005b6e1df7fbe4db35d21d3bee116381286a4c583b3b9beb12719e627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `hello-world:nanoserver` - windows version 10.0.17763.1879; amd64

```console
$ docker pull hello-world@sha256:ea0cfb27fd41ea0405d3095880c1efa45710f5bcdddb7d7d5a7317ad4825ae14
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101343231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096dec0e4e755d8697a19e8ff11d5c89e49e2bc6e1bafd4c50bcc87460e9c749`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 12:19:40 GMT
RUN cmd /S /C #(nop) COPY file:dbb4e437ca342a79d5980fcb71c065abfe00353f696b1b54084e7c09d32ec085 in C: 
# Wed, 14 Apr 2021 12:19:41 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ff2c14a87a38bd856aba54b346a0f7805bf9b7c362b6bd4560875ef908d5f1c4`  
		Last Modified: Wed, 14 Apr 2021 12:19:59 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fdf8822288a44ff0676832fed8dba9b80330c3faa310ace82bcc0c1e7fca01`  
		Last Modified: Wed, 14 Apr 2021 12:19:58 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
