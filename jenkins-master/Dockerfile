FROM    jenkins/jenkins:2.414.3

RUN    echo "JENKINS MASTER"

USER    root
RUN    apt update && apt install -y curl && curl -fsSL https://get.docker.com | sh
RUN    curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl" && chmod +x kubectl && chown jenkins:jenkins kubectl && mv kubectl /usr/local/bin/
RUN    usermod -aG docker jenkins
USER    jenkins
