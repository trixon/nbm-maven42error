# nbm-maven42error
This sample application results in an error when having a dependency
```        <dependency>
            <groupId>org.netbeans.api</groupId>
            <artifactId>org-netbeans-modules-options-api</artifactId>
            <version>${netbeans.version}</version>
        </dependency>
```
in combination with the following call:

        org.openide.awt.Actions.forID("Window", "org.netbeans.modules.options.OptionsWindowAction");

like in Trigger1.java

## Output
```
cd /atlas/data/git/java/nbm-maven42error; JAVA_HOME=/usr/lib/jvm/default /usr/local/netbeans-11.0/java/maven/bin/mvn -DskipTests=true --errors --errors install
Error stacktraces are turned on.
Scanning for projects...
------------------------------------------------------------------------
Reactor Build Order:

nbm-maven42error-parent
nbm-maven42error-branding
nbm-maven42error-sample
nbm-maven42error-app
                                                                        
------------------------------------------------------------------------
Building nbm-maven42error-parent 1.0.0-SNAPSHOT
------------------------------------------------------------------------

--- maven-install-plugin:2.4:install (default-install) @ nbm-maven42error-parent ---
Installing /atlas/data/git/java/nbm-maven42error/pom.xml to /home/pata/.m2/repository/se/trixon/nbm-maven42error-parent/1.0.0-SNAPSHOT/nbm-maven42error-parent-1.0.0-SNAPSHOT.pom
                                                                        
------------------------------------------------------------------------
Building nbm-maven42error-branding 1.0.0-SNAPSHOT
------------------------------------------------------------------------

--- maven-resources-plugin:3.0.2:resources (default-resources) @ nbm-maven42error-branding ---
Using 'UTF-8' encoding to copy filtered resources.
Copying 1 resource

--- maven-compiler-plugin:3.8.1:compile (default-compile) @ nbm-maven42error-branding ---
No sources to compile

--- nbm-maven-plugin:4.2:manifest (default-manifest) @ nbm-maven42error-branding ---
NBM Plugin generates manifest

--- maven-resources-plugin:3.0.2:testResources (default-testResources) @ nbm-maven42error-branding ---
Using 'UTF-8' encoding to copy filtered resources.
skip non existing resourceDirectory /atlas/data/git/java/nbm-maven42error/branding/src/test/resources

--- maven-compiler-plugin:3.8.1:testCompile (default-testCompile) @ nbm-maven42error-branding ---
No sources to compile

--- maven-surefire-plugin:2.19.1:test (default-test) @ nbm-maven42error-branding ---
Tests are skipped.

--- maven-jar-plugin:3.1.2:jar (default-jar) @ nbm-maven42error-branding ---
Building jar: /atlas/data/git/java/nbm-maven42error/branding/target/nbm-maven42error-branding-1.0.0-SNAPSHOT.jar

--- nbm-maven-plugin:4.2:branding (default-branding) @ nbm-maven42error-branding ---
Building jar: /atlas/data/git/java/nbm-maven42error/branding/target/nbm/netbeans/nbmmaven42error/core/locale/core_nbmmaven42error.jar
Building jar: /atlas/data/git/java/nbm-maven42error/branding/target/nbm/netbeans/nbmmaven42error/modules/locale/org-netbeans-core-windows_nbmmaven42error.jar
Building jar: /atlas/data/git/java/nbm-maven42error/branding/target/nbm/netbeans/nbmmaven42error/modules/locale/org-netbeans-core_nbmmaven42error.jar

--- nbm-maven-plugin:4.2:nbm (default-nbm) @ nbm-maven42error-branding ---
Copying module JAR to /atlas/data/git/java/nbm-maven42error/branding/target/nbm/netbeans/nbmmaven42error/modules
Generating Auto Update information for se.trixon.nbm.maven42error.branding
No updater.jar specified, cannot validate Info.xml against DTD
Building jar: /atlas/data/git/java/nbm-maven42error/branding/target/nbm/nbm-maven42error-branding-1.0.0-SNAPSHOT.nbm

--- maven-install-plugin:2.5.2:install (default-install) @ nbm-maven42error-branding ---
Installing /atlas/data/git/java/nbm-maven42error/branding/target/nbm-maven42error-branding-1.0.0-SNAPSHOT.jar to /home/pata/.m2/repository/se/trixon/nbm-maven42error-branding/1.0.0-SNAPSHOT/nbm-maven42error-branding-1.0.0-SNAPSHOT.jar
Installing /atlas/data/git/java/nbm-maven42error/branding/pom.xml to /home/pata/.m2/repository/se/trixon/nbm-maven42error-branding/1.0.0-SNAPSHOT/nbm-maven42error-branding-1.0.0-SNAPSHOT.pom
Installing /atlas/data/git/java/nbm-maven42error/branding/target/nbm-maven42error-branding-1.0.0-SNAPSHOT.nbm to /home/pata/.m2/repository/se/trixon/nbm-maven42error-branding/1.0.0-SNAPSHOT/nbm-maven42error-branding-1.0.0-SNAPSHOT.nbm
                                                                        
------------------------------------------------------------------------
Building nbm-maven42error-sample 1.0.0-SNAPSHOT
------------------------------------------------------------------------

--- maven-resources-plugin:3.0.2:resources (default-resources) @ nbm-maven42error-sample ---
Using 'UTF-8' encoding to copy filtered resources.
Copying 1 resource

--- maven-compiler-plugin:3.8.1:compile (default-compile) @ nbm-maven42error-sample ---
Changes detected - recompiling the module!
Compiling 2 source files to /atlas/data/git/java/nbm-maven42error/nbm-maven42error-sample/target/classes
Supported source version 'RELEASE_7' from annotation processor 'org.netbeans.api.annotations.common.proc.StaticResourceProcessor' less than -source '1.8'
Supported source version 'RELEASE_7' from annotation processor 'org.netbeans.modules.openide.awt.ActionProcessor' less than -source '1.8'
Supported source version 'RELEASE_7' from annotation processor 'org.netbeans.modules.openide.filesystems.declmime.MIMEResolverProcessor' less than -source '1.8'
Supported source version 'RELEASE_6' from annotation processor 'org.netbeans.modules.openide.util.NbBundleProcessor' less than -source '1.8'
Supported source version 'RELEASE_7' from annotation processor 'org.netbeans.modules.openide.util.ServiceProviderProcessor' less than -source '1.8'
Supported source version 'RELEASE_7' from annotation processor 'org.netbeans.modules.openide.util.NamedServiceProcessor' less than -source '1.8'
Supported source version 'RELEASE_7' from annotation processor 'org.netbeans.modules.options.OptionsPanelControllerProcessor' less than -source '1.8'
Supported source version 'RELEASE_7' from annotation processor 'org.netbeans.modules.openide.loaders.DataObjectFactoryProcessor' less than -source '1.8'
Supported source version 'RELEASE_7' from annotation processor 'org.netbeans.modules.templates.TemplateProcessor' less than -source '1.8'
Supported source version 'RELEASE_7' from annotation processor 'org.netbeans.modules.editor.mimelookup.CreateRegistrationProcessor' less than -source '1.8'
Supported source version 'RELEASE_7' from annotation processor 'org.netbeans.modules.openide.nodes.NodesAnnotationProcessor' less than -source '1.8'
Supported source version 'RELEASE_7' from annotation processor 'org.netbeans.modules.openide.windows.TopComponentProcessor' less than -source '1.8'

--- nbm-maven-plugin:4.2:manifest (default-manifest) @ nbm-maven42error-sample ---
NBM Plugin generates manifest
Private classes referenced in module: [org.netbeans.modules.options.OptionsWindowAction]
Project depends on packages not accessible at runtime in module org.netbeans.api:org-netbeans-modules-options-api:jar:RELEASE110
------------------------------------------------------------------------
Reactor Summary:

nbm-maven42error-parent ............................ SUCCESS [  0.125 s]
nbm-maven42error-branding .......................... SUCCESS [  1.414 s]
nbm-maven42error-sample ............................ FAILURE [  0.745 s]
nbm-maven42error-app ............................... SKIPPED
------------------------------------------------------------------------
BUILD FAILURE
------------------------------------------------------------------------
Total time: 3.183 s
Finished at: 2019-06-16T09:45:53+02:00
Final Memory: 30M/490M
------------------------------------------------------------------------
Failed to execute goal org.apache.netbeans.utilities:nbm-maven-plugin:4.2:manifest (default-manifest) on project nbm-maven42error-sample: See above for failures in runtime NetBeans dependencies verification. -> [Help 1]
org.apache.maven.lifecycle.LifecycleExecutionException: Failed to execute goal org.apache.netbeans.utilities:nbm-maven-plugin:4.2:manifest (default-manifest) on project nbm-maven42error-sample: See above for failures in runtime NetBeans dependencies verification.
	at org.apache.maven.lifecycle.internal.MojoExecutor.execute(MojoExecutor.java:212)
	at org.apache.maven.lifecycle.internal.MojoExecutor.execute(MojoExecutor.java:153)
	at org.apache.maven.lifecycle.internal.MojoExecutor.execute(MojoExecutor.java:145)
	at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject(LifecycleModuleBuilder.java:116)
	at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject(LifecycleModuleBuilder.java:80)
	at org.apache.maven.lifecycle.internal.builder.singlethreaded.SingleThreadedBuilder.build(SingleThreadedBuilder.java:51)
	at org.apache.maven.lifecycle.internal.LifecycleStarter.execute(LifecycleStarter.java:128)
	at org.apache.maven.DefaultMaven.doExecute(DefaultMaven.java:307)
	at org.apache.maven.DefaultMaven.doExecute(DefaultMaven.java:193)
	at org.apache.maven.DefaultMaven.execute(DefaultMaven.java:106)
	at org.apache.maven.cli.MavenCli.execute(MavenCli.java:863)
	at org.apache.maven.cli.MavenCli.doMain(MavenCli.java:288)
	at org.apache.maven.cli.MavenCli.main(MavenCli.java:199)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:498)
	at org.codehaus.plexus.classworlds.launcher.Launcher.launchEnhanced(Launcher.java:289)
	at org.codehaus.plexus.classworlds.launcher.Launcher.launch(Launcher.java:229)
	at org.codehaus.plexus.classworlds.launcher.Launcher.mainWithExitCode(Launcher.java:415)
	at org.codehaus.plexus.classworlds.launcher.Launcher.main(Launcher.java:356)
Caused by: org.apache.maven.plugin.MojoFailureException: See above for failures in runtime NetBeans dependencies verification.
	at org.apache.netbeans.nbm.NetBeansManifestUpdateMojo.checkModuleClassPath(NetBeansManifestUpdateMojo.java:759)
	at org.apache.netbeans.nbm.NetBeansManifestUpdateMojo.execute(NetBeansManifestUpdateMojo.java:550)
	at org.apache.maven.plugin.DefaultBuildPluginManager.executeMojo(DefaultBuildPluginManager.java:134)
	at org.apache.maven.lifecycle.internal.MojoExecutor.execute(MojoExecutor.java:207)
	... 20 more

Re-run Maven using the -X switch to enable full debug logging.

For more information about the errors and possible solutions, please read the following articles:
[Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoFailureException

After correcting the problems, you can resume the build with the command
  mvn <goals> -rf :nbm-maven42error-sample
```
