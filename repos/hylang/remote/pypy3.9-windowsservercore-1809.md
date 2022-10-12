## `hylang:pypy3.9-windowsservercore-1809`

```console
$ docker pull hylang@sha256:1119b3b86ee488faedf655257ad72cde6cff705188c20270ef3d4b2380aa314a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `hylang:pypy3.9-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull hylang@sha256:9b712cf5ae2d61926edfbf58f545ff6de0f68093aa1465af934d69006d0825b1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2760717689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6011b80e09ee2a274a097756b4dedc587582a0fa5e7939d8c7b2294854711bff`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 12:08:15 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 12 Oct 2022 12:09:14 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 12:09:14 GMT
ENV PYPY_VERSION=7.3.9
# Wed, 12 Oct 2022 12:10:40 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.9-v7.3.9-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'be48ab42f95c402543a7042c999c9433b17e55477c847612c8733a583ca6dff5'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.9-v7.3.9-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 12:10:41 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 12 Oct 2022 12:10:42 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 12 Oct 2022 12:12:23 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 12:12:24 GMT
CMD ["pypy"]
# Wed, 12 Oct 2022 16:21:03 GMT
ENV HY_VERSION=0.24.0
# Wed, 12 Oct 2022 16:21:04 GMT
ENV HYRULE_VERSION=0.2
# Wed, 12 Oct 2022 16:23:42 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 12 Oct 2022 16:23:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c83b73c5aec906bf29d023824962f606da367af193b8e5236b4b1dcdcb3adde`  
		Last Modified: Wed, 12 Oct 2022 12:34:36 GMT  
		Size: 344.8 KB (344811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648e1068c8429c01c4970044dffd1725b8b0ab79b516f579964e02ad3b19cdec`  
		Last Modified: Wed, 12 Oct 2022 12:34:38 GMT  
		Size: 15.5 MB (15489023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8d589211a79f0eb97496f62eeb4bacd9e1549ee4dbe246146f7b579052b0f5`  
		Last Modified: Wed, 12 Oct 2022 12:34:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6477bafd4f109cc21847c1d3750e35d93e1aa72b44ee02ae3962aeb673e2eb6f`  
		Last Modified: Wed, 12 Oct 2022 12:34:41 GMT  
		Size: 26.4 MB (26358610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4257411a0526693b64209ba6cff222e995ec1a4ada1693e97c07c59e3e212dc`  
		Last Modified: Wed, 12 Oct 2022 12:34:32 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcea7a9397ebab14fb9d595ccfbce6d5094dd48055f8b58ac9806f1d8a3e74e6`  
		Last Modified: Wed, 12 Oct 2022 12:34:32 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b148ead37fcf98b39c6bf08682fa91217c75dc4303fff44312f6c8a5cf709e`  
		Last Modified: Wed, 12 Oct 2022 12:34:34 GMT  
		Size: 3.0 MB (2978960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bceae57e862c25ddf4c35b6b207e63f714ff58f3ab9c66ffb20f6712294e13`  
		Last Modified: Wed, 12 Oct 2022 12:34:32 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210f3b5d140281a12102619815f59067cfdec7f1f7169d9054687993350e62df`  
		Last Modified: Wed, 12 Oct 2022 16:35:59 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15256008df2c68e46fe1cba060b6bb7ab094a246ee376d949ee04f00615aaf91`  
		Last Modified: Wed, 12 Oct 2022 16:35:58 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53002b7cbc704279ff9ae7fc1e62a7aabf3dad67d6e198aaec0b8d0973a8880c`  
		Last Modified: Wed, 12 Oct 2022 16:36:00 GMT  
		Size: 4.4 MB (4371429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cfeaea7d989ce0a7851e30d24a909fce301fc795d96c187c96dff779101cd1`  
		Last Modified: Wed, 12 Oct 2022 16:35:58 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
