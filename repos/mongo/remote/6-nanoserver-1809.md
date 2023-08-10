## `mongo:6-nanoserver-1809`

```console
$ docker pull mongo@sha256:fab5c14f2444bcbd33d446da05674991779a014a84aebb67c2b11d2fa3a45bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `mongo:6-nanoserver-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull mongo@sha256:3b44a1a3757b4c6963fe91d198075e87fe076ea69887a5dc7edc2c0411afd5e6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.4 MB (621363738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46e0f399a4b41978472cc783c56db5083733a7a6432e5f884ba1b202b76320c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Thu, 10 Aug 2023 00:48:08 GMT
SHELL [cmd /S /C]
# Thu, 10 Aug 2023 01:15:48 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 01:15:57 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 10 Aug 2023 01:15:57 GMT
USER ContainerUser
# Thu, 10 Aug 2023 01:15:58 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Thu, 10 Aug 2023 01:30:47 GMT
ENV MONGO_VERSION=6.0.8
# Thu, 10 Aug 2023 01:31:25 GMT
COPY dir:ece1ac4e72523e5445e13262209cd12cb9863d3774981ba252b9a3cd29bf28b9 in C:\mongodb 
# Thu, 10 Aug 2023 01:31:38 GMT
RUN mongod --version
# Thu, 10 Aug 2023 01:31:38 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 10 Aug 2023 01:31:39 GMT
EXPOSE 27017
# Thu, 10 Aug 2023 01:31:40 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:86fab75eb466cadf89d853682179b3b57eba9fe28c78041dd52bced81e18a627`  
		Last Modified: Tue, 08 Aug 2023 17:55:54 GMT  
		Size: 104.5 MB (104459386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298e0f667b1d8252956bc07b8438d68801dd9eb4ebb7ad345fde0bed30609680`  
		Last Modified: Thu, 10 Aug 2023 01:03:59 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814fa0d01fded994ad965ae5487dc312820ecd968291d0bb20ee608f702a9689`  
		Last Modified: Thu, 10 Aug 2023 02:00:40 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021e83a508dc7adbef323d416f3a04d3d4889d441750fa4ecf3ed425ee2e1f0`  
		Last Modified: Thu, 10 Aug 2023 02:00:39 GMT  
		Size: 69.2 KB (69188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956b7c3ad022ed0da478f25e9b64d0c5ac7947ac14c611b3d359ef414b7abf35`  
		Last Modified: Thu, 10 Aug 2023 02:00:38 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf6796c7b91221863b1920e4991f4a08153b38f271641d2b9cd3ab35640e935`  
		Last Modified: Thu, 10 Aug 2023 02:00:38 GMT  
		Size: 267.2 KB (267155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5532049bb2bde05d7d9c644d579bdcc75d2954e55a68c6b27b695bbeed188d0a`  
		Last Modified: Thu, 10 Aug 2023 02:12:36 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932b92ed19bc49c76f7af441b356ccca41baad38eee41b672ffb5ea2b55b8cd8`  
		Last Modified: Thu, 10 Aug 2023 02:13:50 GMT  
		Size: 516.5 MB (516482000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb44d0bf25bb5fc69a72d7b6ab334d359e67a56e2491f6102ddf6c6b2ae43301`  
		Last Modified: Thu, 10 Aug 2023 02:12:34 GMT  
		Size: 78.3 KB (78273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6581d093ab9fd1cf8fa88c337472e947d96ef0eeef91bb02f159d453859221e4`  
		Last Modified: Thu, 10 Aug 2023 02:12:34 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162d390b36f210d92cf854a3c15b4ee50d7a1895a02eb83c3828d1b680bbcc70`  
		Last Modified: Thu, 10 Aug 2023 02:12:34 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1529ea26e14cc91b0ea1896c5ca657ab339c7fb1479bbf979b0da8bab5990a`  
		Last Modified: Thu, 10 Aug 2023 02:12:34 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
