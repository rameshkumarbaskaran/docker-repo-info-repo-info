## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:6ec9fe851d863e499bbff1c6ebe24df42d9df4207c7302a5994ea8b217141c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull hello-world@sha256:4fb0dd2040e4a909567fb8fd36338a00e727926da9e8f93fa1fe58cbc3b9af9c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102706808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0269b73752169ed92549b265c23faea7bed83e077136f9dc94f456519c6b5c`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 12:15:10 GMT
RUN cmd /S /C #(nop) COPY file:dbb4e437ca342a79d5980fcb71c065abfe00353f696b1b54084e7c09d32ec085 in C: 
# Wed, 15 Sep 2021 12:15:11 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a25c4ee2d18d05dd63dbec973ddf256712163d8ef1411ae69fafc9b03a7cda31`  
		Last Modified: Wed, 15 Sep 2021 12:15:34 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee745e5dec327b4974d8621a3fb982e3952809bba3a49b0dd10db4828571ef2a`  
		Last Modified: Wed, 15 Sep 2021 12:15:34 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
