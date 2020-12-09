## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:651bab66a30a39cd2d8f448d5f7f0f3f36fd37e4930143bdc8ef9c4a73b1db2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:45be90b14254e72787810aad606ccd4d37b296d1969e815017fa1cf7540cb26a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408976712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e98282f2d93288883d04152d4182e9faf78d3d41b1cef34f258f27aa602d513`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:36:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:36:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:36:36 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:37:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:37:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:37:52 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:37:53 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:37:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9257be76bd37cad15d45905ec5910266409794a9dbd8a0428174f8b2f352a`  
		Last Modified: Wed, 09 Dec 2020 17:42:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce12d099c4f8deaeb8b91eecc396f9b0db017e29087d9b101a7b24c8e53f2db`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbf54e6b3a7d9cf4345b6cbbf9bb383129ce792795dccf79a53db79869fc968`  
		Last Modified: Wed, 09 Dec 2020 17:41:58 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278cf3ca07ba69ac82df664d7396cd49a61c1cc509f82f5f2a991ad12e660a9b`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c11b4ea4e91b3c9ad1f6ad9bd4c51a0961e8a10eafe40691439fff4e66616e6`  
		Last Modified: Wed, 09 Dec 2020 17:42:02 GMT  
		Size: 4.8 MB (4843263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2755f47bf0200184985eec72df9064186ed7a6ea2bfa1da09e3e7187dbdb5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:08 GMT  
		Size: 13.2 MB (13248209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aec46694c6b5483c50d068186be07a5e00247bfe4678d9804a2386f9608386`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21af927ab73dbbc8dbf9a9d9c46cf1cd1b8f67af5de09608cf59941ac8a65bed`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48e8a4bdf82163a3715d172cad9fab44e5416d28730c3e48a9164e1d5352f6`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24890fc54bc0b6cd916c3d35fb39241cec6ee1bb968a47bd96b0869dece707dc`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
