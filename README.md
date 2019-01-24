# Kakadu-Java

Kakadu-Java is a Maven project that will build the Kakadu source code and create two Jars: one with the compiled Java code and one with the native Kakadu libraries and binaries. If you run `mvn install -Dkakadu.version=<YOUR_VERSION>` those jars will also be stored in your local Maven repository for use by other projects (built on that same machine).

Since Kakadu is proprietary software, it cannot be distributed by this project. To get the Kakadu source code you will need a license from [Kakadu Software](http://kakadusoftware.com/). Once you've attained a license, they will give you the source code in a Zip file with a name like: v7_A_6-00999N.zip. You can unzip that file into the Kakadu-Java project like so:

    unzip -d /path/to/kakadu-java /path/to/v7_A_6-00999N.zip

Once you've done that you can run the build:

    cd /path/to/kakadu-java
    mvn package -Dkakadu.version=v7_A_6-00999N

You will need to supply the version number as a build parameter. The version number is the same as name of the Zip file you received, and includes the version of the software you have and a unique identifier (the number associated with your particular license).

If there are dependencies that your system doesn't have installed, you'll see a failed build with a message telling you what needs to be installed. Note, this is still a work in progress so not all dependencies are currently checked (i.e., this is an aspirational goal at this point).

## Contact

If you have questions about kakadu-java <a href="mailto:ksclarke@ksclarke.io">feel free to ask</a> or, if you encounter a problem, please feel free to [open a ticket](https://github.com/ksclarke/kakadu-java/issues) in the project's issues queue.
