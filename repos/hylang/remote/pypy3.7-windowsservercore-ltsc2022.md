## `hylang:pypy3.7-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:0af939c8df61d86e7c734404decb31253cc0413c042d2e39c042ff66fabc9c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.587; amd64

### `hylang:pypy3.7-windowsservercore-ltsc2022` - windows version 10.0.20348.587; amd64

```console
$ docker pull hylang@sha256:9e387162d248784c57e2c4c163839f5e6b1c2279d3013f995511576e695cfff9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269670696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a42057bee8c4a3b8087d7d370665e9119f2984f01f35b04b34994cf6b3ccc98`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Mar 2022 19:27:44 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 08 Mar 2022 19:28:39 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 08 Mar 2022 19:28:39 GMT
ENV PYPY_VERSION=7.3.8
# Tue, 08 Mar 2022 19:45:08 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.7-v7.3.8-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '96df67492bc8d62b2e71dddf5f6c58965a26cac9799c5f4081401af0494b3bcc'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.7-v7.3.8-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy3 --version") ...'; 	pypy3 --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 08 Mar 2022 19:45:09 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 08 Mar 2022 19:45:10 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 08 Mar 2022 19:46:37 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 08 Mar 2022 19:46:38 GMT
CMD ["pypy3"]
# Wed, 09 Mar 2022 23:25:51 GMT
ENV HY_VERSION=1.0a4
# Wed, 09 Mar 2022 23:25:51 GMT
ENV HYRULE_VERSION=0.1
# Wed, 09 Mar 2022 23:26:36 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 09 Mar 2022 23:26:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05429111ea1a767be23087b3f6fa1981262988c6d2df8593c80c89c9e2a4e861`  
		Last Modified: Tue, 08 Mar 2022 20:00:30 GMT  
		Size: 598.5 KB (598492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698c85ea3e7dd99853bbb9a33f94d396c7d355a5e77c52e258d46f0f0ce810d4`  
		Last Modified: Tue, 08 Mar 2022 20:00:32 GMT  
		Size: 15.7 MB (15701447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3090b66358b36c375366945149396c4b34fdc1ce3d99f2b6f2040f136e2d994`  
		Last Modified: Tue, 08 Mar 2022 20:00:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7405af58d6b3fbdb4dc9da008ba0edb68bc3dcdffd5246e3de206494e90c51a6`  
		Last Modified: Tue, 08 Mar 2022 20:03:28 GMT  
		Size: 25.6 MB (25630967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4385a8378820c992d1d6f0c8cb6aaf488c65c6361a64a278c07779d0bd3f4ba`  
		Last Modified: Tue, 08 Mar 2022 20:03:20 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc820d8519bb423f1efbdec95a9fb730a2ded03204b0ba3282477b2c278617e0`  
		Last Modified: Tue, 08 Mar 2022 20:03:20 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529a821f8bc6e12170c2fc90dea74470fa9b4de7e84cf6d187aff43663d3b6df`  
		Last Modified: Tue, 08 Mar 2022 20:03:22 GMT  
		Size: 3.0 MB (3002794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce84a67f3f09fe7ee6513c1253d8d0d7ca9590e7252ed1a548d3893df9a40c2f`  
		Last Modified: Tue, 08 Mar 2022 20:03:20 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22bf304b74af54ad479e8aea20dd40bcf55edd7d01c097d8163ce2f9dc05f61`  
		Last Modified: Wed, 09 Mar 2022 23:27:56 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9510c95b86168be34a211f0f7f503cdffd55384bccde7e161326f2a31111ed`  
		Last Modified: Wed, 09 Mar 2022 23:27:56 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a06c94f173bab4eb0a3df504f94594158dd060734afbd8b7a0ffb28efe19a3`  
		Last Modified: Wed, 09 Mar 2022 23:28:00 GMT  
		Size: 3.5 MB (3478658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a760adcbcd6573e79cf3dcbe2d144ec7901c72c625b35b6aff4dd2e1a1a6b393`  
		Last Modified: Wed, 09 Mar 2022 23:27:56 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
