
        keytool -import -alias <the short name of the server> -file <cert_file_name_you_exported.cer> -keystore cacerts -storepass changeit


# What's this
Included certs files usually used for main maven/sbt/.. repogitories. 

etc:

        https://repo.maven.apache.org
        https://repo1.maven.org/
        https://dl.bintray.com
        https://repo.typesafe.com
        ...


        # How to use:

        $ which java

        Then copy&override the `cacerts` file to your %JAVA_HOME%/jre/lib/security:

        $ cp cacerts %JAVA_HOME%/jre/lib/security/



# Resolve problems like:

        :::: ERRORS
                Server access Error: sun.security.validator.ValidatorException: PKIX path building failed: sun.security.provider.certpath.SunCertPathBuilderException: unable to find valid certification path to requested target url=https://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/sbt/0.13.11/ivys/ivy.xml
