## `docker:20-windowsservercore-1809`

```console
$ docker pull docker@sha256:1d46aa0a32d316d4f40e4cf5aee286878a6f0c527b24d9934b6035e24864621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `docker:20-windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull docker@sha256:f3714b84a387d3897f180235aadce776774798d4f394f44a405f17d8c1929db3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769895637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c67d6ad6f01b9e1397beb07301451929fd69133247b0909b8fcc8206740280e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 18:55:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 18:55:58 GMT
ENV DOCKER_VERSION=20.10.14
# Wed, 13 Apr 2022 18:55:59 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Wed, 13 Apr 2022 18:57:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181d542854f38ea0a4a21bbed1dc9ed1475a2e4e4ce2bca7f65258aae0e626d`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 364.3 KB (364252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28bb615d8550327c53488febde5e688f6089af17c006de3f81239daac1db82a`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7a7fd5c743b0106388ee4cc511d22e686f07c88bc1c78315c3f86566626abe`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a708ff879c76b4a6402649789b43994b88a410f169331e300c80ccb3375cb8`  
		Last Modified: Wed, 13 Apr 2022 18:59:06 GMT  
		Size: 53.6 MB (53606816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
