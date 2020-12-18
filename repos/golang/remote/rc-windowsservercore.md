## `golang:rc-windowsservercore`

```console
$ docker pull golang@sha256:368fa1cbb1e613697b246934271ab7294257c5b207564cc9a46447a66c9f8bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `golang:rc-windowsservercore` - windows version 10.0.17763.1637; amd64

```console
$ docker pull golang@sha256:917d62348a74d367def2927124c4a63b1eac5903ea03c18857e2bdf8711786b8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2571389937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443db3a66b8d3a6fcb799a588e6b3f9d7e338d141f88c0d29f7840bd7cfeb26a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 13:30:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Dec 2020 13:30:17 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Dec 2020 13:30:18 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Dec 2020 13:30:18 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Dec 2020 13:30:19 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Dec 2020 13:31:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Dec 2020 13:31:35 GMT
ENV GOPATH=C:\gopath
# Wed, 09 Dec 2020 13:31:57 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Dec 2020 19:15:09 GMT
ENV GOLANG_VERSION=1.16beta1
# Fri, 18 Dec 2020 19:17:54 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.16beta1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'f06e2d7f300843473527e8fdd2d496aef5ffa6507ade0ac1141934e5c6ca7d63'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 18 Dec 2020 19:17:55 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a4372d14958dc8a7eaaace9e4774e7f1db524da5eb4474b5e46738848a3a61a5`  
		Last Modified: Wed, 09 Dec 2020 13:54:38 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea5287e7eabe2989764541d2d84c4676b838a30a6cf7582ae1634e551b3ef2f`  
		Last Modified: Wed, 09 Dec 2020 13:54:39 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588b553e313f50806677aefb0ecff1b14bc3bf2af3502007ed9a8d56a8583fc5`  
		Last Modified: Wed, 09 Dec 2020 13:54:35 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13dbdf38d85835112bbd66c15c88fa10af5cc452590f50bed5c4eb114aef12e9`  
		Last Modified: Wed, 09 Dec 2020 13:54:34 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b50f011f5bd2ab0eaef775ba7b2f9a5fbb8d05f53f675cfb55480847fa80c3`  
		Last Modified: Wed, 09 Dec 2020 13:54:27 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a9000bff3ee5b419217d7c208139db32357708f5e042073232d013021b9648`  
		Last Modified: Wed, 09 Dec 2020 13:54:39 GMT  
		Size: 34.3 MB (34329902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb549abdec7bb8d4debb3e8d9c2220fe8a39c707f3b55ca0041105f451407112`  
		Last Modified: Wed, 09 Dec 2020 13:54:24 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5766c92af76c17356f7a58754b35eef18ba39be13fac5c7122c2fdcf092668de`  
		Last Modified: Wed, 09 Dec 2020 13:54:24 GMT  
		Size: 293.7 KB (293711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8f179bf39ee1a284231c7dac613469dae6e6e48c67a4ef13f64c8ebdbe6e13`  
		Last Modified: Fri, 18 Dec 2020 19:25:57 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844bcc5d8259e13e5a76b03f8ea5fc3281b199ab3d2b136161bfe8661b912473`  
		Last Modified: Fri, 18 Dec 2020 19:26:27 GMT  
		Size: 145.9 MB (145882599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f509515fc55ec6623d48735d9d60a74a961abf3446c13f8906c71688519e6f`  
		Last Modified: Fri, 18 Dec 2020 19:25:58 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-windowsservercore` - windows version 10.0.14393.4104; amd64

```console
$ docker pull golang@sha256:7e619287f762a5190c428e7e200429c9b4b40443dea4b6ace9c52118c0d3d26b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5960665867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4d6f55367e9fcca930f82f901c03d8fc17671f1231c45d828c5ecbcee5056f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 13:34:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Dec 2020 13:34:45 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Dec 2020 13:34:45 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Dec 2020 13:34:46 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Dec 2020 13:34:47 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Dec 2020 13:36:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Dec 2020 13:36:54 GMT
ENV GOPATH=C:\gopath
# Wed, 09 Dec 2020 13:38:10 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Dec 2020 19:18:07 GMT
ENV GOLANG_VERSION=1.16beta1
# Fri, 18 Dec 2020 19:21:42 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.16beta1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'f06e2d7f300843473527e8fdd2d496aef5ffa6507ade0ac1141934e5c6ca7d63'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 18 Dec 2020 19:21:44 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c6d005eb9e78ad42f77f3dad7e29d954e78f0547f9884fe024a71f4042412970`  
		Last Modified: Wed, 09 Dec 2020 13:55:31 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f374b7a81d8d1da3ea2e749c7510b6aa8464f5cf9cfd8635eee23c26c264186`  
		Last Modified: Wed, 09 Dec 2020 13:55:32 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c2e54f8832483cbe5f46ec46fd2932e9656680f47c5811d036e1f9c60f9b79`  
		Last Modified: Wed, 09 Dec 2020 13:55:30 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a357d7b727e3e4efaec8f4443236eb37c1fed68ca863b98d5b19ad17395225`  
		Last Modified: Wed, 09 Dec 2020 13:55:28 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa0785c68a2876dc32a5ff5aea8c9dbaddcea68864db06f5af609f3f65240a9`  
		Last Modified: Wed, 09 Dec 2020 13:55:28 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661765d49c7f605a23d3caa9a99455ce231aa2576dd72ff0b8eab7a5e2ec7ce6`  
		Last Modified: Wed, 09 Dec 2020 13:56:06 GMT  
		Size: 35.1 MB (35137422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4862d1f955bf7fa5325ae4ff054954789b3895bf8fab9ecc625537f8f673abd5`  
		Last Modified: Wed, 09 Dec 2020 13:55:24 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc55fb10a0bab3af9f2e63e7fcb33ba85af44f9e4877a85c0301a6114533edd`  
		Last Modified: Wed, 09 Dec 2020 13:55:26 GMT  
		Size: 5.5 MB (5497159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b102107c2cb3f31d70c5563fd6654e03decaeb040d605537c9e009cab576eb87`  
		Last Modified: Fri, 18 Dec 2020 19:26:44 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce1d187019503a4ffb2c73aaf8506e1eb733277df4014777bb92dfa1cfd1541`  
		Last Modified: Fri, 18 Dec 2020 19:27:14 GMT  
		Size: 151.2 MB (151177993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cded4cb90c9ebaa6a2a8c045fc844cdeeda5fdd281394088fa01c704a3d6792e`  
		Last Modified: Fri, 18 Dec 2020 19:26:44 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
