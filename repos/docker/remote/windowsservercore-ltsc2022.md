## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f10cd504d09011ac66e85ad70c551a4bb16edb03f9c5c994349037b63be211be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull docker@sha256:edf247a340baea4e8c2d622fb5af1598abe85113b713dd6a3cd5bc5e40506a42
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1480426537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd92513f922f244389d26853ae3f9cabce18252ff320f58d25bc03adebf7fb3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:33:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jul 2023 20:15:10 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 20:15:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.3.zip
# Thu, 06 Jul 2023 20:15:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:15:40 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:15:41 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:15:42 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:16:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:16:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:16:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:16:09 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:16:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c818796445a77806e10e6c159d076d6b0f5105edd8e7f27848042efb890970dd`  
		Last Modified: Sat, 24 Jun 2023 03:41:36 GMT  
		Size: 326.7 KB (326673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343faf4d8143dadaf9de6d52c214909510a19d32a2ef2f90860d9aaf4a919692`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8ab0e8f6197c22da65ebbadcd1fe496b029f0fadf873bc625f887c7580a75b`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49d31da5904ec14a1003079c30d7a269f65706ca9af5e2d6ea0cbe7a2762d2d`  
		Last Modified: Thu, 06 Jul 2023 20:21:22 GMT  
		Size: 17.5 MB (17458414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b059f4f69ae92c7ab553a89fe911075af37b363f07301b5821fa58e14158ed9d`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dd12c4af4dd1eda3383bc2e1023236c4a9d31ad0483bd80ff541d5ca92aaf7`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b223fadd37e4d376cc64a69c7c31a7c10bd36cfd3d4c74e85ebe780d2add0c`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ef3be65907ccf52605b51db71fe3b3b12292bad11ab1a49a78a699b004ab06`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 17.9 MB (17883688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f9df1df7303a9e93905852c6fd3c1183da3654ea42a86788484596b0c52a5d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a0de7a4b55054578241a4e2ec66ccf03b270537b6a18c4e0b3b4250ed14a1c`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c928426eb1e8b4be9068775a7abafdca91118e43ac375399595fe896c759b189`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78728e406ce8bdc2b7dfab0c83103ff85dcf7d19630d4dfd18450e5f13fa2128`  
		Last Modified: Thu, 06 Jul 2023 20:21:21 GMT  
		Size: 18.4 MB (18447298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
