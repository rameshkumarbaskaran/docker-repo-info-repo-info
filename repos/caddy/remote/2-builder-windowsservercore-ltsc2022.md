## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:1834697a8364fc6ee4ee5ffa28c81b39ec291cb266777f278eea81eb05591845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull caddy@sha256:a423e874465bb5a774b23330784cb3f3113b12503f31075a61fccd0f288ddeee
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1611381514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822ebac3dbea73693544a7526ba138dbf203013d7f0a84dd08aafada1592b44b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 01:39:57 GMT
ENV GIT_VERSION=2.23.0
# Sat, 24 Jun 2023 01:39:58 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Sat, 24 Jun 2023 01:39:59 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Sat, 24 Jun 2023 01:40:00 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Sat, 24 Jun 2023 01:40:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Sat, 24 Jun 2023 01:40:34 GMT
ENV GOPATH=C:\go
# Sat, 24 Jun 2023 01:40:55 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 Jun 2023 02:03:48 GMT
ENV GOLANG_VERSION=1.19.10
# Sat, 24 Jun 2023 02:06:44 GMT
RUN $url = 'https://dl.google.com/go/go1.19.10.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c749a054a5da17202113455040484893c29ebe5ab71fa89f60cdfb4561dcce8c'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Sat, 24 Jun 2023 02:06:45 GMT
WORKDIR C:\go
# Sat, 24 Jun 2023 03:24:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:24:45 GMT
ENV XCADDY_VERSION=v0.3.4
# Sat, 24 Jun 2023 03:24:46 GMT
ENV CADDY_VERSION=v2.6.4
# Sat, 24 Jun 2023 03:24:47 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 24 Jun 2023 03:25:15 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('542b4c083852d41081186c79757b66ff3c26248f72ed461dbc038b51687d0a8a8ce8eee69e3b5a1d43360c48b3405b611b940fa378debe98aaa0b3c5aebfa218')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Sat, 24 Jun 2023 03:25:16 GMT
WORKDIR C:\
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
	-	`sha256:24a725a5b1d95b19c55801da205e401134949a3ef3b2bb040c785986202ad134`  
		Last Modified: Sat, 24 Jun 2023 02:16:35 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94771fd18b203dc5bc66c78c94d318edc726e0d3622915884225783fae93b5d`  
		Last Modified: Sat, 24 Jun 2023 02:16:33 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c970e5e0e48292f70cad71999574a45005b6e3963bda38cfde70630ada11e37`  
		Last Modified: Sat, 24 Jun 2023 02:16:33 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6de2df6562966a148a26d7f00bf85d056d4d22c71ebe170634f84253f0b559`  
		Last Modified: Sat, 24 Jun 2023 02:16:33 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d888c846778cfed7da69e726b491b06cbec333bdbe711985b03844e3948608`  
		Last Modified: Sat, 24 Jun 2023 02:16:38 GMT  
		Size: 25.4 MB (25401467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ac5846332b11bb977d027d06552fe067f700a9d5a62560972a0e3c561e19be`  
		Last Modified: Sat, 24 Jun 2023 02:16:31 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0157f348cbd78f039722165c2f836f19d234498082d52f2bb0b601aca16fab`  
		Last Modified: Sat, 24 Jun 2023 02:16:31 GMT  
		Size: 264.3 KB (264272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d5cdace32abce9fdea8a8c776b5a33460acd2c6a1d4c6300cbffde6023dc96`  
		Last Modified: Sat, 24 Jun 2023 02:20:55 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdcc9fecdcd78088b5f0cf1cf9b0aabc93e7dbf6e09f261a9c563a6f2473a0c`  
		Last Modified: Sat, 24 Jun 2023 02:21:29 GMT  
		Size: 157.7 MB (157734312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9988f3f93503ca9b8d2bf44df20b095b61ca317d23e85169d4d01bba7f0995`  
		Last Modified: Sat, 24 Jun 2023 02:20:55 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830ff0e805b8f11336495d041d3b85d376f62dc2cb3abb3d434ac61780dd7ba8`  
		Last Modified: Sat, 24 Jun 2023 03:31:05 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491096e01d536188d6fb5898c4359fcf7153c6c3cba314a8e91a4f4654ece690`  
		Last Modified: Sat, 24 Jun 2023 03:31:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6797599122f231abb3f2779c5f09cec071f4b5c32bc9f7c28571ed5896825a3e`  
		Last Modified: Sat, 24 Jun 2023 03:31:02 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edabd4fbff2bfcf3e8fe988283b0f4cb0232ff5b6be727d9917d5b91c811224`  
		Last Modified: Sat, 24 Jun 2023 03:31:02 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ed91fbff97a345ba30e7297a12357241a9a12ea9b8ad1fa23428a4075ac2fc`  
		Last Modified: Sat, 24 Jun 2023 03:31:03 GMT  
		Size: 1.7 MB (1664814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0541ea4982954ac8ebba7dfd0c6c10f72f9359f5343c757e1d35a5efae31ca78`  
		Last Modified: Sat, 24 Jun 2023 03:31:02 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
