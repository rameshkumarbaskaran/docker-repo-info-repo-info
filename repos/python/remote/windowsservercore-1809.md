## `python:windowsservercore-1809`

```console
$ docker pull python@sha256:39036da73fd9742b6b8365d374074de9a5017ddc3c1cd00119aad3ed2a204fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `python:windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull python@sha256:581cc261a24a8f2e190e55b5722c6f0d29512e9648ca7a726ceb7dad896dc6af
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1707011731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3f7e62e1ed687e713bce17371746aa241e0057009f4643fa9e892a7291cc74`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 05:46:00 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 24 Jun 2023 06:01:52 GMT
ENV PYTHON_VERSION=3.11.4
# Sat, 24 Jun 2023 06:03:18 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Sat, 24 Jun 2023 06:03:19 GMT
ENV PYTHON_PIP_VERSION=23.1.2
# Sat, 24 Jun 2023 06:03:20 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 24 Jun 2023 06:03:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Sat, 24 Jun 2023 06:03:22 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Sat, 24 Jun 2023 06:04:14 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Sat, 24 Jun 2023 06:04:15 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2668a63b8f1889eb75f3d48fcfb2542a7d913199a1bf3d0a27ee68fd8c4a1a3`  
		Last Modified: Sat, 24 Jun 2023 05:52:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acef1c76937d257b0004f7faf7a3a86ff90001cc23b58bdcabe2f2e0f968b89b`  
		Last Modified: Sat, 24 Jun 2023 06:05:47 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ee233337613133df172a4aed6ed8b1ea291118126e5b728b478a864594c789`  
		Last Modified: Sat, 24 Jun 2023 06:05:54 GMT  
		Size: 50.6 MB (50621059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea64f0667433935783dfc58558a1a3eb15195ce0be1976199e3cd23a0fbb46ed`  
		Last Modified: Sat, 24 Jun 2023 06:05:47 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97182a6bb4a0041a492825b81a5e64e2a83ff0df823638ed1709a22245ff1f8d`  
		Last Modified: Sat, 24 Jun 2023 06:05:44 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5227991b89e14eb75d4bd514a826d4d05a432e02990ffec0f674ecdcb2e0e1e4`  
		Last Modified: Sat, 24 Jun 2023 06:05:44 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4317a284a7683e62be7ce118df0f2455a12f0f473a668742ecff7d8df3fb0e9`  
		Last Modified: Sat, 24 Jun 2023 06:05:45 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a36c5e37eeb6ff1155b5cd118985f9ecf3159d4d279ef38adc83140bcd349c`  
		Last Modified: Sat, 24 Jun 2023 06:05:46 GMT  
		Size: 5.6 MB (5642640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16aa07aa24c1f3b5e0aa0f9984c77ff49a7a62c4a5c1964c70e2b7a6ce7ca6a2`  
		Last Modified: Sat, 24 Jun 2023 06:05:44 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
