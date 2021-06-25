## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:a673dfea57d51e9d21677796f5f72f60d13dab15b74dd8b2dfe32518cd6ca782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:2b5fc0956f7fa5e8a5d73443e2b2cff10b2c5a1d750238f0c39d388ad230e889
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2646697143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3296c025e7c6bdec1087e1cd78a2af9c8398fde53f8acc26c4c2c62dade1e2fc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 13:15:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:52:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:14:27 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:14:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:14:33 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:15:14 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:16:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:16:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:22 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae7d2dc4b590128efeafd375d02122e65a2525623ac2be100c1a390caf8a4b49`  
		Last Modified: Wed, 09 Jun 2021 15:28:02 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507a90d55d261855b42c7b5905599cdc274ca135ad962fffffe1fa6246c9bba7`  
		Last Modified: Wed, 09 Jun 2021 15:59:38 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29775406c1781fcc27d8bf50b4b0bfcd9418dda6cfae494e4d9383e0213df24b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3bf008ba6d0a427891ae36a26107b3e1f386cb9be8dbd0427623920c08cb93`  
		Last Modified: Thu, 24 Jun 2021 18:21:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35cb02232de3ac8c2255dee0bc6a718b0b3cb29b7baa3caf9825fae6519353c`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811ca1ef9b5e7b658fe9eb6dcf4145a8c7fc2108cddf27604a32625196d9435`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 363.9 KB (363906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07799fa10e1ce0eeb453bb8919dd2756d7f46df37096e364eaef1cf48ee4d27b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 4.7 MB (4734976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7d8a61897a84ba84d3157167674e44f39375855accec3dbfd1bfcc8fb1911d`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.9 KB (1921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5675249b0aafebc9b96c1c5359219fa68fe30b7e67d7877c5d2a8c6083b153da`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42271808b9146dc5744c45edba3f979ab16c9a382b62c44320fa4f04f9ab0f97`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dd08bcc8b2cc2e24a6318d63fcc471176adf3acdf78b10ac15b1fa5527c568`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
