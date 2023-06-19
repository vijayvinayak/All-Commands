# All-Commands



1.	aws sts get-caller-identity: This AWS CLI command is used to retrieve information about the AWS identity making the API request. It returns details about the AWS account and the IAM user or role associated with the credentials used to authenticate the request.
2.	aws eks --region eu-west-1 update-kubeconfig --name cinchy_dev: This AWS CLI command is used to update the kubeconfig file for an Amazon Elastic Kubernetes Service (EKS) cluster. It updates the kubeconfig with the necessary authentication and cluster information to interact with the "cinchy_dev" EKS cluster located in the "eu-west-1" region.
3.	kubectl get pods --kubeconfig ./.kube/config: This command uses kubectl to retrieve information about the pods in the currently configured Kubernetes cluster. The --kubeconfig flag specifies the path to the kubeconfig file that contains the necessary credentials and cluster information.
4.	kubectl get pods: This command retrieves information about the pods in the currently configured Kubernetes cluster using the default kubeconfig file located at ~/.kube/config.
5.	kubectl get svc: This command is used to retrieve information about the services running in the currently configured Kubernetes cluster.
6.	kubectl get deploy -n omni-app-dev: Retrieves information about the deployments in the "omni-app-dev" namespace.
7.	kubectl delete deploy smockin-stub: Deletes the deployment named "smockin-stub" from the default namespace.
8.	kubectl delete deploy smockin-stub -n omni-app-dev: Deletes the deployment named "smockin-stub" from the "omni-app-dev" namespace.
9.	kubectl get deploy -n omni-app-dev: Retrieves information about the deployments in the "omni-app-dev" namespace.
10.	kubectl get deploy: Retrieves information about the deployments in the default namespace.
11.	kubectl get deploy -n omni-app-dev: Retrieves information about the deployments in the "omni-app-dev" namespace.
12.	kubectl get pods -n omni-app-dev: Retrieves information about the pods in the "omni-app-dev" namespace.
13.	kubectl create secret docker-registry wilkoregistrycred --docker-server=registry.gitlab.com --docker-username=wilkouser --docker-password=sungBNUBP-eMaR3SfJ3X -n omni-app-stubs --dry-run=client -o yaml > wilkoregistrycred.yml:


 Creates a secret named "wilkoregistrycred" in the "omni-app-stubs" namespace, containing Docker registry credentials. The command uses the --dry-run=client flag to generate the YAML configuration and saves it to a file named "wilkoregistrycred.yml".
