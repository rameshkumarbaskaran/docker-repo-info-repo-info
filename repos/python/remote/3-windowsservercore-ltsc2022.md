## `python:3-windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:04e49b465fd93e29d8f1817be7c901f5f5ed020b2c87c8bd9681a9aefb83eea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1850; amd64

### `python:3-windowsservercore-ltsc2022` - windows version 10.0.20348.1850; amd64

```console
$ docker pull python@sha256:cdcac0b47cfcc5242052b24e2f403dc914ca1539bd303f3eeea557ba64cbafd2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1793799622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1f01b501f8dcc4f007e82f4b2b97d947120bdf9687ca6ec0d482b803e5d243`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jul 2023 21:29:32 GMT
RUN Install update 10.0.20348.1850
# Thu, 13 Jul 2023 20:29:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Jul 2023 21:17:41 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 13 Jul 2023 21:23:54 GMT
ENV PYTHON_VERSION=3.11.4
# Thu, 13 Jul 2023 21:25:11 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Thu, 13 Jul 2023 21:25:12 GMT
ENV PYTHON_PIP_VERSION=23.1.2
# Thu, 13 Jul 2023 21:25:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Tue, 08 Aug 2023 21:38:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/9af82b715db434abb94a0a6f3569f43e72157346/public/get-pip.py
# Tue, 08 Aug 2023 21:38:23 GMT
ENV PYTHON_GET_PIP_SHA256=45a2bb8bf2bb5eff16fdd00faef6f29731831c7c59bd9fc2bf1f3bed511ff1fe
# Tue, 08 Aug 2023 21:39:10 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 08 Aug 2023 21:39:11 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a7416e1317a892f4786a89c62493b21df55e0e06b82a4bb007cc79df0f949`  
		Last Modified: Tue, 11 Jul 2023 18:03:32 GMT  
		Size: 348.8 MB (348766456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3e3828ab9c4326158b6161915d8bad87619b3107529ab32863eb31b684d127`  
		Last Modified: Thu, 13 Jul 2023 21:07:36 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7fa37abcdee2521f900bc4e19d03de3b47e79a339c580f57aadf23be6644de`  
		Last Modified: Thu, 13 Jul 2023 21:30:21 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4682ae5268190b45b1be3f1c1012e7395bdcc1a111c346fc090ec1ab52fa44`  
		Last Modified: Thu, 13 Jul 2023 21:30:58 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6062a58f91296a75df7048f8fc9e430f9cd96c6f70499749c9435de620ed4d7d`  
		Last Modified: Thu, 13 Jul 2023 21:31:04 GMT  
		Size: 50.7 MB (50736850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc1468b7ac596f8ca31afc28becd97e7be07e8d559e537eca8b416d1cd957f5`  
		Last Modified: Thu, 13 Jul 2023 21:30:57 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05805afa44bd077fadd3376a20ff86f2ebb1a866d79ec5dbeac30a801eefbeb`  
		Last Modified: Thu, 13 Jul 2023 21:30:55 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d26e2d9b9d8a8305ac33a6de47ffb3fd2618b4be654cff5fe0332912fba82e`  
		Last Modified: Tue, 08 Aug 2023 21:42:12 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770c9f65bdd1fbc9b6b4086dd3993db549da875e07a60c28a8a3aaa6ff8e23b1`  
		Last Modified: Tue, 08 Aug 2023 21:42:12 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13e667f7d79cf512099bb89d90de24818a72673e2d49ef27c656013f1b5a64f`  
		Last Modified: Tue, 08 Aug 2023 21:42:14 GMT  
		Size: 5.7 MB (5686257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036195fd9b08953c5e14e270913a35cc859b77a23da58fe029b65e4fa5381719`  
		Last Modified: Tue, 08 Aug 2023 21:42:12 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
