## `docker:rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:35d815c0f33797de72b554f4b54011993fc220a443932c9d7a57ec5b5e1ff5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `docker:rc-windowsservercore-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull docker@sha256:11e833c8880b2318e4f0f2c161c7ecf04ec129277ae8d9040971b04185b53b04
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2681925749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4e2c4281dbb643e4ea2b0ae3993b6652eb026718c537c2223dc3d607bb1de7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:10:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:10:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Wed, 13 Jul 2022 17:10:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-22.06.0-beta.0.zip
# Wed, 13 Jul 2022 17:11:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d6c0a51981d7e8209dadd5b937bfeaf0f26a2c75f59ffe3fd0b942900682fd`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 351.6 KB (351622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca49c3d0f1b10ab622d1ad62fdff5b201db2b1b5d796919f0d74b70a933b6a2`  
		Last Modified: Wed, 13 Jul 2022 17:14:21 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadd2a4879da5a12799c4722e6d956052140ab1b2c9246ade10879c43a875d98`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd78d697ed3fbe490f2c2eab2f6d2591b4205efc5b6c041f7b6853dcebd8d154`  
		Last Modified: Wed, 13 Jul 2022 17:14:24 GMT  
		Size: 9.5 MB (9526144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
