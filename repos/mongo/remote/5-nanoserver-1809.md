## `mongo:5-nanoserver-1809`

```console
$ docker pull mongo@sha256:9c059589a8359c8fe13bdf744892acdfbac7a08e17defa1c81f7125671f5704e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `mongo:5-nanoserver-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull mongo@sha256:2c2208400a89c7dd874e68f59d9e814f263463288fca042278ffe59e5c820b4d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.5 MB (419547767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7587140776d781d9c76f151e9f2dab5fbf2ecc27d59e95d4e6c6faaa6ebf83`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Wed, 12 Apr 2023 00:23:53 GMT
SHELL [cmd /S /C]
# Wed, 12 Apr 2023 00:23:54 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 00:24:05 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 12 Apr 2023 00:24:06 GMT
USER ContainerUser
# Wed, 12 Apr 2023 00:31:26 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 12 Apr 2023 00:31:27 GMT
ENV MONGO_VERSION=5.0.16
# Wed, 12 Apr 2023 00:32:01 GMT
COPY dir:075c117c846ecae2a4dae09c1251726c18757124193e63e7a862c7fb794f695e in C:\mongodb 
# Wed, 12 Apr 2023 00:32:19 GMT
RUN mongo --version && mongod --version
# Wed, 12 Apr 2023 00:32:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Apr 2023 00:32:21 GMT
EXPOSE 27017
# Wed, 12 Apr 2023 00:32:22 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e9c90f3a763714533d4a634f7ab3d23374e5208e2ac8bae4288243917bd972`  
		Last Modified: Wed, 12 Apr 2023 02:34:36 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6552b5bd1c6568d6f39240a39a0344d31519e6acaf2437760d33a2f1bd16ebb4`  
		Last Modified: Wed, 12 Apr 2023 07:26:01 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb24d44a5b22599181c1f6c9ebdf5458cb1fc58facdffff33b51e656ba5a14b`  
		Last Modified: Wed, 12 Apr 2023 07:25:59 GMT  
		Size: 68.8 KB (68801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61d7e4579b59b23268c08766daece41ab2483fa4867cc1a017edcfc07642639`  
		Last Modified: Wed, 12 Apr 2023 07:25:59 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f852ca225da877b3fd9632d1eaf590255b257c97045bc7165d49cc5d006e62`  
		Last Modified: Wed, 12 Apr 2023 07:31:00 GMT  
		Size: 263.4 KB (263379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1a866079be60d8ff24e56cb6237eb9454ea7c842a9a340dd93e548ac049241`  
		Last Modified: Wed, 12 Apr 2023 07:30:59 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c23399dfbbb2441bcc8e938be88404904787c259a404eba513b08d19ab4e650`  
		Last Modified: Wed, 12 Apr 2023 07:31:58 GMT  
		Size: 312.3 MB (312338611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0adb14ab6801c5df10d398bce9f786b4b7c5285748cf429d3278c437f157c99e`  
		Last Modified: Wed, 12 Apr 2023 07:30:58 GMT  
		Size: 80.2 KB (80221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4a7a2929b4c35cd66a5ebbe533cfa9485399300e507dc6c9ff2e8a3d53f8ea`  
		Last Modified: Wed, 12 Apr 2023 07:30:58 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec400791ab380cb12ea7627742e3630bd7db4444cbcb2482b5b3a47f16a496e`  
		Last Modified: Wed, 12 Apr 2023 07:30:57 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd167eecd87518cf7d2f0090e1e4230919ff125c91032a40507d1b393869446`  
		Last Modified: Wed, 12 Apr 2023 07:30:57 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
