## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:bb8e38f2b1f040427de14aa47fb934621821a03a129275f70bc1ad4ff88d56d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `golang:1-nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull golang@sha256:d765527e38df6f07a93dc9489d1cd24585f3e9f966d1dd0511a07b967ef74225
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234169947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e6012e7fdf9092245da1124fed064c4b67cc6b1506fca1a81650210f3fa542`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 12:22:44 GMT
SHELL [cmd /S /C]
# Wed, 11 Mar 2020 12:22:45 GMT
ENV GOPATH=C:\gopath
# Wed, 11 Mar 2020 12:22:46 GMT
USER ContainerAdministrator
# Wed, 11 Mar 2020 12:23:03 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Wed, 11 Mar 2020 12:23:04 GMT
USER ContainerUser
# Wed, 08 Apr 2020 23:13:22 GMT
ENV GOLANG_VERSION=1.14.2
# Wed, 08 Apr 2020 23:15:32 GMT
COPY dir:cedee7ee5ff520e4aa4bf8ec004e9eba31ccdfd2a912466d83949af88a223e83 in C:\go 
# Wed, 08 Apr 2020 23:15:47 GMT
RUN go version
# Wed, 08 Apr 2020 23:15:48 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5bd48aea83b7e2963ae4ac0db2f96681643b4dc342cb3946ca3e871118d13dc`  
		Last Modified: Wed, 11 Mar 2020 12:44:25 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5477696fd9e22926db0f7309a634f6944f820196822afefa1ac999b75c02547`  
		Last Modified: Wed, 11 Mar 2020 12:44:25 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad59b57411eae55dbcd4b8866c459b097d96859ab5b362bf55915c63a137cab1`  
		Last Modified: Wed, 11 Mar 2020 12:44:26 GMT  
		Size: 936.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4945c92290e8b2226499045f6b2ae5ca967c87c1b8f99eb649a1ae4f6fa1ec`  
		Last Modified: Wed, 11 Mar 2020 12:44:25 GMT  
		Size: 63.6 KB (63586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd405078311545e65484faccb35564c272103e6b9e1d0323f9e76f718cf6188`  
		Last Modified: Wed, 11 Mar 2020 12:44:22 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25c8bd7d60e4976526ad098afdf3f8613cdaf9565aa93744d04f700b21ba3bb`  
		Last Modified: Thu, 09 Apr 2020 00:27:17 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b1a890220be1cc3c23482a8f0db4afdc4e07e5e9240dda3e7dc982d8e26f6e`  
		Last Modified: Thu, 09 Apr 2020 00:27:42 GMT  
		Size: 133.0 MB (132977410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364e19fef4441a11f41eaad14c23d0d17ffb159a4728fa339b89e093e95af3ed`  
		Last Modified: Thu, 09 Apr 2020 00:27:17 GMT  
		Size: 73.0 KB (72954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d4d53b3766b6d0360ac540b4d66ec2395ca7e38db4c55b853dfac24272822e`  
		Last Modified: Thu, 09 Apr 2020 00:27:18 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
