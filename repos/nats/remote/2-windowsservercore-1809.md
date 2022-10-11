## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:fb39a5ed839f11261b832e0dca62197ee21a2ad938138f4cc656a9a52d03d975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:4bddc4dfe1d225cfe86ce8237721abb0c49bd069e8c0bf1ab5c0ba2ec5c6899b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2716818637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ab84e2e207d755fd864c921bfee7744f5f0533ef2a8eb1649486351579db39`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 17:22:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Oct 2022 17:22:08 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:22:09 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:22:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.3/nats-server-v2.9.3-windows-amd64.zip
# Tue, 11 Oct 2022 17:22:11 GMT
ENV NATS_SERVER_SHASUM=83b25dad03dee498becb734623ae4d096235b2863be878d5f6d6a32d76f7e85f
# Tue, 11 Oct 2022 17:23:56 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Oct 2022 17:25:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 11 Oct 2022 17:25:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:32 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:25:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462d88c3de2e572b0d0ee482e3424c3ecb6eae150e8b29e5c8678a3059178bea`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12db35ec0388714c2e4e91a025ad3c010583c420b244c7941d378814da4b414`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61065ad9c7494c241e65c1c1b701828947105c6de39a9a246ef1da83d1967b`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a922f9001668df7166a8c2806eb76dacbac25dfe2a6a6b366546a53ff4a68be`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 350.4 KB (350379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696f9101e75d054c09b2f5086fdb484f298ac859200417dc480c0c95d4db8b79`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 5.3 MB (5290962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063d7a0294a6b35b745dafda4218ac1caccd20c2862af30174e073d25df4240f`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d46f46f65dffc178e8ef8c4d17fc35f23e32db9c2b23028319ab7d51f92b36e`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea87d29a4c3431239148436823825cc53a83211b86daa22eb69df30ff028bde`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245dfbad1025b6c7d6ad15e3336d3a11bd111607ce8db6de8efed6a157cc5872`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
