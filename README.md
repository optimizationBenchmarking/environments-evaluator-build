# optimizationbenchmarking/evaluator-build

[![Image Size](https://img.shields.io/imagelayers/image-size/optimizationbenchmarking/evaluator-build/latest.svg)](https://hub.docker.com/r/optimizationbenchmarking/evaluator-build/)
[![Image Layers](https://img.shields.io/imagelayers/layers/optimizationbenchmarking/evaluator-build/latest.svg)](https://hub.docker.com/r/optimizationbenchmarking/evaluator-build/)
[![Docker Pulls](https://img.shields.io/docker/pulls/optimizationbenchmarking/evaluator-build.svg)](https://hub.docker.com/r/optimizationbenchmarking/evaluator-build/)
[![Docker Stars](https://img.shields.io/docker/stars/optimizationbenchmarking/evaluator-build.svg)](https://hub.docker.com/r/optimizationbenchmarking/evaluator-build/)

The current version of this image is 0.8.5.

## Components

This environment can be used for building the optimizationBenchmarking evaluator component. It therefore extends the [`optimizationbenchmarking/evaluator-runtime`](https://hub.docker.com/r/optimizationbenchmarking/evaluator-runtime/) environment with the necessary build tools, namely

- [`Apache Ant`](http://ant.apache.org/)
- [`Apache Maven`](http://maven.apache.org/)

We automatically pre-install packages and plugins for Maven which are likely used by our builds.

## Usage

You can run this image by using:

    docker run --rm -t -i optimizationbenchmarking/evaluator-build:<VERSION>
  
to look around in the image.