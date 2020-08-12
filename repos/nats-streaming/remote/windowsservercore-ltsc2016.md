## `nats-streaming:windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:42262ddae4ea4f271a30da262eca5022b7cba71e8302c75a7a8f4ff3df6b4f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3866; amd64

### `nats-streaming:windowsservercore-ltsc2016` - windows version 10.0.14393.3866; amd64

```console
$ docker pull nats-streaming@sha256:89e03a9aa43c0bdb588f21434ef27b8a7fbb22078dd92fd2e4d8904092f477cd
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5759345739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ddb01ea7294dc74ae6adc0db5bec4bf64cdeabe17c5c7a20451f4641634cb1`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 Aug 2020 12:23:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:13:46 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:30:30 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 12 Aug 2020 18:30:31 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Wed, 12 Aug 2020 18:30:31 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Wed, 12 Aug 2020 18:31:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 18:33:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 18:33:31 GMT
EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:33:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:33:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:44c31749d2d4be3aede3e54780d9e54b5a7eeaa617e1adf027e92fce2ebf0f2a`  
		Last Modified: Wed, 12 Aug 2020 14:52:35 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966377bd81e347a691363116c353d48b02f40befd2b38ce2a9f31459dfe79978`  
		Last Modified: Wed, 12 Aug 2020 15:17:51 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc178724568b0a2420fb8850ed0546a60d333fa1f23c34e94c71ab06b647ec5`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0536da8d0a8e905c039f2308f1e3bdb97838b9cf6bc5c37430e118fbcaa8e7d9`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cba38fec9b073ade1a0c6dda91e36104b894652a380b76bbec19cf24e6a2695`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f072dda1f9db7b0b0327db1abb0a4ab10dc5830995b40ee063911f55b9af7a16`  
		Last Modified: Wed, 12 Aug 2020 18:34:43 GMT  
		Size: 5.4 MB (5389867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a180d1a5f8d118ec75fe9836ee20b46ab6c2ba5ea3f535245c46adadb1bf79f`  
		Last Modified: Wed, 12 Aug 2020 18:34:45 GMT  
		Size: 15.8 MB (15799524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b923ee9d4a8b167e7d0240164f7cda58fdd12f6c179ef683ad4da6b9fea0dc99`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acbacb00093bd8283cfce1fedfd5b7482263e99c0781041861bbe8ea1f3771a`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd20adcf0b6de8eb3754b51205750c0c072878f2abcb5b39413238f4f026e8ca`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
