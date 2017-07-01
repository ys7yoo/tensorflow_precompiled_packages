# tensorflow_precompiled_packages


# A brief memo for building TensorFlow on OSX

1. install bazel

Bazel installer is here: [https://github.com/bazelbuild/bazel/releases](https://github.com/bazelbuild/bazel/releases)

As of 2017. 7. 1, 0.5.2 is the latest version.
Get it by typing the following code in the Terminal.
```
wget https://github.com/bazelbuild/bazel/releases/download/0.5.2/bazel-0.5.2-installer-darwin-x86_64.sh
chmod 755 bazel-0.5.2-installer-darwin-x86_64.sh
sudo ./bazel-0.5.2-installer-darwin-x86_64.sh
```


2. Get TensorFlow source from 

[https://github.com/tensorflow/tensorflow/releases](https://github.com/tensorflow/tensorflow/releases)

3. Build TensorFlow 

```bash
./configure
bazel build --config=opt //tensorflow/tools/pip_package:build_pip_package
```

