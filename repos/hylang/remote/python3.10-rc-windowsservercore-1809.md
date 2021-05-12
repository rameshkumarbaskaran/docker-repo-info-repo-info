## `hylang:python3.10-rc-windowsservercore-1809`

```console
$ docker pull hylang@sha256:620d1fb0c4afe948bafbbf12fdaa4ccf0be8f0eb92c7139395c01c17b1756f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1935; amd64

### `hylang:python3.10-rc-windowsservercore-1809` - windows version 10.0.17763.1935; amd64

```console
$ docker pull hylang@sha256:14f7b446a8a271de179e984c7a55ffba90dc26fb5d3e056a34bff61a7cf84d97
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2533480098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecb39676cedd3ea4f02d3ffc05dca88cded41afa2447d41608cfe76d7bd9f5d`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 08 May 2021 09:21:48 GMT
RUN Install update 1809-amd64
# Wed, 12 May 2021 12:10:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 May 2021 12:15:16 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 12 May 2021 15:50:24 GMT
ENV PYTHON_VERSION=3.10.0b1
# Wed, 12 May 2021 15:50:25 GMT
ENV PYTHON_RELEASE=3.10.0
# Wed, 12 May 2021 15:52:17 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 12 May 2021 15:52:19 GMT
ENV PYTHON_PIP_VERSION=21.1.1
# Wed, 12 May 2021 15:52:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1954f15b3f102ace496a34a013ea76b061535bd2/public/get-pip.py
# Wed, 12 May 2021 15:52:21 GMT
ENV PYTHON_GET_PIP_SHA256=f499d76e0149a673fb8246d88e116db589afbd291739bd84f2cd9a7bca7b6993
# Wed, 12 May 2021 15:53:18 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 12 May 2021 15:53:19 GMT
CMD ["python"]
# Wed, 12 May 2021 16:26:30 GMT
ENV HY_VERSION=1.0a1
# Wed, 12 May 2021 16:27:11 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 12 May 2021 16:27:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8116de3c91c3f1ef2d6c09b49ef5407c9b4d672896eb3af5182a997c3c5379c9`  
		Size: 756.2 MB (756156286 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5b8861e3624ab787e21ee36b876b374a3b5ec40eed1621cebfe2f81d1c2cda37`  
		Last Modified: Wed, 12 May 2021 12:20:32 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9aa1c8ec0c5a4f42cff7e6de598f0e6cc847b6806a9261b7989f4a96fdbd1f`  
		Last Modified: Wed, 12 May 2021 12:21:24 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e35736f622b24a888ff506b25072db6da63e910c69d22ac23bc23446dfb896e`  
		Last Modified: Wed, 12 May 2021 16:15:50 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ef2915630ae30a85600aeaf688a9ab9f31d3576b505b817030c2a173e24168`  
		Last Modified: Wed, 12 May 2021 16:15:49 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499fc024e9831ac11480d3c548f1ce031dd101428e21ae83a9f1baa53aed7dd9`  
		Last Modified: Wed, 12 May 2021 16:15:58 GMT  
		Size: 51.4 MB (51434429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff53ff90d7647d884529fc0549b12bc96b94c65249b1561922ee0c61e4a3f0c`  
		Last Modified: Wed, 12 May 2021 16:15:47 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bcf6ee4ea3e192effb53d89cd028918f49582f4e3566fb619cc0d393e81eb70`  
		Last Modified: Wed, 12 May 2021 16:15:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b291f1583833275078f65c646531bb71d2f1dc7a1ee65e3bb759a8e0ead322ce`  
		Last Modified: Wed, 12 May 2021 16:15:47 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8669b181bc0466566e96dc44587bce0011b6c26fc99b2d49e9f33b936db828`  
		Last Modified: Wed, 12 May 2021 16:15:54 GMT  
		Size: 6.4 MB (6362305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644c721cb8e2e58f2356f26b87dc51e7ee22ed9f53d64c4465a59440fe57ce32`  
		Last Modified: Wed, 12 May 2021 16:15:47 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8828323a8591f19e32ee837ea494cb8707ac3b4c6366319b74eb6576798bcd2`  
		Last Modified: Wed, 12 May 2021 16:33:13 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b79a44025289cd811955db1cb0f0db6cb48dbcd1604c60823489db294b2c04`  
		Last Modified: Wed, 12 May 2021 16:33:14 GMT  
		Size: 1.2 MB (1180083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87321a2894a4a52498962513e43387c8bc0d4adbf2e109891c26f4629fcc7687`  
		Last Modified: Wed, 12 May 2021 16:33:13 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
