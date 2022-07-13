## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:c4c60a9bf7998d5b05c8c6d30644c7301e26edcba1ba9a13afbb4e8d372b9043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull docker@sha256:d286ed6b7161125360b30763cddc35da6be81a4a8d40a46269788a647ab0b4a6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2724680561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa00e049b0813b313a68cbcc666e527d2ee40c170b3c61f83c75952483ee5fbb`
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
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:13:27 GMT
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
	-	`sha256:3c86af5967d42c804ec0ac2f177b83169359deede4dafa6dbfb40bc97aad7181`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d48e2e1c03a59c2bc5fa97787d608c1c56d2c5dea767bcb8266ece9c31be0`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f086bc01bdb19544655edff05b0730da6228f93c165306b8a1c2afbac5b4396`  
		Last Modified: Wed, 13 Jul 2022 17:15:11 GMT  
		Size: 52.3 MB (52281174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
