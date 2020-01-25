## `hylang:0-windowsservercore-1809`

```console
$ docker pull hylang@sha256:d8e56c1e4748f2e226a8d44023238b90ec027d9781e78be2df536d0f99e7b78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `hylang:0-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull hylang@sha256:aade3875edfe6ea43cef08ba1c67250f495521fb298fbcf3afc35e83e5fd66a6
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2274814363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa29ece080b5b67e1acae871cd313ab7dc5dd1c783eb31c9cf93db303107880`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 18:21:20 GMT
ENV PYTHON_VERSION=3.7.6
# Wed, 15 Jan 2020 18:21:21 GMT
ENV PYTHON_RELEASE=3.7.6
# Wed, 15 Jan 2020 18:23:56 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Sat, 25 Jan 2020 02:32:53 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Sat, 25 Jan 2020 02:32:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/42ad3426cb1ef05863521d7988d5f7fec0c99560/get-pip.py
# Sat, 25 Jan 2020 02:32:56 GMT
ENV PYTHON_GET_PIP_SHA256=da288fc002d0bb2b90f6fbabc91048c1fa18d567ad067ee713c6e331d3a32b45
# Sat, 25 Jan 2020 02:34:00 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Sat, 25 Jan 2020 02:34:02 GMT
CMD ["python"]
# Sat, 25 Jan 2020 04:28:56 GMT
ENV HY_VERSION=0.17.0
# Sat, 25 Jan 2020 05:06:45 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Sat, 25 Jan 2020 05:06:46 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0075ddccbb615fbc85871d2a0a68a914e7ac78aca3ed104814afa389bca3fa`  
		Last Modified: Wed, 15 Jan 2020 18:42:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e2afa1ef6bd2b3c4303f55af9bc56895a7ed0d99c30466abd4612acaeb8938`  
		Last Modified: Wed, 15 Jan 2020 18:42:25 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fad19f450e99e076a79708f4a96049ddd1e98b7aebe71dfc9d91a93dcee9b72`  
		Last Modified: Wed, 15 Jan 2020 18:42:51 GMT  
		Size: 50.9 MB (50855255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab78f08111b374067e00673867ea7e2d885e75f3850a87358f56e53bd2ed4eb1`  
		Last Modified: Sat, 25 Jan 2020 03:13:55 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d5626c6fd9d913a3b4c40dc1b2d4b04c108a674519da9e664d8c3051daf15b`  
		Last Modified: Sat, 25 Jan 2020 03:13:55 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977e32f6123811842256a39a0402e1a54b77619ef3b7d9bb2c038fa132cfcc18`  
		Last Modified: Sat, 25 Jan 2020 03:13:55 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addfa9fc544754f14cf28c3db789c87ff141bfa201e49165a64dcf731e9a070e`  
		Last Modified: Sat, 25 Jan 2020 03:14:03 GMT  
		Size: 5.4 MB (5350538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cecc3181199d5532c315a889d3d3beb524ff7df7393e588c45d3e9b97610ce4`  
		Last Modified: Sat, 25 Jan 2020 03:13:56 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcb37dbea5ddcb678c6c0cbaffd46a1a1df6ae74aa2408fb2b8696d5d202e8c`  
		Last Modified: Sat, 25 Jan 2020 05:11:47 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3239f0405d97d2114248b0222e3c036d7b2ff2ffdb72b97bc096ffad8eb72f6`  
		Last Modified: Sat, 25 Jan 2020 05:11:49 GMT  
		Size: 1.2 MB (1186671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7496dd9d9387397ba77ea24bc1ac59ad5baf0d3b8ffa66dcafe35e8727bb6f8`  
		Last Modified: Sat, 25 Jan 2020 05:11:47 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
