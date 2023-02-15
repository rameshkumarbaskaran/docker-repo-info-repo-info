## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:e4b4bb126038410035c8c6962d643dbf73d0b1d8ee3108c4f005238402a9a0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:bff20886c4e50c2ff56c65ce2b8b2f6f861b63544087ebc9828b8283abf3e9ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1893205034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9666c08cd03c61fe14a234d3f8760533430f35e891dccd0f5540cb34fd9834a4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 03:01:55 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 03:01:56 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 03:01:57 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 03:01:58 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 03:02:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 03:03:01 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 03:03:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:35:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:39:32 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:39:34 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:16:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:16:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:04 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:20:39 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203425975bec1802428fad91a2e5f01172b161062c12eddf729e548bf7e134e0`  
		Last Modified: Thu, 12 Jan 2023 03:48:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80e42e19ab862b4adea06f1995e1f5cbb2c11ad8d68ae4a7bb5d0da5d0e6f38`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be5d5df8cec6d1386f78a342668c3d2cb809372865459c1b35aa8d5a39a463b`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e467d553c4972b55bf8e3d80b16f245e5bb38f28d80b91ca4f9f90c09a6c28d`  
		Last Modified: Thu, 12 Jan 2023 03:48:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97054b77b205167acd5a303c8aa82e380f090ff4e2ded81d3425ec78500139d`  
		Last Modified: Thu, 12 Jan 2023 03:48:14 GMT  
		Size: 25.5 MB (25470784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e150d9e1a1da09e17313cb3b6358d2f16cf2919c51e9addf30500de9d03292ef`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c0d792e2a7942826a61fdc26b6081ab404122751ff4f4dd8f5b8b0eca21399`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 324.5 KB (324466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd89ac843c0479ae40ca8c747e8a676229754549dbfeb9fe7157fdf1a60e685f`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0892c7d4de38540a99ca06e09c0a995b2e119c5ae853eadc2f7558f69bf44bb1`  
		Last Modified: Tue, 14 Feb 2023 20:56:57 GMT  
		Size: 157.8 MB (157805981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b2ec2bef689e3f934369ec3ebb90a5b06c0cbd77b2364e23a776b4da7a68f5`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066daab446064e42a798fe1592cbb9befd18dc7c368cc287f403168c17647f44`  
		Last Modified: Tue, 14 Feb 2023 21:18:46 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ea7fb211a6a6bdf1db9842354942dfaf3dc66bb87b9ce2b1620b897655022d`  
		Last Modified: Tue, 14 Feb 2023 21:18:44 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1a9f71a17b653aeea9897c2da8205709b77073460fc648f6daa323ffffee8d`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53678f100709f21522f2dd0732c10bbb5a70107fa9a4fcdd4895786c68d0bb27`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a973e4e836b19e1ccb3104f7458b2ed9a0aee58d697b6b7a8f7b8800265560f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:53 GMT  
		Size: 1.6 MB (1641852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9b2ad53ca032d7a1d8ef1944923a40be2d6c2fbd4945695a1d7cf5ea708613`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
