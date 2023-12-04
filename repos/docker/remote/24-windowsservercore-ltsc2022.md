## `docker:24-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:768cbf4592934d765e93c76e0e28c0ab47099717d40a9eb86d96d17580f9dbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `docker:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull docker@sha256:69aba7120e3f4014bfa80f4eae2cfc9698dcb6b8a5d64daf06de4039a19846ce
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1941438090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14796d059c4452817642e398254941a9b2c8df8582054034dc1e487fb1183cbf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Tue, 28 Nov 2023 19:12:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Nov 2023 19:13:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 28 Nov 2023 19:13:13 GMT
ENV DOCKER_VERSION=24.0.7
# Tue, 28 Nov 2023 19:13:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.7.zip
# Tue, 28 Nov 2023 19:13:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 28 Nov 2023 19:13:29 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Tue, 28 Nov 2023 19:13:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.windows-amd64.exe
# Tue, 28 Nov 2023 19:13:30 GMT
ENV DOCKER_BUILDX_SHA256=dcf01329368381fae8c24b494186a30d2f1c4adb4bef7a0410b4803e5bb1c352
# Tue, 28 Nov 2023 19:13:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 28 Nov 2023 19:13:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Tue, 28 Nov 2023 19:13:39 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-windows-x86_64.exe
# Tue, 28 Nov 2023 19:13:39 GMT
ENV DOCKER_COMPOSE_SHA256=7d3f56cc84838ca54c5f0e9c8a3645dd96030482d838663c367d93bc6c38dc05
# Tue, 28 Nov 2023 19:13:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e24a7015435126c8cf990c62440a31508a1071bccf0dbd2f44a3713853e2434`  
		Last Modified: Tue, 28 Nov 2023 19:13:57 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf233ed050243c457d847d4c6787947b7beff4f83bf11abf11ac33e30a53e94`  
		Last Modified: Tue, 28 Nov 2023 19:13:57 GMT  
		Size: 497.4 KB (497428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3f888338075748550786bf531962866d802b1059793a7e029098b7e79a9075`  
		Last Modified: Tue, 28 Nov 2023 19:13:57 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa01c24837bdb901fa7950e18c8649f36f99bdb428569c194ffd3fd0af052c76`  
		Last Modified: Tue, 28 Nov 2023 19:13:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858526bd9a0cc8fb4ddf2cb4473480ec1fd8366dd43e3b84bd38c62901758501`  
		Last Modified: Tue, 28 Nov 2023 19:13:57 GMT  
		Size: 17.5 MB (17492510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec542e83ca3d1f532291e9ac9eaff7691c34d624711165586dd320e008237987`  
		Last Modified: Tue, 28 Nov 2023 19:13:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd8c2af45d77cc044918ec8473b6b2306b071ee079a5e1066357bd3c542b52b`  
		Last Modified: Tue, 28 Nov 2023 19:13:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef072a3b2c1fa44c5d030d15356790a19084d23c2ae3ffde78b67ef5ebff11d`  
		Last Modified: Tue, 28 Nov 2023 19:13:53 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626005edc53fe342cce5855f84b184ecf86409c0a73ccb8a6af56b5104e17952`  
		Last Modified: Tue, 28 Nov 2023 19:13:54 GMT  
		Size: 18.0 MB (17985118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422f27639a61b071ae4e81b5fd93ccdac6878969a80c9f8ddab77908d2e774ae`  
		Last Modified: Tue, 28 Nov 2023 19:13:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65315a3742297857b4cff715918072a4bb1c66688df5112a88aae36ec84f2491`  
		Last Modified: Tue, 28 Nov 2023 19:13:51 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9211767dac42a5e87ad5e6fa166c1170f96fb667bd8a09da7c05aac13898f277`  
		Last Modified: Tue, 28 Nov 2023 19:13:51 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52227266319f6cfd54fff1f3f3c817f2c521bc975ebae03e2a80f8dba98f37c8`  
		Last Modified: Tue, 28 Nov 2023 19:13:54 GMT  
		Size: 18.7 MB (18670042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
