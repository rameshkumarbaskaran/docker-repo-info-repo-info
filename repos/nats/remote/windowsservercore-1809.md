## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:f29246f54ab87c353272363dc66d3c4c048e1509a00978c0948bf7444af6e691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.1217; amd64

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
