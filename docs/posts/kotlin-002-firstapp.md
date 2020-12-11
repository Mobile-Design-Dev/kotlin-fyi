# The First Kotlin App

{!includes/abbrev.md!}

???+ quote "Helpful Resources"

    1. [Setup: Command Line Compiler](https://kotlinlang.org/docs/tutorials/command-line.html)
    2. [Getting Started With Kotlin](https://kotlinlang.org/docs/tutorials/getting-started.html)
    3. [IntelliJ IDEA: Create a new project](https://www.jetbrains.com/help/idea/new-project-wizard.html)
    4. [IntelliJ IDEA: Import a project](https://www.jetbrains.com/help/idea/import-project-or-module-wizard.html#top)

I am assuming you already have the relevant Kotlin development environments (IDE and CLI) setup. If not, my [Setup: Your Development Environments](/posts/kotlin-001-setup/) post is worth scanning first. 

All set? Let's go!

## Using: Kotlin CLI

??? example "CLI Tutorial Walkthrough"

    I followed the [CLI tutorial](https://kotlinlang.org/docs/tutorials/command-line.html#homebrew) with a minor adaptation in message. You can find the code on [GitHub](https://github.com/Mobile-Design-Dev/kotlin-fyi/code/100days/001-hello.kt)

    ```kotlin 
    // Filename: code/100days/001-hello.kt
    fun main() {
        println("Hello, Kotlinverse!!")
    }
    ```

    Now open your terminal of choice, change to the code directory, and let's go exploring! First we need to *compile the source code* using `kotlinc`, the command-line Kotlin compiler.

    ```kotlin
    $ cd code/100days
    $ kotlinc ./001-hello.kt  -d hello.jar
    $ ls
    001-hello.kt    hello.jar
    ```

    This generates the classic JAR file familiar to Java developers. You can use the `jar` command to peek into the generated archive and identify generated classes.

    ```
    $ jar -tvf hello.jar 
    META-INF/MANIFEST.MF
    _001_helloKt.class
    META-INF/main.kotlin_module
    ```

    Now run the code using the `kotlin` command with the class name identified above.

    ```
    $kotlin -classpath hello.jar  _001_helloKt
    Hello, Kotlinverse!!
    ```

    Or, if you are familiar with Java - this is a standard jar file with a defined entry point, so you can also just do this:

    ```
    $java -jar hello.jar 
    Hello, Kotlinverse!!
    ```

??? info "Under The Hood: hello.jar"

    If you're curious about what's in a jar file, you can unpack it using:

    ```
    $jar xvf hello.jar 
    inflated: META-INF/MANIFEST.MF
    inflated: _001_helloKt.class
    inflated: META-INF/main.kotlin_module
    ```
    
    The `MANIFEST.MF` file gives you all the information you need, to figure out what the entry point or `Main-Class` for this archive is. This is what mine looks like - and clearly identifies `_001_helloKt` as the entry point.

    ```
    $ cat META-INF/MANIFEST.MF 
    Manifest-Version: 1.0
    Created-By: JetBrains Kotlin
    Main-Class: _001_helloKt
    ```


## Using: VS Code + CLI

??? example "**Option 1: Use VSCode + CodeRunner **" 

    Type `F1` to get the commands selector, then select `Run Code` to activate the extension. It should open up a built-in terminal and produce output like this:

    ```kotlin
    [Running] cd "/Users/nitya/Documents/GitHub/kotlin-fyi/code/100days/" && kotlinc 001-hello.kt -include-runtime -d 001-hello.jar && java -jar 001-hello.jar

    Hello, Kotlinverse!!

    [Done] exited with code=0 in 3.145 seconds
    ```

??? example "**Option 2: Use VSCode Terminal manually **" 

    If you're a Java developer, the syntax and approach will be very familiar. In fact, if you look at the output of the code runner above, you can spot the commands it uses, to execute the built/run sequence! Or refer to the [Using CLI](#using-cli) section for the standard terminal commands.

    To open the built-in Terminal in VS Code, you can use the "Cmd + `" shortcut on the Mac. There might be other shortcuts available for different environments.

    ## Using: IntelliJ IDEA

    Next, let's explore the richer tooling of IntelliJ IDEA to create a new application (from scratch), and also to work with existing code like the sample above. 

??? question "How can we create a new project?"

    I started with the [Getting Started with IntelliJ IDEA](https://kotlinlang.org/docs/tutorials/jvm-get-started.html) tutorial, building a `HelloKotlinverse` application using the `Console Application` template and default configurations. You can also read the [IntelliJ Guide](https://www.jetbrains.com/help/idea/new-project-wizard.html) for more options and details.

    By default, your project uses the [Gradle](https://gradle.org/) build system with Kotlin DSL. If you open the default boilerplate project, you will see this distribution:

    ```
    .gradle/
    .idea/
    build.gradle.kts
    gradle/
        wrapper/
            gradle-wrapper.jar
            gradle-wrapper.properties
    gradle.properties
    gradlew
    gradlew.bat
    settings.gradle.kts
    src/
        main/
            kotlin/
                main.kt
            resources/
        test/
            kotlin/
                main.kt
            resources/
    ```

    The main file to look at right now is the `src/main/kotlin/main.kt` file which contains this code:

    ```
    fun main(args: Array<String>) {
        println("Hello World!")
    }
    ```

    Yes - the exact code sample we used for exploring CLI usage is the default "Hello World" boilerplate code - except it declares the main function's accepted `args` parameter explicitly. 

    Change the code to send a different message - I went with `Hello Kotlinverse!` for mine - then click the `Run` (green arrow) in the gutter of your editor screen to run the code. You should see something like this (some output eliminated for clarity)

    ```
    1:11:52 PM: Executing task 'MainKt.main()'...

    Starting Gradle Daemon...
    Gradle Daemon started in 815 ms
    > Task :wrapper

    BUILD SUCCESSFUL in 4s
    1 actionable task: 1 executed

    > Task :compileKotlin
    ..
    ..
    Hello Kotlinverse!

    BUILD SUCCESSFUL in 6s
    2 actionable tasks: 2 executed
    1:12:04 PM: Task execution finished 'MainKt.main()'.
    ```

    And that's it! You've validated your IDE install and compiled your first app. In later sections we'll explore the purpose and usage of the various other files and settings in this IDE.


??? question "How can we import and work with existing projects?"

    The short answer is _"it depends!". You can import an existing IDEA project (e.g., move project to new environment), or create it from the source in a version control system, or create it from source files in your local directory. 
    
    Read [this guide](https://www.jetbrains.com/help/idea/import-project-or-module-wizard.html#top) for more on all these options.


## Summary

!!! quote "What we completed here:"
 
    - [X] verified our development environment is setup correctly
    - [X] wrote the basic "Hello, World" equivalent in Kotlin
    - [X] compiled and ran it from command-line (CLI)
    - [X] setup and used the CLI from a different editor (VS Code)
    - [X] imported and ran the code in the IntelliJ IDEA IDE
    - [X] learned to build and run a new app using IntelliJ IDEA

    The ["Referenced Resources"](#the-first-kotlin-app) section at the top of the page lists all the resources used in this segment. 



