## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:81de2577b1b8e348069bff3037d6ba00da6d5b1707341f1864c78efafbc13885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.169; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.169; amd64

```console
$ docker pull hello-world@sha256:71ca70650c09da31487c1dfb348bf780c8807b9617974180eaaed46381e82ab0
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (117982763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffabee5fb25e9182c7af7816e4ff76821653e8cfb4f6dc97928126ee56cf16b`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Mon, 09 Aug 2021 15:12:42 GMT
RUN Apply image ltsc2022-amd64
# Tue, 24 Aug 2021 23:27:19 GMT
RUN cmd /S /C #(nop) COPY file:55c009fa8b983e38026b41064e5367bc779dae76c0d404a11886c3cb19ec4509 in C: 
# Tue, 24 Aug 2021 23:27:21 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:ee7a9c9193e3d9bee1b6c8ddddddd5356aed50f77c78d18d377241f4aee6d676`  
		Size: 118.0 MB (117979975 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bc88b4a942843406c08602e5ed3b178e0f0815276dcd12754bf0e513debaf89c`  
		Last Modified: Tue, 24 Aug 2021 23:27:36 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64481920de098fff09ecf54382bcfba57038e6f5f13cd1844a0993b79495ddff`  
		Last Modified: Tue, 24 Aug 2021 23:27:36 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
