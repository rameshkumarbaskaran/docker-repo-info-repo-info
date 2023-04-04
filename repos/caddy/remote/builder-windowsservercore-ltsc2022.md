## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:a04bbae350bc4c84e3c01ca321ae14706fe5655633f0931e8182ef0de6d323ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1607; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.1607; amd64

```console
$ docker pull caddy@sha256:b57f59c72940afe0b6a28f9817dd43c8cf46cafd7a052faa2df8742441a54be2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1900173942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4252deb3d3f742a9d696ca7b4d04d6a2fbe162de755f27fde7746793ed96e699`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 10 Mar 2023 06:37:36 GMT
RUN Install update 10.0.20348.1607
# Thu, 16 Mar 2023 00:38:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 02:00:02 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Mar 2023 02:00:03 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Mar 2023 02:00:04 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Mar 2023 02:00:05 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Mar 2023 02:00:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Mar 2023 02:01:00 GMT
ENV GOPATH=C:\go
# Thu, 16 Mar 2023 02:01:33 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 04 Apr 2023 18:40:22 GMT
ENV GOLANG_VERSION=1.19.8
# Tue, 04 Apr 2023 18:43:54 GMT
RUN $url = 'https://dl.google.com/go/go1.19.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '433558e81b8be2983f370bf8e21ac52e76e9e1e50c69b6dc0047f1b6acde97fd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 04 Apr 2023 18:43:55 GMT
WORKDIR C:\go
# Tue, 04 Apr 2023 19:24:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Apr 2023 19:24:34 GMT
ENV XCADDY_VERSION=v0.3.2
# Tue, 04 Apr 2023 19:24:36 GMT
ENV CADDY_VERSION=v2.6.4
# Tue, 04 Apr 2023 19:24:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 04 Apr 2023 19:25:07 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 04 Apr 2023 19:25:09 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c921d7eac594f5e3ce3ef10adb8fd0f71bdbb713c4854336b995d25f89c44d42`  
		Last Modified: Thu, 16 Mar 2023 01:41:04 GMT  
		Size: 327.9 MB (327911088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bca4593035ae0e8d1b6e6eb1b053fddc6a6824b28f45f99de726d752d2c0f72`  
		Last Modified: Thu, 16 Mar 2023 01:39:50 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc92251be4a3030d0c1ad240813d13619cab05ed6114271f4f31e2e37ade28a`  
		Last Modified: Thu, 16 Mar 2023 02:45:31 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39cf6573a7f6e725c805ddf277348509d33f67f8a6216a2a0e1b04f1be37158`  
		Last Modified: Thu, 16 Mar 2023 02:45:26 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28db9d107c8208ad44d6a6873db70ff7887d6d3afad4cf934a0b2babd2cc48ca`  
		Last Modified: Thu, 16 Mar 2023 02:45:25 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4f39a3aa63487027366004c347541623d246d80d6fe57e23ce4040c94709ef`  
		Last Modified: Thu, 16 Mar 2023 02:45:25 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3be7e7a27e770912dcb9b9a3ef7e82764a250d64726013c23ac515b5b810573`  
		Last Modified: Thu, 16 Mar 2023 02:45:35 GMT  
		Size: 25.8 MB (25825670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5990e3c132a38a31cb5f36c7fe62af4390ed95711decdc15695ce969dbfc38`  
		Last Modified: Thu, 16 Mar 2023 02:45:23 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2807b4fd79ee2ec379a6f147d376f4c869daabbd081cb9dbb601ec6d397dd92`  
		Last Modified: Thu, 16 Mar 2023 02:45:23 GMT  
		Size: 540.0 KB (540000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268d668773bbbd967e0fe7f0c34e5bce19504b7867d907615fee2d728d5786d1`  
		Last Modified: Tue, 04 Apr 2023 19:02:07 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968c88aa99824065fbfff28c41b04f94f82d2a2a7cf725be5c612ef7164dfc8a`  
		Last Modified: Tue, 04 Apr 2023 19:02:58 GMT  
		Size: 158.0 MB (158000628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a620f8f89f4f31bf97e8acd0fa1daf547622000d823cccfcd50286a25bccae`  
		Last Modified: Tue, 04 Apr 2023 19:02:07 GMT  
		Size: 1.5 KB (1543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317eb69d2fcaf5ad207fb3783bbdf3673698f3165d15b0711951ccff1a462d47`  
		Last Modified: Tue, 04 Apr 2023 19:26:09 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b0691a4e698816b9117a35f942736955d0c3d96aceae074d0d6a85b24209c`  
		Last Modified: Tue, 04 Apr 2023 19:26:06 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ffe3c39b524fac736b1c0d5027971d732b7131afb369254f97e35a88a9e658`  
		Last Modified: Tue, 04 Apr 2023 19:26:06 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de09c192195b93c4ad32e5fca3c98e66595ccb03beb0d819798d4a7f4a0cec7`  
		Last Modified: Tue, 04 Apr 2023 19:26:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b8b6327045a98973765523ca3e69faeeb31a0a4b3696622c3577550273975b`  
		Last Modified: Tue, 04 Apr 2023 19:26:07 GMT  
		Size: 1.8 MB (1849040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece662b14f50166823d167189de9d4cc68678529649deafbf8e80361baf8f864`  
		Last Modified: Tue, 04 Apr 2023 19:26:06 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
