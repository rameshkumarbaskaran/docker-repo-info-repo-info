## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:3cddcc32f4abfa346000828d972103bcc78caed90de577f078e29a57c7507dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull docker@sha256:49fe52f004ab753bf8b5fcdb8589ee7a7f7057b446073449d7e9487cfb04f7ae
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1993836626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f6e640ae8a73a7ffcb148c979b4ba3e976f92cdcf10c4ccd4770abd5d500f9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jul 2023 00:29:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Jul 2023 00:29:34 GMT
ENV DOCKER_VERSION=24.0.4
# Fri, 14 Jul 2023 00:29:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.4.zip
# Fri, 14 Jul 2023 00:30:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Jul 2023 00:30:49 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Fri, 14 Jul 2023 00:30:49 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Fri, 14 Jul 2023 00:30:50 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Fri, 14 Jul 2023 00:31:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Jul 2023 00:31:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.20.0
# Fri, 14 Jul 2023 00:32:00 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-windows-x86_64.exe
# Fri, 14 Jul 2023 00:32:00 GMT
ENV DOCKER_COMPOSE_SHA256=94ae3b1302faf173ccd1cdc3556bd150f90780ff94cdf6e704a8302a75574da6
# Fri, 14 Jul 2023 00:33:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faeb4cf79c2f4d846a90b33b635df0502f42d01fd0ee86b04449dfcec7cef5db`  
		Last Modified: Fri, 14 Jul 2023 00:39:45 GMT  
		Size: 230.5 KB (230461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159731638bc90a9f0bd35aa147c7caf45cb7eedcb01bb292fb2fe9fe1c81df14`  
		Last Modified: Fri, 14 Jul 2023 00:39:44 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7933132035cf06cc7c507dfffcc6e08c422ba49068d439e68b4e3518a5f3e472`  
		Last Modified: Fri, 14 Jul 2023 00:39:43 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2585570eecc23b6ccbefc5f252f9d21997cbc9c44063bed0822982b1430286a6`  
		Last Modified: Fri, 14 Jul 2023 00:39:46 GMT  
		Size: 17.6 MB (17620781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97523ad9220a9f4b92abdd2a1cc475b49985606847e929b80a5c792f4ebc22a2`  
		Last Modified: Fri, 14 Jul 2023 00:39:42 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc078207dd9e7f5fa7ba6fd059decaa87b3ec5e162b6d9eb31712c1ac63bc1fd`  
		Last Modified: Fri, 14 Jul 2023 00:39:41 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4174f3b1d96aa1c23e579a99d26d6db2d2e30592f7c39b8e16843decc9a9dd47`  
		Last Modified: Fri, 14 Jul 2023 00:39:41 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac3853e228d19449f6408591778422c917fe046ea6216e51ee3cf9e06b68ef7`  
		Last Modified: Fri, 14 Jul 2023 00:39:44 GMT  
		Size: 17.9 MB (17856072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa688c0dcb7f41e70f930863dc4aaf0de773e789db2f440bfd5c05f1c2d58ed6`  
		Last Modified: Fri, 14 Jul 2023 00:39:39 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e402cc7e594dcf951bad673489140ef2725f67f1cdc4c40da8292d51bf7054`  
		Last Modified: Fri, 14 Jul 2023 00:39:39 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70d8932c39e313a28511053af59cfcc1f1a7e5fd371373010c55bfcbccfaff1`  
		Last Modified: Fri, 14 Jul 2023 00:39:39 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d3bf2d3e7368905eb01338c31897058966466d1e8fd2d9ee353652f371826e`  
		Last Modified: Fri, 14 Jul 2023 00:39:44 GMT  
		Size: 18.4 MB (18427599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
