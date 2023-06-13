## `docker:23-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:7926808eee47db6deda097bcf6fc1cfcdd7216a2b54623827618d5f138485f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `docker:23-windowsservercore-ltsc2022` - windows version 10.0.20348.1726; amd64

```console
$ docker pull docker@sha256:31132886aed458bd4e2ac5453f6929a1f0dc977c7ebcd8cf8c526af5359df081
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1827489152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65b6f7efc5ea5bd23d3b332c131dee6f989ccb6bd421fa1f0f90559ee9fe503`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:13:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 03:24:47 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 03:24:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Wed, 10 May 2023 03:25:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 13 Jun 2023 19:18:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.0
# Tue, 13 Jun 2023 19:18:14 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.windows-amd64.exe
# Tue, 13 Jun 2023 19:18:15 GMT
ENV DOCKER_BUILDX_SHA256=e314569943a591a097fa9119bf786556a4eb5c710e8ddefa57e95cd95aa7cc7f
# Tue, 13 Jun 2023 19:18:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 13 Jun 2023 19:18:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.1
# Tue, 13 Jun 2023 19:18:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-windows-x86_64.exe
# Tue, 13 Jun 2023 19:18:40 GMT
ENV DOCKER_COMPOSE_SHA256=6083a9057010a6a048d83c94318d254657abee48600baca2402fbe887d0b7ec4
# Tue, 13 Jun 2023 19:19:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94bc80e6c1e6606bc432e9fa1ebc3ed83fe3ceb5a176e0a7b2c8334bf863c53`  
		Last Modified: Wed, 10 May 2023 07:11:29 GMT  
		Size: 446.9 KB (446946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e927fbd88402bacc902c2a4593f281068b2a6657c7f8b4e53ac01f8e636901`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165e88795de1230f78ac3b0186a534bd16fad90474fddb00254443f5440c8c65`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438806a743132696d59ff6500d80c1c45b0742da1613dbde135436ef14f725af`  
		Last Modified: Wed, 10 May 2023 07:12:05 GMT  
		Size: 17.3 MB (17316446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b33ffae54de9358bdb84234763bea62b7a6488a9100a0e2dd6a49f0fa297c`  
		Last Modified: Tue, 13 Jun 2023 19:22:51 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7387d3042b2ed81c3f976782fa1f6466a8fb264d71e973de90a98d85adfe5823`  
		Last Modified: Tue, 13 Jun 2023 19:22:51 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0cb8297d23be6f7bdc96b9f706a24960f5229fcb5c6e0bd219e21e538d08bf`  
		Last Modified: Tue, 13 Jun 2023 19:22:51 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65887cb767d8b3bae4d623cae6386452588d1668045cb9475a7a413937b43361`  
		Last Modified: Tue, 13 Jun 2023 19:22:54 GMT  
		Size: 17.9 MB (17875246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e196bccfd8a312736dc686dfefe690569c1d58ba21cd44444779376cb264a421`  
		Last Modified: Tue, 13 Jun 2023 19:22:49 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c86ce85ba00bc767fcaca6f85c2fc51120d17e2352e3cb1e326f44a8720952`  
		Last Modified: Tue, 13 Jun 2023 19:22:49 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02ac1ac966fdae98ff28d1d5d70d718894acbb7e9cbb93c6e255a21c7aa6772`  
		Last Modified: Tue, 13 Jun 2023 19:22:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f451d2916cc8e682f439cb5056e53f9a34bd0759b0fec923d420a144dfb91f`  
		Last Modified: Tue, 13 Jun 2023 19:22:54 GMT  
		Size: 16.9 MB (16856351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
