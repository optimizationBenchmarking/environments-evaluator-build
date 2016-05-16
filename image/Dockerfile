#
# optimizationbenchmarking/evaluator-build
#
# This is the image of the build tools needed to build the
# by the elements of the optimizationBenchmarking evaluator.
# We pre-install several required external dependencies and
# maven plugins in order to reduce the build time.
# 
# 
FROM optimizationbenchmarking/evaluator-runtime
MAINTAINER Thomas Weise <tweise@ustc.edu.cn>

RUN export LANG=C.UTF-8 &&\
    apt-get update &&\
    apt-get install -f -y maven=3.0.* wget &&\
    cd /tmp/ &&\
    wget "http://raw.githubusercontent.com/optimizationBenchmarking/utils-build/master/antWebInstallerLinux.sh" &&\
    chmod 755 antWebInstallerLinux.sh &&\
    ./antWebInstallerLinux.sh &&\
    wget http://github.com/optimizationBenchmarking/evaluator-gui/archive/master.zip &&\
    unzip master.zip &&\
    rm -f master.zip &&\
    cd evaluator-gui-master &&\
    ant -DskipTests=true &&\
    apt-get purge -f -y wget &&\
    apt-get clean &&\
    apt-get autoclean -y &&\
    apt-get autoremove -y &&\
    apt-get clean &&\
    rm -rf /tmp/evaluator-gui-master /tmp/antWebInstallerLinux.sh &&\    
    rm -rf /tmp/* /var/tmp/* &&\
    rm -rf /var/lib/apt/lists/* &&\
    rm -f /etc/ssh/ssh_host_*