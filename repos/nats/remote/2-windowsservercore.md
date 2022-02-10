## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:33946d4adb965632134b6c514f7e588e27df9e4f7d4e3b555d31c28496fd2181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:2f206c7404528b4d1b631e8747726f7f32fa0519169bc201b32fc2b826d89a1f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718958093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8800eccde299346c51025ba23593daa22a824125479a0501431412ee4934a6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 15:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 18:10:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:48:50 GMT
ENV NATS_SERVER=2.7.2
# Wed, 09 Feb 2022 20:48:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Wed, 09 Feb 2022 20:48:52 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Wed, 09 Feb 2022 20:49:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Feb 2022 20:51:00 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Feb 2022 20:51:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:02 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f49d3791198cf2ea875fd54ce3bb715670742d4a58c00252395ad1b74036662a`  
		Last Modified: Wed, 09 Feb 2022 16:39:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4235aeeb4e8b577cc7aa26c7994ec94c94dd53a38764fc510b330b77cef4abad`  
		Last Modified: Wed, 09 Feb 2022 18:14:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5624de3564dcef1325bc61eea92cfcb7dbc1c7b35b0023cd17b2f17c38e6df9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3f050ab2ed35215f1fa3bd806046f502f70d7e85d3f070bdd6fd744864cf9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58550f980b41b606662c4c2d767cca700cbd91b7ec3445c99c5044ca946d586b`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5343d460a59e635dddf02a131dadf49fd2316ad0fef64a08af5e30a3cba30cb5`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 364.5 KB (364524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd6e130904f62e22c3a23ea8b080883ee9bbb534b2db618e0a38cab2766151e`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 4.9 MB (4865553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac13c2b0fa7ddd6703c6c46640b9752b4b5be3aac511ccf5af6c20188a55152`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff779110ef51e3be2fae7dc9e966b4392f3dc10973c23dc689c8c5e78e35494`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9efdff7b3152cb65b604c10ab9822a72e900481f5815179012a1c7a945f9567`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb94adbb9b65f8ab12036ec18b5b9903bb67aa43ed6e10f680078e35eb76c4fe`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