14.	kubectl apply -f wilkoregistrycred.yml: Applies the configuration in the "wilkoregistrycred.yml" file, creating the secret.
15.	kubectl get secrets -n omni-app-stubs: Retrieves information about the secrets in the "omni-app-stubs" namespace.
16.	kubectl get ingress: Retrieves information about the ingresses in the default namespace.
17.	kubectl get ingress -n omni-app-dev: Retrieves information about the ingresses in the "omni-app-dev" namespace.
18.	kubectl delete ingress smockin-stub-ui -n omni-app-dev: Deletes the ingress named "smockin-stub-ui" from the "omni-app-dev" namespace.
19.	kubectl get ingress -n omni-app-dev: Retrieves information about the ingresses in the "omni-app-dev" namespace.
20.	kubectl get svc -n omni-app-dev: Retrieves information about the services in the "omni-app-dev" namespace.
21.	kubectl delete service smockin-stub -n omni-app-dev: Deletes the service named "smockin-stub" from the "omni-app-dev" namespace.
22.	kubectl get svc -n omni-app-dev: Retrieves information about the services in the "omni-app-dev" namespace.
23.	kubectl get deployment -n omni-app-dev: Retrieves information about the deployments in the "omni-app-dev" namespace.
24.	kubectl get ing -n omni-app-stubs -o yaml: This command retrieves information about the ingresses in the "omni-app-stubs" namespace and outputs the result in YAML format.
25.	kubectl get ing -n omni-app-stubs: This command retrieves information about the ingresses in the "omni-app-stubs" namespace.
26.	kubectl edit ing smockin-stub-proxy -n omni-app-stubs: This command opens the specified ingress resource ("smockin-stub-proxy") in an editor, allowing you to modify its configuration. The resource is located in the "omni-app-stubs" namespace.
27.	kubectl get ing -n omni-app-stubs: This command retrieves information about the ingresses in the "omni-app-stubs" namespace after the modification made in the previous command.
28.	kubectl edit ing smockin-stub-proxy -n omni-app-stubs: This command opens the ingress resource ("smockin-stub-proxy") in an editor again, allowing you to further modify its configuration.
29.	kubectl get secret wilkoregistrycred -n omni-app-dev -o yaml | sed s/"namespace: omni-app-dev"/"namespace: omni-app-stubs"/ | kubectl apply -n omni-app-stubs -f -: This command retrieves the YAML representation of the secret named "wilkoregistrycred" in the "omni-app-dev" namespace, replaces the namespace value with "omni-app-stubs" using sed, and then applies the modified YAML to create or update the secret in the "omni-app-stubs" namespace.
30.	kubectl exec -it smockin-stub-67b8c665d4-tf7x2 -n omni-app-stubs sh: This command executes an interactive shell session inside the pod named "smockin-stub-67b8c665d4-tf7x2" in the "omni-app-stubs" namespace.
31.	kubectl get ing -n omni-app-stubs -o yaml: This command retrieves information about the ingresses in the "omni-app-stubs" namespace and outputs the result in YAML format.
32.	kubectl get ing -n omni-app-stubs: This command retrieves information about the ingresses in the "omni-app-stubs" namespace.
33.	kubectl edit ing smockin-stub-proxy -n omni-app-stubs: This command opens the specified ingress resource ("smockin-stub-proxy") in an editor, allowing you to modify its configuration. The resource is located in the "omni-app-stubs" namespace.
34.	kubectl get ing -n omni-app-stubs: This command retrieves information about the ingresses in the "omni-app-stubs" namespace after the modification made in the previous command.
35.	kubectl edit ing smockin-stub-proxy -n omni-app-stubs: This command opens the ingress resource ("smockin-stub-proxy") in an editor again, allowing you to further modify its configuration.
36.	FROM ubuntu:bionic: Sets the base image to Ubuntu Bionic.
37.	USER root: Switches the user to the root user.
38.	RUN apt-get upgrade -y: Upgrades the existing packages in the image.
39.	apt update && apt-get update: Updates the package lists.
40.	apt-get -y install --no-install-recommends: Installs packages without recommended packages.
41.	curl: Command-line tool for making HTTP requests.
42.	wget: Command-line tool for retrieving files over HTTP, HTTPS, and FTP.
43.	git: Version control system for tracking changes in files.
44.	unzip: Utility for extracting compressed files.
45.	postgresql-client: Client package for PostgreSQL database.
46.	ca-certificates: Common CA certificates.
47.	apt-transport-https: Transport package for secure package downloads.
48.	curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip": Downloads the AWS CLI installer.
49.	unzip awscliv2.zip && chmod a+x /aws/install && ./aws/install: Unzips the AWS CLI installer, gives it execute permissions, and runs the installer.
50.	aws --version: Verifies the installation of AWS CLI by displaying its version.
51.	wget https://releases.hashicorp.com/terraform/1.3.4/terraform_1.3.4_linux_amd64.zip: Downloads the Terraform binary.
52.	unzip terraform_1.3.4_linux_amd64.zip && mv terraform /usr/local/bin/: Unzips the Terraform binary and moves it to the /usr/local/bin/ directory.
53.	curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.25.4/bin/linux/amd64/kubectl: Downloads the kubectl binary for managing Kubernetes clusters.
54.	chmod a+x ./kubectl && mv ./kubectl /usr/local/bin/kubectl: Gives execute permissions to the kubectl binary and moves it to the /usr/local/bin/ directory.
55.	curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3: Downloads the Helm installation script.
56.	chmod +x get_helm.sh && ./get_helm.sh: Gives execute permissions to the Helm installation script and runs it.
57.	rm -rv /var/lib/apt/lists/*: Removes package lists.
58.	rm -rf /var/lib/apt/lists.d/*: Removes package lists.
59.	rm -rv /var/cache/apt/archives/*: Removes cached package archives.
60.	apt-get autoremove: Removes automatically installed packages that are no longer required.
61.	apt-get clean: Clears out the local repository of retrieved package files.
62.	apt-get autoclean: Clears out the local repository of retrieved package files, but only removes packages that can no longer be downloaded.
63.	rm *.zip: Removes any remaining zip files.
64.	ls -ltr: Lists the files and directories in the current directory.
65.	RUN find /usr/sbin/* ! -type f -a ! -name nologin -a ! -name setup-proxy -a ! -name sshd -a ! -name start.sh -a ! -name apt -exec rm -rv {} \;: Removes unnecessary files and directories from /usr/sbin/ directory, except for specific files mentioned in the command.
66.	RUN adduser --disabled-password --shell /sbin/nologin --uid 10000 --home /opt/app appuser: Creates a new user named "appuser" with the specified UID (10000), a disabled password, and a non-interactive shell (/sbin/nologin). The home directory is set to /opt/app.
67.	RUN sed -i -r 's/^appuser:!:/appuser:x:/' /etc/shadow: Modifies the /etc/shadow file to change the password field of the "appuser" entry, allowing login with an empty password.
68.	RUN rm -Rf /var/spool/cron /etc/crontabs /etc/periodic: Removes existing cron-related files and directories.
69.	RUN sed -i -r '/^(appuser|root|sshd)/!d' /etc/group: Removes unnecessary user accounts from the /etc/group file, except for "appuser", "root", and "sshd".
70.	RUN sed -i -r '/^(appuser|root|sshd)/!d' /etc/passwd: Removes unnecessary user accounts from the /etc/passwd file, except for "appuser", "root", and "sshd".
71.	RUN sed -i -r '/^appuser:/! s#^(.*):[^:]*$#\1:/sbin/nologin#' /etc/passwd: Changes the login shell of all users except "appuser" to /sbin/nologin in the /etc/passwd file.
72.	ENV sysdirs="/bin /etc /lib /sbin /usr /usr/bin": Sets an environment variable sysdirs to a list of system directories to be used in the following cleanup steps.
73.	RUN find $sysdirs -xdev -type d -exec chown root:root {} \; -exec chmod 0755 {} \;: Sets the ownership and permissions of system directories specified in the sysdirs variable to be owned by root and have permissions 0755 (readable and executable by root).
74.	RUN find $sysdirs -xdev -type f -a -perm /4000 -delete: Removes all setuid files (files with the setuid permission) within the system directories specified in the sysdirs variable.
75.	`` Removes unnecessary files and directories from /sbin/ directory, except for specific files mentioned in the command.
76.	RUN find $sysdirs -xdev \( -name hexdump -o -name chgrp -o -name od -o -name strings -o -name su -o -name ping -o -name netstat -o -name gunzip -o -name nslookup \) -delete: Deletes specific programs (hexdump, chgrp, od, strings, su, ping, netstat
77.	RUN rm -Rf /etc/sysctl* /etc/modprobe.d /etc/modules /etc/mdev.conf /etc/acpi /root /etc/fstab: Removes kernel tunables and various system configuration files and directories.
78.	RUN find $sysdirs -xdev -type l -exec test ! -e {} \; -delete: Deletes broken symbolic links within the system directories specified in the sysdirs variable.
79.	RUN rm -rf /var/lib/apt/lists/*: Removes unwanted cache and package lists from the /var/lib/apt/lists/ directory.
80.	USER appuser: Switches the user context to the "appuser" that was created earlier.
81.	WORKDIR /opt/app: Sets the working directory to /opt/app.
82.	RUN aws --version: Verifies the installed version of AWS CLI.
83.	RUN kubectl version --client: Verifies the installed version of Kubernetes client (kubectl).
84.	RUN terraform --version: Verifies the installed version of Terraform.
85.	RUN psql --version: Verifies the installed version of PostgreSQL client.
86.	RUN helm version --short: Verifies the installed version of Helm.
87.	apt-get update: This command updates the local package index with the latest package information from the repositories.
88.	apt-get install ca-certificates curl gnupg lsb-release: This command installs the necessary dependencies for the Docker installation, including ca-certificates, curl, gnupg, and lsb-release.
89.	mkdir -p /etc/apt/keyrings: This command creates a directory named "keyrings" under the "/etc/apt" directory. This directory will be used to store Docker's GPG key.
90.	curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg: This command downloads Docker's GPG key and saves it as "docker.gpg" in the previously created keyrings directory.
91.	echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null: This command adds the Docker repository to the system's package sources. It creates a file named "docker.list" in the "/etc/apt/sources.list.d" directory and adds a repository line for Docker with the correct architecture and GPG key information.
92.	apt-get update: This command updates the package index again to include the newly added Docker repository.
93.	apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin: This command installs Docker Community Edition (docker-ce), Docker CLI (docker-ce-cli), containerd.io, and the Docker Compose plugin.
94.	apt-cache madison docker-ce: This command displays the available versions of the docker-ce package.
95.	apt-get install docker-ce=5:20.10.17~3-0~ubuntu-jammy docker-ce-cli=5:20.10.17~3-0~ubuntu-jammy containerd.io docker-compose-plugin: This command installs a specific version of docker-ce, docker-ce-cli, containerd.io, and the Docker Compose plugin. In this case, it installs version 20.10.17ubuntu-jammy.
96.	docker -v: This command displays the version of Docker installed on the system.
97.	docker pull openjdk:8: This command pulls the Docker image tagged as "openjdk" with version "8" from the Docker registry. It downloads the image to the local system.
98.	docker images: This command lists the Docker images available on the local system.
99.	docker build -it -d 2a8331246713 /bin/sh: This command attempts to build a Docker image with the ID "2a8331246713" using "/bin/sh" as the build context. The command is invalid as the order of the options is incorrect. The -it and -d options are contradictory.
100.	docker build -i -t -d 2a8331246713 /bin/sh: This command attempts to build a Docker image with the ID "2a8331246713" using "/bin/sh" as the build context. The command is invalid as the order of the options is incorrect. The -i, -t, and -d options should be placed before specifying the build context.
101.	docker build -d 2a8331246713 /bin/sh: This command attempts to build a Docker image with the ID "2a8331246713" using "/bin/sh" as the build context. The -d option is invalid as it is used to detach the build and should not be used in this context.
102.	docker run -it -d 2a8331246713 /bin/sh: This command creates a new Docker container from the image with ID "2a8331246713" and starts it in interactive mode (-it) and detached mode (-d). It runs the "/bin/sh" command inside the container.
103.	docker exec -it 7027519a8fde4e9253011a296b13951ab886bd9aa375602b6ae34361465d6842 /bin/sh: This command starts an interactive shell session inside a running Docker container with the container ID "7027519a8fde4e9253011a296b13951ab886bd9aa375602b6ae34361465d6842".
104.	exit: This command is used to exit the current shell session inside the Docker container and return to the host system.
105.	docker -v: This command displays the version of Docker installed on the system after exiting the container.
106.	docker images: This command lists the Docker images available on the local system after exiting the container.
107.	docker ps: This command lists the running Docker containers.
108.	docker ps -a: This command lists all Docker containers, including those that are not currently running.
109.	docker rm 7027519a8fde: This command removes a Docker container with the ID "7027519a8fde".
110.	ls -a: This command lists all files and directories, including hidden ones, in the current directory on the host system.
111.	docker ps -a: This command lists all Docker containers, including those that are not currently running.
112.	docker images: This command lists the Docker images available on the local system.
113.	docker rm 2a8331246713: This command removes a Docker container with the ID "2a8331246713".
114.	docker login: This command is used to log in to a Docker registry. It prompts for credentials to authenticate the user.
115.	docker registry: This command is incomplete or incorrect. It is not a valid Docker command.
116.	docker -h: This command displays the help information for Docker and provides an overview of available Docker commands and options.
117.	docker config: This command is used to manage Docker configurations, including creating, listing, and removing configurations.
118.	docker inspect: This command is used to obtain detailed information about Docker objects such as containers, images, volumes, networks, etc.
119.	docker inspect --help: This command displays the help information for the docker inspect command, providing details on how to use it and its available options.
120.	docker inspect --type string: This command is incomplete or incorrect. The --type option of the docker inspect command requires a specific Docker object type to be specified, such as container, image, volume, network, etc.
121.	docker inspect config: This command inspects the Docker configuration for the specified object, such as a container, image, volume, or network.
122.	cd /: This command changes the current directory to the root directory ("/").
123.	ls: This command lists the files and directories in the current directory ("/").
124.	ls -a: This command lists all files and directories, including hidden ones, in the current directory ("/").
125.	cd etc: This command changes the current directory to the "/etc" directory.
126.	ls: This command lists the files and directories in the "/etc" directory.
127.	cd docker: This command changes the current directory to the "/etc/docker" directory.
128.	ls: This command lists the files and directories in the "/etc/docker" directory.
129.	ls -a: This command lists all files and directories, including hidden ones, in the "/etc/docker" directory.
130.	cat key.json: This command displays the contents of the "key.json" file.
131.	cd /: This command changes the current directory to the root directory ("/").
132.	cd /opt: This command changes the current directory to the "/opt" directory.
133.	ls: This command lists the files and directories in the "/opt" directory.
134.	cd /: This command changes the current directory to the root directory ("/").
135.	find docker: This command searches for files and directories with the name "docker" starting from the current directory and recursively scans the entire file system. It displays the paths of any matching files or directories found.
136.	find /docker: This command searches for files and directories with the name "docker" starting from the root directory ("/"). It displays the paths of any matching files or directories found.
137.	find config: This command searches for files and directories with the name "config" starting from the current directory. It displays the paths of any matching files or directories found.
138.	cd /: This command changes the current directory to the root directory ("/").
139.	cd ~: This command changes the current directory to the user's home directory.
140.	export sysdirs="...": This command assigns a multi-line string containing various directory paths to the environment variable sysdirs.
141.	/bin \: This line adds the /bin directory path to the sysdirs string.
142.	/etc \: This line adds the /etc directory path to the sysdirs string.
143.	/lib \: This line adds the /lib directory path to the sysdirs string.
144.	/sbin \: This line adds the /sbin directory path to the sysdirs string.
145.	/usr \: This line adds the /usr directory path to the sysdirs string.
146.	/usr/bin \: This line adds the /usr/bin directory path to the sysdirs string.
147.	": This line closes the string assignment for the sysdirs environment variable.
148.	find $sysdirs -xdev \( -name hexdump -o -name chgrp -o -name od -o -name strings -o -name su -o -name ping -o -name netstat -o -name gunzip -o -name nslookup \) -delete: This command searches for specific executables (hexdump, chgrp, od, strings, su, ping, netstat, gunzip, nslookup) within the directories listed in $sysdirs and deletes them. It ensures that these executables are removed from the system.
149.	echo $sysdirs: This command prints the value of the sysdirs environment variable, displaying the multi-line string assigned to it.
150.	ls: This command lists the files and directories in the current directory.
151.	docker pull mcr.microsoft.com/powershell: This command pulls the Docker image tagged as "powershell" from the Microsoft Container Registry (mcr.microsoft.com).
152.	docker images: This command lists the Docker images available on the local system.
153.	docker exec -it eb3172124839: This command is incomplete as it doesn't specify the command to execute within the container or provide a container name or ID.
154.	docker exec -it eb3172124839 /bin/sh: This command starts an interactive shell session inside a running Docker container with the container ID "eb3172124839", running the "/bin/sh" command inside the container.
155.	docker run -it eb3172124839 /bin/sh: This command creates a new Docker container from the image with the ID "eb3172124839" and starts it in interactive mode (-it) with the "/bin/sh" command as the entry point.
156.	docker build -t powershell /home/ubuntu/: This command attempts to build a Docker image with the tag "powershell" using the Dockerfile located in "/home/ubuntu/".
157.	ls: This command lists the files and directories in the current directory.
158.	touch Dockerfile: This command creates an empty file named "Dockerfile" in the current directory.
159.	vi Dockerfile: This command opens the "Dockerfile" in the vi text editor for editing.
160.	docker build -t powershell /home/ubuntu/: This command attempts to build a Docker image with the tag "powershell" using the Dockerfile located in "/home/ubuntu/".
161.	vi Dockerfile: This command opens the "Dockerfile" in the vi text editor for editing.
162.	docker build -t powershell /home/ubuntu/: This command attempts to build a Docker image with the tag "powershell" using the Dockerfile located in "/home/ubuntu/".
163.	vi Dockerfile:The command "vi Dockerfile" opens the file named "Dockerfile" in the vi text editor. Vi is a popular and powerful text editor available on Unix-like systems.
164.	docker build -t powershell /home/ubuntu/: This command attempts to build a Docker image with the tag "powershell" using the Dockerfile located in the "/home/ubuntu/" directory.
165.	vi Dockerfile: This command opens the "Dockerfile" in the vi text editor for editing.
166.	docker build -t powershell /home/ubuntu/: This command attempts to build a Docker image with the tag "powershell" using the Dockerfile located in the "/home/ubuntu/" directory.
167.	vi Dockerfile: This command opens the "Dockerfile" in the vi text editor for editing.
168.	docker build -t powershell /home/ubuntu/: This command attempts to build a Docker image with the tag "powershell" using the Dockerfile located in the "/home/ubuntu/" directory.
169.	vi Dockerfile: This command opens the "Dockerfile" in the vi text editor for editing.
170.	pwd: This command prints the current working directory, which represents the directory you are currently in.
171.	docker build -t powershell /root: This command attempts to build a Docker image with the tag "powershell" using the Dockerfile located in the "/root" directory.
172.	docker images: This command lists the Docker images available on the local system.
173.	docker ps: This command lists the currently running Docker containers.
174.	vi Dockerfile: This command opens the "Dockerfile" in the vi text editor for editing.
175.	docker build -t powershell /root: This command attempts to build a Docker image with the tag "powershell" using the Dockerfile located in the "/root" directory.
176.	vi Dockerfile: This command opens the "Dockerfile" in the vi text editor for editing.
177.	docker build -t powershell /root: This command attempts to build a Docker image with the tag "powershell" using the Dockerfile located in the "/root" directory.
178.	vi Dockerfile: This command opens the "Dockerfile" in the vi text editor for editing.
179.	docker build -t powershell /root: This command attempts to build a Docker image with the tag "powershell" using the Dockerfile located in the "/root" directory.
180.	ls: This command lists the files and directories in the current directory.
181.	vi Dockerfile: This command opens the "Dockerfile" in the vi text editor for editing.
182.	rm Dockerfile: This command removes (deletes) the "Dockerfile" from the current directory.
183.	ls: This command lists the files and directories in the current directory.
184.	touch Dockerfile: This command creates an empty file named "Dockerfile" in the current directory.
185.	ls: This command lists the files and directories in the current directory.
186.	vi Dockerfile: This command opens the "Dockerfile" in the vi text editor for editing.
187.	cat Dockerfile: This command displays the contents of the "Dockerfile" on the terminal.
188.	history: This command displays the command history of the current session.
189.	docker build -t prudhvi /root: This command attempts to build a Docker image with the tag "prudhvi" using the Dockerfile located in the "/root" directory.
190.	docker images: This command lists the Docker images available on the local system.
191.	docker ps: This command lists the currently running Docker containers.
192.	docker rm a253390dfa5d: This command attempts to remove the Docker container with the specified container ID ("a253390dfa5d").
193.	docker rm -f a253390dfa5d: This command forcefully removes the Docker container with the specified container ID ("a253390dfa5d").
194.	ls: This command lists the files and directories in the current directory.
195.	docker ps -a: This command lists all Docker containers, including the stopped ones.
196.	docker rm -f 3e6c1aacf6e1~: This command attempts to remove a Docker container with the specified container ID ("3e6c1aacf6e1~"), but the ID seems to have a typo ("~").
197.	docker rm -f 3e6c1aacf6e1: This command forcefully removes the Docker container with the specified container ID ("3e6c1aacf6e1").
198.	docker rm -f b959cb816c7a: This command forcefully removes the Docker container with the specified container ID ("b959cb816c7a").
199.	docker ps -aa: This command lists all Docker containers, including the stopped and exited ones.
200.	docker ps -a: This command lists all Docker containers, including the stopped and exited ones.
201.	docker images -a: This command lists all Docker images, including the intermediate and dangling ones.
202.	docker images: This command lists the Docker images available on the local system.
203.	docker rm -f mcr.microsoft.com/powershell: This command attempts to forcefully remove a Docker container with the specified container ID or name ("mcr.microsoft.com/powershell"), but it seems like you are trying to remove an image as a container, which is not valid.
204.	docker rm mcr.microsoft.com/powershell: This command attempts to remove a Docker container with the specified container ID or name ("mcr.microsoft.com/powershell"), but it seems like you are trying to remove an image as a container, which is not valid.
205.	docker rmi mcr.microsoft.com/powershell: This command attempts to remove a Docker image with the specified image ID or name ("mcr.microsoft.com/powershell").
206.	docker rmi ubuntu: This command attempts to remove a Docker image with the specified image ID or name ("ubuntu").
207.	docker rmi openjdk: This command attempts to remove a Docker image with the specified image ID or name ("openjdk").
208.	docker images: This command lists the Docker images available on the local system.
209.	docker build -h: This command displays the help information for the docker build command, which provides details on how to use the command and its available options.
210.	docker rmi prudhvi: This command attempts to remove a Docker image with the specified image ID or name ("prudhvi").
211.	docker images: This command lists the Docker images available on the local system.
212.	docker rmi -f 2a8331246713: This command forcefully removes a Docker image with the specified image ID ("2a8331246713").
213.	docker images -a: This command lists all Docker images, including the intermediate and dangling ones.
214.	docker build -h: This command displays the help information for the docker build command, providing details on how to use the command and its available options.
215.	ls: This command lists the files and directories in the current directory.
216.	docker build --compress -t prudhvi /root: This command attempts to build a Docker image named "prudhvi" using the Dockerfile located in the "/root" directory, with the "--compress" option enabled.
217.	docker images: This command lists the Docker images available on the local system.
218.	docker run prudhvi: This command attempts to run a Docker container from the image with the specified image ID or name ("prudhvi"), but it seems you are missing the necessary options and command to run within the container.
219.	docker run -it prudhvi: This command runs a Docker container interactively with a TTY allocated, based on the image with the specified image ID or name ("prudhvi"). This allows you to access and interact with the container's shell or command-line environment.
220.	docker images: This command lists the Docker images available on the local system.
221.	docker run -it prudhvi: This command attempts to run a Docker container interactively with a TTY allocated, based on the image with the specified image ID or name ("prudhvi").
222.	vi Dockerfile: This command opens the Dockerfile in the default text editor.
223.	docker build --compress -t prudhvi2 /root: This command attempts to build a Docker image named "prudhvi2" using the Dockerfile located in the "/root" directory, with the "--compress" option enabled.
224.	docker run -it prudhvi2: This command runs a Docker container interactively with a TTY allocated, based on the image with the specified image ID or name ("prudhvi2").
225.	docker ps: This command lists the running Docker containers.
226.	docker ps -a: This command lists all Docker containers, including the stopped and exited ones.
227.	docker rm -f dfe9a77c5da5: This command attempts to forcefully remove a Docker container with the specified container ID ("dfe9a77c5da5").
228.	docker rm -f 7d1b16ec2feb: This command attempts to forcefully remove a Docker container with the specified container ID ("7d1b16ec2feb").
229.	docker rm -f ff9ccbd5bf99: This command attempts to forcefully remove a Docker container with the specified container ID ("ff9ccbd5bf99").
230.	docker rm -f e1b977ca09d0: This command attempts to forcefully remove a Docker container with the specified container ID ("e1b977ca09d0").
231.	ls: This command lists the files and directories in the current directory.
232.	docker build -t prudhvi2 /root: This command attempts to build a Docker image named "prudhvi2" using the Dockerfile located in the "/root" directory.
233.	docker run -it prudhvi2: This command runs a Docker container interactively with a TTY allocated, based on the image with the specified image ID or name ("prudhvi2").
234.	docker ps: This command lists the running Docker containers.
235.	docker ps -a: This command lists all Docker containers, including the stopped and exited ones.
236.	docker images: This command lists the Docker images available on the local system.
237.	docker pull mcr.microsoft.com/powershell: This command pulls the latest version of the "mcr.microsoft.com/powershell" Docker image from the Docker registry.
238.	docker images: This command lists the Docker images available on the local system.
239.	docker images: This command lists the Docker images available on the local system.
240.	docker ps: This command lists the running Docker containers.
241.	docker ps -a: This command lists all Docker containers, including the stopped and exited ones.
242.	docker exec -it 7438f8581a88 /bin/sh: This command attempts to execute a command inside a running Docker container with the specified container ID ("7438f8581a88"), opening an interactive shell session.
243.	docker run -it 7438f8581a88: This command attempts to run a Docker container interactively with a TTY allocated, based on the image with the specified image ID or name ("7438f8581a88").
244.	docker run -it 4bcdf53ee67b: This command attempts to run a Docker container interactively with a TTY allocated, based on the image with the specified image ID ("4bcdf53ee67b").
245.	docker run -it prudhvi2: This command attempts to run a Docker container interactively with a TTY allocated, based on the image with the specified image ID or name ("prudhvi2").
246.	ls: This command lists the files and directories in the current directory.
247.	docker ps: This command lists the running Docker containers.
248.	docker ps -a: This command lists all Docker containers, including the stopped and exited ones.
249.	docker rm -f bffa37dd3c07: This command attempts to forcefully remove the Docker container with the specified container ID ("bffa37dd3c07").
250.	docker rm -f a298fd990b8e: This command attempts to forcefully remove the Docker container with the specified container ID ("a298fd990b8e").
251.	docker rm -f 7438f8581a88: This command attempts to forcefully remove the Docker container with the specified container ID ("7438f8581a88").
252.	docker rm -f c9fc9b436d1d: This command attempts to forcefully remove the Docker container with the specified container ID ("c9fc9b436d1d").
253.	docker rm -f 04a4455798b3: This command attempts to forcefully remove the Docker container with the specified container ID ("04a4455798b3").
254.	ls: This command lists the files and directories in the current directory.
255.	docker ps: This command lists the running Docker containers.
256.	docker ps -a: This command lists all Docker containers, including the stopped and exited ones.
257.	docker images: This command lists the Docker images on your system.
258.	docker run -it 4bcdf53ee67b: This command attempts to run a Docker container interactively with a TTY allocated, based on the image with the specified image ID ("4bcdf53ee67b").
259.	docker run -it prudhvi2: This command attempts to run a Docker container interactively with a TTY allocated, based on the image with the specified image ID or name ("prudhvi2").
260.	docker images: This command lists the Docker images on your system.
261.	docker run -it prudhvi2: This command attempts to run a Docker container interactively with a TTY allocated, based on the image with the specified image ID or name ("prudhvi2").
262.	docker images: This command lists the Docker images on your system.
263.	docker run -it prudhvi2: This command attempts to run a Docker container interactively with a TTY allocated, based on the image with the specified image ID or name ("prudhvi2").
264.	cd /etc: This command changes the current directory to /etc.
265.	ls: This command lists the files and directories in the current directory (/etc).
266.	cat passwd: This command displays the contents of the file passwd located in the /etc directory.
267.	docker run -it prudhvi2: This command attempts to run a Docker container interactively with a TTY allocated, based on the image with the specified image ID or name ("prudhvi2").
268.	cd /: This command changes the current directory to the root directory.
269.	ls: This command lists the files and directories in the current directory.
270.	cd ~: This command changes the current directory to your home directory.
271.	ls: This command lists the files and directories in your home directory.
272.	vi dockerfile: This command opens the file named "dockerfile" for editing using the vi text editor.
273.	pwd: This command displays the current working directory.
274.	vi dockerfile: This command opens the file named "dockerfile" for editing using the vi text editor.
275.	docker build -t prudhvi3 /root: This command builds a Docker image with the tag "prudhvi3" using the Dockerfile located in the "/root" directory.
276.	docker images: This command lists the Docker images on your system.
277.	docker run -it prudhvi3: This command runs a Docker container interactively with a TTY allocated, based on the image with the tag "prudhvi3".
278.	docker images: This command lists the Docker images on your system.
279.	docker rmi prudhvi3: This command removes the Docker image with the tag "prudhvi3" from your system.
280.	docker images: This command lists the Docker images on your system.
281.	docker build --no-cache -t prudhvi3: This command builds a Docker image with the tag "prudhvi3" while disabling the use of cache during the build process.
282.	docker build --no-cache -t prudhvi3 /root: This command builds a Docker image with the tag "prudhvi3" while disabling the use of cache during the build process, using the Dockerfile located in the "/root" directory.
283.	docker images: This command lists the Docker images on your system.
284.	ls: This command lists the files and directories in the current directory.
285.	rm dockerfile: This command removes the file named "dockerfile".
286.	docker rmi prudhvi3: This command removes the Docker image with the tag "prudhvi3" from your system.
287.	vi Docker: This command opens the file named "Docker" for editing using the vi text editor.
288.	ls: This command lists the files and directories in the current directory.
289.	vi Dockerfile: This command opens the file named "Dockerfile" for editing using the vi text editor.
290.	docker build --no-cache -t prudhvi3 /root: This command builds a Docker image with the tag "prudhvi3" while disabling the use of cache during the build process, using the Dockerfile located in the "/root" directory.
291.	docker images: This command lists the Docker images on your system.
292.	docker run -it prudhvi3: This command runs a Docker container interactively with a TTY allocated, based on the image with the tag "prudhvi3".
293.	ls: This command lists the files and directories in the current directory.
294.	sudo apt-get update && sudo apt-get install -y gnupg software-properties-common: This command updates the package lists for upgrades and installs the packages gnupg and software-properties-common using apt-get.
295.	wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg: This command downloads the GPG key for HashiCorp's apt repository, converts it to binary format, and saves it as /usr/share/keyrings/hashicorp-archive-keyring.gpg.
296.	gpg --no-default-keyring --keyring /usr/share/keyrings/hashicorp-archive-keyring.gpg --fingerprint: This command displays the fingerprint of the GPG key stored in /usr/share/keyrings/hashicorp-archive-keyring.gpg.
297.	echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list: This command adds a new entry to the /etc/apt/sources.list.d/hashicorp.list file, specifying the HashiCorp apt repository with the signed GPG key.
298.	sudo apt update: This command updates the package lists to include the newly added HashiCorp apt repository.
299.	sudo apt-get install terraform: This command installs the Terraform package using apt-get.
300.	terraform --help: This command displays the help information for Terraform.
301.	git: This command checks if Git is installed on your system. If it is installed, it will display the Git version and usage information.
302.	git clone https://github.com/innovationnorway/terraform-azurerm-service-bus.git: This command clones the Git repository located at the given URL (https://github.com/innovationnorway/terraform-azurerm-service-bus.git) to your current directory.
303.	ls: This command lists the files and directories in the current directory.
304.	cd terraform-azurerm-service-bus: This command changes the current directory to the terraform-azurerm-service-bus directory.
305.	ls: This command lists the files and directories in the terraform-azurerm-service-bus directory.
306.	terraform init: This command initializes the Terraform working directory, downloading and configuring the necessary provider plugins and modules.
307.	ls: This command lists the files and directories in the current directory (which is terraform-azurerm-service-bus).
308.	cd terraform-azurerm-service-bus: This command changes the current directory to terraform-azurerm-service-bus.
309.	terraform init: This command initializes the Terraform working directory, downloading and configuring the necessary provider plugins and modules.
310.	terraform validate: This command checks the syntax and validity of the Terraform configuration files in the current directory.
311.	terraform plan: This command generates an execution plan for Terraform, showing the proposed changes to be made based on the current configuration.
312.	docker images: This command lists the available Docker images on your system.
313.	kubectl get pods: This command lists all pods in the default namespace.
314.	kubectl get pods -n default: This command also lists all pods in the default namespace. The -n flag specifies the namespace explicitly.
315.	kubectl run nginx --image=nginx: This command creates a new pod named "nginx" using the "nginx" container image.
316.	kubectl get pods: This command lists all pods in the default namespace, including the newly created "nginx" pod.
317.	kubectl describe pods newpods-kwjpz: This command describes the details of the "newpods-kwjpz" pod.
318.	kubectl get pods newpods-kwjpz -o wide: This command lists the details of the "newpods-kwjpz" pod, including additional information such as IP address and node name.
319.	kubectl get pods: This command lists all pods in the default namespace.
320.	kubectl describe pod webapp: This command describes the details of the "webapp" pod.
321.	kubectl describe pod webapp: This command describes the details of the "webapp" pod again.
322.	kubectl delete pod webapp: This command deletes the "webapp" pod.
323.	kubectl get pods: This command lists all pods in the default namespace after deleting the "webapp" pod.
324.	kubectl run redis --image=redis123 --dry-run=client -o yaml > redis-definition.yaml: This command generates a YAML definition file for creating a pod named "redis" with the "redis123" container image, and it saves the output to "redis-definition.yaml" file.
325.	ls: This command lists the files in the current directory.
326.	kubectl create -f redis-definition.yaml: This command creates a pod using the definition specified in the "redis-definition.yaml" file.
327.	kubectl get pods: This command lists all pods in the default namespace, including the newly created "redis" pod.
328.	cat sample.yaml: This command displays the contents of the "sample.yaml" file.
329.	vi sample.yaml: This command opens the "sample.yaml" file in the vi text editor for editing.
330.	kubectl apply -f sample.yaml: This command applies the configuration specified in the "sample.yaml" file to create or update Kubernetes resources.
331.	ls: This command lists the files in the current directory.
332.	vi redis-definition.yaml: This command opens the "redis-definition.yaml" file in the vi text editor for editing.
333.	kubectl apply -f sample.yaml: This command applies the configuration specified in the "sample.yaml" file to create or update Kubernetes resources.
334.	kubectl create -f redis-definition.yaml: This command creates a pod using the configuration specified in the "redis-definition.yaml" file.
335.	kubectl delete pod redis: This command deletes the pod named "redis".
336.	kubectl create -f redis-definition.yaml: This command creates a pod using the configuration specified in the "redis-definition.yaml" file.
337.	kubectl get replicasets: This command retrieves information about the ReplicaSets in the current namespace.
338.	kubectl describe replicaset: This command provides a detailed description of a specific ReplicaSet. You need to specify the name of the ReplicaSet.
339.	kubectl get pods: This command retrieves information about the pods in the current namespace.
340.	kubectl describe pods new-replica-set-xdlqt: This command provides a detailed description of a specific pod. You need to specify the name of the pod.
341.	kubectl delete pods new-replica-set-xdlqt: This command deletes the pod named "new-replica-set-xdlqt".
342.	kubectl get pods: This command retrieves information about the pods in the current namespace.
343.	cd /root/: This command changes the current directory to the root directory ("/root/").
344.	ls: This command lists the contents of the current directory.
345.	kubectl create -f replicaset-definition-1.yaml: This command creates a ReplicaSet using the configuration specified in the "replicaset-definition-1.yaml" file.
346.	vi replicaset-definition-1.yaml: This command opens the "replicaset-definition-1.yaml" file in the vi editor. You can make modifications to the file in the editor.
347.	kubectl create -f replicaset-definition-1.yaml: This command creates a ReplicaSet using the updated configuration from the "replicaset-definition-1.yaml" file.
348.	kubectl create -f replicaset-definition-2.yaml: This command creates another ReplicaSet using the configuration specified in the "replicaset-definition-2.yaml" file.
349.	vi replicaset-definition-2.yaml: This command opens the "replicaset-definition-2.yaml" file in the vi editor. You can make modifications to the file in the editor.
350.	kubectl create -f replicaset-definition-2.yaml: This command creates a ReplicaSet using the updated configuration from the "replicaset-definition-2.yaml" file.
351.	kubectl get replicasets: This command retrieves information about the ReplicaSets in the current namespace.
352.	kubectl delete replicaset-1 replicaset-2: This command attempts to delete ReplicaSets named "replicaset-1" and "replicaset-2". Please ensure that the correct names of the ReplicaSets are used.
353.	kubectl delete replicaset-1: This command attempts to delete a ReplicaSet named "replicaset-1". Please ensure that the correct name of the ReplicaSet is used.
354.	kubectl delete replicaset-1: This command attempts to delete a ReplicaSet named "replicaset-1". Please ensure that the correct name of the ReplicaSet is used.
355.	kubectl delete replicaset replicaset-1: This command attempts to delete a ReplicaSet named "replicaset-1". Please ensure that the correct name of the ReplicaSet is used.
356.	kubectl delete replicaset replicaset-2: This command attempts to delete a ReplicaSet named "replicaset-2". Please ensure that the correct name of the ReplicaSet is used.
357.	ls: This command lists the contents of the current directory.
358.	kubectl edit replicaset new-replica-set: This command opens the specified ReplicaSet ("new-replica-set") in an editor for modification. Ensure that the ReplicaSet name is correct.
359.	kubectl get pods: This command retrieves information about the pods in the current namespace.
360.	kubectl get replicasets: This command retrieves information about the ReplicaSets in the current namespace.
361.	kubectl edit replicaset new-replica-set: This command opens the specified ReplicaSet ("new-replica-set") in an editor for modification. Ensure that the ReplicaSet name is correct.
362.	kubectl apply replicaset new-replica-set: This command attempts to apply changes to a ReplicaSet named "new-replica-set". Please ensure that the correct name of the ReplicaSet is used and the appropriate YAML configuration is provided.
363.	kubectl apply -f replicaset new-replica-set: This command attempts to apply changes to a ReplicaSet using the "replicaset" and "new-replica-set" as file names or resources. Ensure that the correct command syntax is used and the YAML configuration file is provided.
364.	ls: This command lists the contents of the current directory.
365.	kubectl update replicaset new-replica-set: This command attempts to update a ReplicaSet named "new-replica-set". Please ensure that the correct name of the ReplicaSet is used.
366.	kubectl get pods: This command retrieves information about the pods in the current namespace.
367.	kubctl delete pods new-replica-set-wdvzh: This command attempts to delete a pod named "new-replica-set-wdvzh". Please ensure that the correct name of the pod is used.
368.	kubectl delete pods new-replica-set-wdvzh: This command deletes a pod named "new-replica-set-wdvzh".
369.	kubectl get pods: This command retrieves information about the pods in the current namespace.
370.	kubectl delete pods new-replica-set-bg48n: This command deletes a pod named "new-replica-set-bg48n".
371.	kubectl delete pods new-replica-set-tdmrt: This command deletes a pod named "new-replica-set-tdmrt".
372.	kubectl delete pods new-replica-set-mdcv8: This command deletes a pod named "new-replica-set-mdcv8".
373.	kubectl get pods: This command retrieves information about the pods in the current namespace.
374.	kubectl scale rs new-replica-set --replicas=5: This command scales the ReplicaSet named "new-replica-set" to have 5 replicas.
375.	kubectl get pods: This command retrieves information about the pods in the current namespace.
376.	history: This command displays the command history.
377.	apiVersion: apps/v1
378.	kind: Deployment
379.	metadata:
380.	name: httpd-frontend
381.	spec:
382.	replicas: 3
383.	selector:
384.	matchLabels:
385.	name: httpd-frontend
386.	template:
387.	metadata:
388.	labels:
389.	name: httpd-frontend
390.	spec:
391.	containers:
-	name: httpd-frontend
392.	image: httpd:2.4-alpine
393.	apiVersion: apps/v1: Specifies the API version for the Deployment object.
394.	kind: Deployment: Defines the type of Kubernetes resource as a Deployment.
395.	metadata: Contains metadata information about the Deployment.
396.	name: httpd-frontend: Specifies the name of the Deployment.
397.	spec: Describes the desired state of the Deployment.
398.	replicas: 3: Defines the desired number of replicas for the Deployment.
399.	selector: Specifies the labels used to select the pods managed by the Deployment.
400.	matchLabels: Defines the labels used for selecting the pods.
401.	name: httpd-frontend: Selects pods with the label "name" set to "httpd-frontend".
402.	template: Defines the pod template used by the Deployment to create new pods.
403.	metadata: Contains metadata for the pod template.
404.	labels: Specifies labels for the pods created from the template.
405.	name: httpd-frontend: Sets the label "name" to "httpd-frontend" for the pods.

406.	kubectl get pods: Retrieves information about running pods in the cluster.
407.	kubectl get rs: Lists the ReplicaSets in the cluster.
408.	kubectl get deployments: Displays information about deployments in the cluster.
409.	kubectl describe pods frontend-deployment-6d8c45b946-bk65v: Provides detailed information about a specific pod named "frontend-deployment-6d8c45b946-bk65v".
410.	ls: Lists the files and directories in the current directory.
411.	kubectl create deplotment -f deployment-definition-1.yaml: There's a typo in the command, it should be kubectl create deployment -f deployment-definition-1.yaml. It creates a deployment based on the specified YAML file.
412.	kubectl explain deployment: Provides documentation and explanation of the Deployment resource.
413.	kubectl explain deployment | head -n1: Displays the first line of the explanation for the Deployment resource.
414.	vi deployment-definition-1.yaml: Opens the specified file in the Vi text editor for editing.
415.	kubectl create -f deployment-definition-1.yaml: Creates a deployment based on the specified YAML file.
416.	kubectl get deployments: Lists the deployments in the cluster.
417.	vi deployment.yaml: Opens the specified file in the Vi text editor for editing.
418.	cat deployment: Displays the content of the file named "deployment".
419.	cat deployment.yaml: Displays the content of the file named "deployment.yaml".
420.	kubectl create -f deployment.yaml: Creates a deployment based on the specified YAML file.
421.	kubectl create deployment <name> --image=<image> --replicas=3: Creates a deployment with the specified name, container image, and number of replicas.
422.	kubectl rollout status deployment/myapp-deployment: Checks the status of the rollout for the deployment named "myapp-deployment".
423.	kubectl rollout history deployment/myapp-deployment: Displays the rollout history for the deployment named "myapp-deployment".
424.	kubectl create -f deployment-definition.yml: Creates a deployment based on the YAML file specified in "deployment-definition.yml".
425.	kubectl get deployments: Lists the deployments in the cluster.
426.	kubectl apply -f deployment-definition.yml: Applies the changes in the YAML file specified in "deployment-definition.yml" to the deployment.
427.	kubectl set image deployment/myapp-deployment nginx=nginx:1.9.1: Updates the container image of the deployment named "myapp-deployment" to "nginx:1.9.1".
428.	kubectl rollout status deployment/myapp-deployment: Checks the status of the rollout for the deployment named "myapp-deployment".
429.	kubectl rollout history deployment/myapp-deployment: Displays the rollout history for the deployment named "myapp-deployment".
430.	kubectl rollout undo deployment/myapp-deployment: Rolls back the deployment named "myapp-deployment" to the previous revision.


