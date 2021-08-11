## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:288e15dfe5fbcea7f092d61afa3320bfcde084b49894031c5c0ac5e5046f932a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4583; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4583; amd64

```console
$ docker pull nats@sha256:8a04c3c164f29ec50268b113b4081be21e6bb4bce86c1796633d9523be372a34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6280704388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5c9cb10b7b738afcde561c6c758f4e83f79140edf6afcc7f6298d44fc91811`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Aug 2021 13:57:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Aug 2021 16:52:27 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Aug 2021 16:52:30 GMT
ENV NATS_SERVER=2.3.4
# Wed, 11 Aug 2021 16:52:33 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.4/nats-server-v2.3.4-windows-amd64.zip
# Wed, 11 Aug 2021 16:52:36 GMT
ENV NATS_SERVER_SHASUM=729dc0609e0461aa5fb893c85c04c6b6afa40945183d8d8324d03186d1678a99
# Wed, 11 Aug 2021 16:53:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Aug 2021 16:56:02 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Aug 2021 16:56:05 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Aug 2021 16:56:08 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Aug 2021 16:56:11 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Aug 2021 16:56:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d6d4b60a6f3b0544427c2eb9a5e27e5f6ddca0fd7632003e11331f01c4e9c6fc`  
		Last Modified: Wed, 11 Aug 2021 16:25:34 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe49d3a206649779952cc6a03fdbb4e828336501708ad40c4e1a07237199e28b`  
		Last Modified: Wed, 11 Aug 2021 16:57:38 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d1c00e5ceccc55fc3ce9c5ac53cfb087548f8c0ee2c0311062174aa6dcae60`  
		Last Modified: Wed, 11 Aug 2021 16:57:33 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5bad1b6ae6476985bf0341f8f1fa8f49ed1d589c3938c4377e707bd7f4e7f6`  
		Last Modified: Wed, 11 Aug 2021 16:57:32 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb63d7e8fc07ed8e62b452abc7e74789dd82e82f798517f1a7b79fcefd0bf56`  
		Last Modified: Wed, 11 Aug 2021 16:57:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e651d42cc4f45ee920b3633faed8a074e6b54c5f7fb54ec6d72019c7f3b27ebd`  
		Last Modified: Wed, 11 Aug 2021 16:57:32 GMT  
		Size: 336.6 KB (336584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017caab39271df8b5221622d0f5b017b8e5026c1364c585e1c772e5c84a3f4a7`  
		Last Modified: Wed, 11 Aug 2021 16:57:41 GMT  
		Size: 9.4 MB (9388435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e87e5fc310866618ca3d29d292509f374092d6c32380f5f9128fb8346fd63b1`  
		Last Modified: Wed, 11 Aug 2021 16:57:30 GMT  
		Size: 2.0 KB (1979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c745fe54e5836cb345920edb0279eefc33e8d14fadc9d01d8b9df71224184353`  
		Last Modified: Wed, 11 Aug 2021 16:57:30 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff48906f8bba1eb5768714cbea7603976ecc492a8d421cb8e6d46fc4aab8275`  
		Last Modified: Wed, 11 Aug 2021 16:57:29 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a980f63478b517d8c3b4b85f001ce4b18da7f48011c02b71f0bb6516d53f46e3`  
		Last Modified: Wed, 11 Aug 2021 16:57:30 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
