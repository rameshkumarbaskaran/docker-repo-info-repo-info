## `python:3-windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:10323ba22a7903b334de29b0b043ff0f1a7cc9e6d6f3a6aacda33aa52d2eeb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `python:3-windowsservercore-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull python@sha256:5410b68a622eeebbe077f65c692400b4b301ae95adbf03b3f8eb3917ab47dfed
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1442595967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c832cc0c827e8527d7a16aab027e1f0d7ad98d8eedf7a1c114ebc9c9574eb914`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 07:43:23 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 12 Jan 2023 07:57:05 GMT
ENV PYTHON_VERSION=3.11.1
# Thu, 12 Jan 2023 07:58:33 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Thu, 12 Jan 2023 07:58:34 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Thu, 12 Jan 2023 07:58:35 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 03 Feb 2023 23:19:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1a96dc5acd0303c4700e02655aefd3bc68c78958/public/get-pip.py
# Fri, 03 Feb 2023 23:19:12 GMT
ENV PYTHON_GET_PIP_SHA256=d1d09b0f9e745610657a528689ba3ea44a73bd19c60f4c954271b790c71c2653
# Fri, 03 Feb 2023 23:20:04 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 03 Feb 2023 23:20:05 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6837a2484af0433279c99af51c3edc897149af0c8ec24d303f2bbc972494655`  
		Last Modified: Thu, 12 Jan 2023 08:33:53 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1d510e7c4e75f1c4eb3d5afa95f58deef9ec018ec3cc4170ed84c6b3f3eb2b`  
		Last Modified: Thu, 12 Jan 2023 08:37:55 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08f825910eb204e5c605d57ce56deecbb91ae6837c5e5a07fbe5289bbaea0ac`  
		Last Modified: Thu, 12 Jan 2023 08:38:03 GMT  
		Size: 50.6 MB (50642051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e344ccbd21a3ca1b1f076f965b67077af4cc2505b2432a3d010059d6a0194c4`  
		Last Modified: Thu, 12 Jan 2023 08:37:55 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9167b0a9a3a810f5eb8a4e4c4c88036280597aa9bf68ee54264652bdd40de483`  
		Last Modified: Thu, 12 Jan 2023 08:37:53 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a27661f291a716ab4bde60cbeb6c80cc011e63aa01405cede30b81f824e24a`  
		Last Modified: Sat, 04 Feb 2023 00:18:24 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb5ba5f937468a440a4c696e0e29aa016b2a10c2dbb36e368cff56aad2292f5`  
		Last Modified: Sat, 04 Feb 2023 00:18:24 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e3eda2d790a7b72655b33bfe558d215d773204701204e82edc46a51dd56daa`  
		Last Modified: Sat, 04 Feb 2023 00:18:26 GMT  
		Size: 5.9 MB (5913464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bb61143d1b7b0dcf2d00b403d6bbac9cc47d82054fc2c77334e8ea396fd320`  
		Last Modified: Sat, 04 Feb 2023 00:18:24 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
