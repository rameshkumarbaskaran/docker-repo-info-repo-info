## `python:windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:b71d391ee3c3b958925c6e87d1701b97a731438783b3b443cb755f2a8d40b645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `python:windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull python@sha256:a5f77c43352fc785909f71e051e88fe271fe2f4607e1f2bcd0d030d3e489e217
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1855407776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a600f3b56ca3efa87c1d6bc4ad4189ed2800aab6b9ed10b4ecf5afbe42633faf`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 05:37:01 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 25 Aug 2023 23:16:29 GMT
ENV PYTHON_VERSION=3.11.5
# Fri, 25 Aug 2023 23:17:52 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Fri, 25 Aug 2023 23:17:54 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Fri, 25 Aug 2023 23:17:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 25 Aug 2023 23:17:56 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/9af82b715db434abb94a0a6f3569f43e72157346/public/get-pip.py
# Fri, 25 Aug 2023 23:17:57 GMT
ENV PYTHON_GET_PIP_SHA256=45a2bb8bf2bb5eff16fdd00faef6f29731831c7c59bd9fc2bf1f3bed511ff1fe
# Fri, 25 Aug 2023 23:18:45 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 25 Aug 2023 23:18:45 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1f72c7c82d86a8708d3fb1408d8d93f310b774e17158726796fa6a3347d693`  
		Last Modified: Thu, 10 Aug 2023 05:47:48 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5f3170caf49faaa58820e2203cc92d93f8033ca45f1c1822b26a43d2c9e3a4`  
		Last Modified: Fri, 25 Aug 2023 23:23:13 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ab55ab21b61b6b79f609ef95e6355e87d055706164487d81d23e013751215c`  
		Last Modified: Fri, 25 Aug 2023 23:23:21 GMT  
		Size: 52.3 MB (52320760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6f16b9d59c6dd08e222d9b8cdd0430e257cdb5e61387539206dfac5ab72fee`  
		Last Modified: Fri, 25 Aug 2023 23:23:13 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cfaafa9da312f2d373b432f8ae2b6d191d8e3a3ee0ffe485466893a7997d7c`  
		Last Modified: Fri, 25 Aug 2023 23:23:11 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41abac8b321947901921ae4318c7fac27ca662fcfd5ec32ba7cae7de1efce9c`  
		Last Modified: Fri, 25 Aug 2023 23:23:12 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43d2acea2f3eb8e6dcf5ef9bf5f0ecb3297772c07e6c82421f03d1c26cdea5f`  
		Last Modified: Fri, 25 Aug 2023 23:23:11 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fd88ab3108debe940cc2ac495a5abd5c4a847ff904edce6e93d2f381954b50`  
		Last Modified: Fri, 25 Aug 2023 23:23:13 GMT  
		Size: 5.7 MB (5711973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00693f2f3c86180470cee79c61d4a7689897ab3dcad25b3fcf329d247c0829e`  
		Last Modified: Fri, 25 Aug 2023 23:23:11 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
