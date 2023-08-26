## `python:3-windowsservercore-1809`

```console
$ docker pull python@sha256:adc1640cf88c391ddfad7ec6a852a78dedb039cd4b33271529e004979c1dda65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `python:3-windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull python@sha256:6b9a92eb0950fcabd0d24705142e8b37b1449aadafdeebd4f2a7e73bf5d66cc1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054006992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb14fec969e9ba2ca5a8b5532193087e4bc2a81b1928e2c8f827b4d722406abb`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 05:39:45 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 25 Aug 2023 23:18:56 GMT
ENV PYTHON_VERSION=3.11.5
# Fri, 25 Aug 2023 23:20:56 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Fri, 25 Aug 2023 23:20:57 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Fri, 25 Aug 2023 23:20:58 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 25 Aug 2023 23:20:59 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/9af82b715db434abb94a0a6f3569f43e72157346/public/get-pip.py
# Fri, 25 Aug 2023 23:21:00 GMT
ENV PYTHON_GET_PIP_SHA256=45a2bb8bf2bb5eff16fdd00faef6f29731831c7c59bd9fc2bf1f3bed511ff1fe
# Fri, 25 Aug 2023 23:22:25 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 25 Aug 2023 23:22:26 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de23271364fc31f3fb91fc0f09f6c17a22cf63cae86126d5ff743f9d9d4fdeea`  
		Last Modified: Thu, 10 Aug 2023 05:48:17 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616b48dbc4a748483e901884a4e11e1b0ff0294f57aed725c834d7be186961eb`  
		Last Modified: Fri, 25 Aug 2023 23:23:38 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4aae03ef796fad575133ed90fb173ac72cfb16c39d30c33612276f016d83082`  
		Last Modified: Fri, 25 Aug 2023 23:23:45 GMT  
		Size: 52.3 MB (52339563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5288fab8136f6ef6625b52cbab390415df30ac97b4e79216547328fb321c77`  
		Last Modified: Fri, 25 Aug 2023 23:23:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8209fe0afc1a2a8d60fcc115d36683f1a11cb2048e1860b82963e7c4a29b97`  
		Last Modified: Fri, 25 Aug 2023 23:23:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d0b6b85eaf5bd8175ac22b607282bd7a04d03a965adf1edee58dbbf85c390f`  
		Last Modified: Fri, 25 Aug 2023 23:23:36 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8794e73bcaca5d4c1633e3aaac3923acf41fdfa0068e5889b3379efadddd555`  
		Last Modified: Fri, 25 Aug 2023 23:23:36 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5b0730dd79db4ed89c6f71609e40d7a8e5c19a087c5fd820088cbd829ec490`  
		Last Modified: Fri, 25 Aug 2023 23:23:37 GMT  
		Size: 5.7 MB (5701497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cab5a7c83239520336454fc244e5376c06c7c6c2bd729fc138130c09e6f82c`  
		Last Modified: Fri, 25 Aug 2023 23:23:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
