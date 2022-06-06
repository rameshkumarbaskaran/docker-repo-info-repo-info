## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:7b53e7d5065f8cdec540d4cb5dff0a6452d9c5e141e3475ce7025646587e2691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.707; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.707; amd64

```console
$ docker pull docker@sha256:e59f9c6431384d61a645aaba06b893312d18b5a844eb29489a3af714fd845c66
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2247906550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36eeb816b4cc4a41c38880b7f79237571631a7cbbf350fb33e7519784b230814`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 05 May 2022 03:02:27 GMT
RUN Install update 10.0.20348.707
# Tue, 10 May 2022 17:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:15:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 06 Jun 2022 18:15:31 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Mon, 06 Jun 2022 18:15:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-22.06.0-beta.0.zip
# Mon, 06 Jun 2022 18:16:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:12fb50a031bdc8d2b65d86d694a4ed20e937852ed1bd3c433d8f2f60279cecc7`  
		Size: 800.7 MB (800671635 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e88d40042c6dc2d74dace22d66dfa64aeebe4cd3eec90e5081400debd9281a35`  
		Last Modified: Tue, 10 May 2022 18:16:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cc0e7671236328b80eb96b578eb47d9bb8c85841986a699074c0abb105d7a6`  
		Last Modified: Wed, 11 May 2022 01:18:49 GMT  
		Size: 604.5 KB (604476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ce5d4f8556d16cfd97e44e5a582deb8398eb7b64cf780e381864567bf2987c`  
		Last Modified: Mon, 06 Jun 2022 18:18:32 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ecca250c0f92063ff845e4544241d25c59661c4d628ca89956af8a07948b21`  
		Last Modified: Mon, 06 Jun 2022 18:18:32 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffa2774904757f64d9793354ee61b805e2e4c355b2cf054a6d023a086562d12`  
		Last Modified: Mon, 06 Jun 2022 18:18:35 GMT  
		Size: 9.8 MB (9762611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
