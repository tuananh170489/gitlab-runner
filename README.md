# Configure gitlab runner
### Download gitlab-runner
```sh
wget --content-disposition https://packages.gitlab.com/runner/gitlab-runner/packages/el/7/gitlab-runner-11.2.0-1.x86_64.rpm/download.rpm
```
### Install gitlab-runner
```sh
rpm -Uvh gitlab-runner-11.2.0-1.x86_64.rpm
```
### Configure gitlab-runner register to gitlab server
```sh
gitlab-runner register --non-interactive --url "$GITLAB_URL" --registration-token "$GITLAB_TOKEN" --executor "shell" --description "$DESCRIPTION" --run-untagged --locked="false"
```
### Start gitlab-runner
```sh
gitlab-runner start
```
