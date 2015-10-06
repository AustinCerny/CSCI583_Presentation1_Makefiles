# Makefile Complaints and Alternatives (cont.)
#
#
* Make is not the only utility for automated building
    * SCons is a common alternative. It uses files written in python which is a more fully featured language than a traditional makefile
    * Many integrated development environments are capable of performing the job of a makefile. Using a makefile with an IDE can potentially become a bottleneck in a software development toolchain. An effective IDE should remove the need for a makefile entirely
* Contiuous Build Tools are also becoming increasingly popular. These tools automatically compile software as it is written. Using these tools can be difficult to set up initially but provide immediate, detailed feedback on system wide perfromance based on local changes.
    * Open source projects that are regularly revised such as Chromium and Mozilla software use continuos build tools
    * Buildbot is a Python based continous build tool