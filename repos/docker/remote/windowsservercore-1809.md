## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:3309d92454b96ac8b98caa77fed9234028a5ad572ff8e9f71aefe6ab5f00a68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:66782f896985fef851151d9c03834d55dc7c0a5cc62f63f0be8deaf3991b9705
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737563440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e689ba929abe8bc074c56efa2271a5d2a6c77eeaa8b97a4da0702ee5332db97e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 25 Oct 2021 22:14:51 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:14:52 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.10.zip
# Mon, 25 Oct 2021 22:16:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae47711e52b43c0ab007c4766c4fdc4ad2eea396536809f52c3dc97026f7c0c`  
		Last Modified: Mon, 25 Oct 2021 22:16:49 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8496294e89bdc509971f65f14aa4a8c4755fb867b10aa5f4541151ac70d849`  
		Last Modified: Mon, 25 Oct 2021 22:16:49 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed70c6ab5fbc25a96ca76000a2aab07ea3eade1ceff6c257e7bd7c0745a687e`  
		Last Modified: Mon, 25 Oct 2021 22:17:02 GMT  
		Size: 50.9 MB (50893149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
