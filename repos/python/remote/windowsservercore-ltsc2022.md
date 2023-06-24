## `python:windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:b1c4fb60c4999655f9f2e371eaf7c7b1cf7cce5112161a2e0ac26bd97e76663c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `python:windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull python@sha256:7e70906c06566580ba0e1fcc2c5cc54cb45d2ebb4a13d256721087dcfb1ebb5d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1482563362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a583beb0e0e8299d12fde42cfab2c667942364f0b3805e4ec66288e2bda92a`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 05:43:00 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 24 Jun 2023 05:59:22 GMT
ENV PYTHON_VERSION=3.11.4
# Sat, 24 Jun 2023 06:00:46 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Sat, 24 Jun 2023 06:00:47 GMT
ENV PYTHON_PIP_VERSION=23.1.2
# Sat, 24 Jun 2023 06:00:47 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 24 Jun 2023 06:00:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Sat, 24 Jun 2023 06:00:49 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Sat, 24 Jun 2023 06:01:39 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Sat, 24 Jun 2023 06:01:40 GMT
CMD ["python"]
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
	-	`sha256:a83c727fd5157faad7e630186346e8bbbc7ae2e3f1f5452fd27d8c2e8044fedc`  
		Last Modified: Sat, 24 Jun 2023 05:52:04 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d5c8a7cf726544d73d2b3db7d78e57fb8cdea2d2a656af0741a19d28829a84`  
		Last Modified: Sat, 24 Jun 2023 06:05:23 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414e3f5ac3b5f1fa72e2c37d3ebc3a456053318642f0060a168a79bd459a8286`  
		Last Modified: Sat, 24 Jun 2023 06:05:30 GMT  
		Size: 50.6 MB (50604388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1385b4adce9882d88e9a67c51a1af64b6fd54b70e7c63fcc196d86d0688968de`  
		Last Modified: Sat, 24 Jun 2023 06:05:23 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b253be64a09301d6df099668a7c5f3f6612f62317166e6325fdd66ebc061a0e`  
		Last Modified: Sat, 24 Jun 2023 06:05:21 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185ec9f19b76fd3af7e6d5f058c820640236f7c629bddc5a7d4cbb25d2aa0294`  
		Last Modified: Sat, 24 Jun 2023 06:05:21 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a843d6b77d8c41ec89b4db3bba647ddeed27e72929419503dc3a39f951bd84bc`  
		Last Modified: Sat, 24 Jun 2023 06:05:21 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5069bc313a6d99669e9f63387a47b2326b43149e7f9eecd570b962e84d488871`  
		Last Modified: Sat, 24 Jun 2023 06:05:22 GMT  
		Size: 5.6 MB (5649102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecec45b3f952c9403db6d2adac9c773817509a1adfb91785dea777755c7749eb`  
		Last Modified: Sat, 24 Jun 2023 06:05:21 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
