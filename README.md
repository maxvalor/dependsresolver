# Cazel
The bazel is a great build tool from google, but a lot of projects do not support being built by it. We can only build these projects by cmake. Since I like the repo management function of bazel so much, I write this tool - cazel, which seems like a "cmake" takes suits of "bazel", to make the cmake manage depends of project like what bazel does. With this, you can easily get depends from several git repo and build then automatically. 

# Install
Install cazel with:

    sudo apt install jq
    git clone https://github.com/maxvalor/cazel cazel
    cd cazel
    sudo ./install.sh

And you can uninstall it with:

    sudo ./install.sh -u

# How To Use
Build the sample with:

    cazel sync mini_ros_sample
    cazel build mini_ros_sample sample

Or you can simply build it with:

    cazel auto mini_ros_sample

Clean the build files with:

    cazel clean mini_ros_sample

Execute the binary file with:

    cazel exec mini_ros_sample sample
