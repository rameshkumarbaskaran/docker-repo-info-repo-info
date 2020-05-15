## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:79891322cb1d314fc48bc91e5fb81898349861c3689ba759a7ed8c9ffd0f72e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64
	-	windows version 10.0.14393.3686; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:2e808e4820850550bfe857b7882f9d2ec3770e0a77135137b715ee56f8865a3d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723094192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb5eb9524269197d09f9bfd26b36ba48e1c49a38ab8dd9c549052b31db4308d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 13:04:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:49:24 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:14:14 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:14:35 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:15:25 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:15:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6e220442d94ba050201e82fee90c58b5e714748e7906735032367404c473c91c`  
		Last Modified: Wed, 13 May 2020 14:27:38 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef78e6a0bb5c035fff387c2c5470bd8420babb53d74f1856b9e3ed900cd9af2`  
		Last Modified: Wed, 13 May 2020 14:54:40 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3733fe8392820a6176aabbce2fea6e7f5cef35d18d29c985b3d6d8ca530b040`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ec67b51ba3368bcc10659dea28daabcfc7f499ebfcfd842eb0225d3ef64bc3`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e950aa317a893230e32972c9029d3055b3c97b947e8edd05d14f8a8171bf4b`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 363.9 KB (363883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad60f095cd746e908ba4cbf28bf09d893d3bed31ab282e76a82fda02a2920c6a`  
		Last Modified: Fri, 15 May 2020 20:19:41 GMT  
		Size: 4.4 MB (4387713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213500fe8035d9fbefc9fc80861db0087b3faa36c0cec1fd54f1df89d563f0c5`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bad6f3a4966270bdc5ea21caec6010e5cc8fa9b5702d54af3f80bc4be10fec`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0be37cd8bdefc66402e2d1b8f176c815ab9387935ca74f36fa899efa9604b3`  
		Last Modified: Fri, 15 May 2020 20:19:35 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c352832c962e7536881277d349b432e55dda53ddb36f026e2af6ed3a2e02ed3d`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.3686; amd64

```console
$ docker pull nats@sha256:7d6dc2fc9b5be7820c127bb780394be4df5edd15ead8fe4ee35111825b09fbf0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5751211970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ce5815af4bf55d474ff2df1c879f7f1c76df45820494ee959d5b15a8c06c8c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 13:13:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:51:03 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:53 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:15:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:16:54 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:18:43 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:18:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:18:47 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:18:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:18:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d9ecf24b3b7ef3e61c8b38d40e28e57a80552d6c97884f4cc142af2110ddff`  
		Last Modified: Wed, 13 May 2020 14:28:09 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356fa8d07c48624dd3553b12cafae53b1e6818e2e77c7b4ad7c5e37a6edf5f5`  
		Last Modified: Wed, 13 May 2020 14:55:20 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9053aba643e655abc4300887f89356fa95a058b168b8d3404b5627365ce052a`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39bb0a54403409eeecf7ca0af5b7256923560250ba96cf5c6559ba385ac63ff`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26a263f1c36137f9ae855980e5932549cd9ba1b2d46f835ec4436f85161680`  
		Last Modified: Fri, 15 May 2020 20:20:20 GMT  
		Size: 5.4 MB (5380243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c19479d4b0b4596257e15252e96bb469f2347136f7714e78a0392001039914a`  
		Last Modified: Fri, 15 May 2020 20:20:24 GMT  
		Size: 13.9 MB (13932166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5f6330c66b8c1505013ec5f840e8a1d49e0d2e486d31927832512fba92e373`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c740936073ba5f4006ea263354ff9fa5e0b59bc5b3945a6cbc4f7458531ad83`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f31836cddc824c6c9fbd8264bda5ec6369a6d10eb828e04528c6989a11c7a1`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4187a4d9e22eb583a18d4ff3c1c002ec90c4841754c44cf33db01ad1fe0ec26`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
