# Setup: Your Development Environments

{!includes/abbrev.md!}

???+ quote "Helpful Resources"

    1. [About IntelliJ IDEA](https://www.jetbrains.com/idea/)
    2. [Setup: IntelliJ IDEA](https://kotlinlang.org/docs/tutorials/jvm-get-started.html)
    3. [Setup: Command Line Compiler](https://kotlinlang.org/docs/tutorials/command-line.html)
    4. [Setup: Eclipse](https://kotlinlang.org/docs/tutorials/getting-started-eclipse.html)
    5. [Setup: Learners Guides](https://www.jetbrains.com/help/education/learner-start-guide.html)
    6. [About: Android Studio IDE](https://developer.android.com/studio/)
    7. [StackOverflow: Android Studio vs. IntelliJ](https://stackoverflow.com/questions/30779596/difference-between-android-studio-and-intellij-idea-with-plugins)
    8. [JetBrains Toolbox App](https://www.jetbrains.com/toolbox-app/)
    9. [EduTools Plugin](https://www.jetbrains.com/help/education/install-edutools-plugin.html)
    10. [Getting Started With Kotlin](https://kotlinlang.org/docs/tutorials/getting-started.html)
    11. [Manage multiple IDEs & Releases with Toolbox App](https://blog.jetbrains.com/blog/2019/01/17/toolbox-app-1-13-with-android-studio/)
    12. [VSCode: Kotlin Language Plugin](https://marketplace.visualstudio.com/items?itemName=mathiasfrohlich.Kotlin)
    13. [VSCode: Code Runner plugin](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)
    14. [VSCode: Setup for Kotlin Development](https://kotlin-code.com/ide/visual-studio-code/setup/)


## 1. Introduction

!!! question "What are my development environment options?"

Kotlin offers [multiple options](https://kotlinlang.org/docs/tutorials/getting-started.html) for development environments:

 - [IntelliJ IDEA](https://kotlinlang.org/docs/tutorials/jvm-get-started.html) - preferred JetBrains IDE
 - [Command Line Compiler](https://kotlinlang.org/docs/tutorials/command-line.html) - pairs well with a text editor
 - [Eclipse](https://kotlinlang.org/docs/tutorials/getting-started-eclipse.html) - likely familiar to Java devs

!!! question "Which one should I use?"

After some research, I recommend the following:

 * **Install the JetBrains Toolbox App** to manage multiple IDE versions (stable, canary releases) or variations. This was a popular [developer suggestion on StackOverflow](https://stackoverflow.com/questions/30779596/difference-between-android-studio-and-intellij-idea-with-plugins) especially when you start moving to Android Studio for native development.

 * **Use IntelliJ when you first get started.** It's maintained & recommended by JetBrains ("go where the devs are") and has built-in [Learners Guides](https://www.jetbrains.com/help/education/learner-start-guide.html) that help you skill up fast. This was also the basis for the Android Studio IDE, so it makes the transition there easier.

 * **Setup the Command Line Compiler if you can.** If you love text editors or environments like VS Code, this is a fast and lightweight way to write/test basic code. The syntax will be familiar to Java devs, and you can apparently [run scripts](https://kotlinlang.org/docs/tutorials/command-line.html#using-the-command-line-to-run-scripts) though I haven't tried it.

## 2. IntelliJ IDEA: Setup

!!! tip "Use JetBrains Toolbox Approach"

I'd previously installed Android Studio and IntelliJ IDEA manually. Now, I simply uninstalled those versions and reinstalled them via [Toolbox App](https://www.jetbrains.com/toolbox-app). The ability to [manage multiple IDEs and releases](https://blog.jetbrains.com/blog/2019/01/17/toolbox-app-1-13-with-android-studio/) from one dashboard, is priceless! _Use the Toolbox App to install IDEA and Android Studio IDEs_

!!! tip "Install the EduTools Plugin"

The [EduTools Plugin](https://www.jetbrains.com/help/education/install-edutools-plugin.html) allows us to explore learning guides (e.g., [Kotlin Koans](https://www.jetbrains.com/help/education/learner-start-guide.html)) directly from the IDE - which also has the benefit of giving you more familiarity with IDE features and tooling, as you practice. _Don't forget to restart the IDE after installing the plugin!_

## 2. Kotlin CLI: Setup

!!! tip "Install the Command Line Compiler"

You have two options: 

 * **1. Reuse from IDEA:** If you had previously installed IntelliJ IDEA, the compiler is already installed in your development environment. You just need to update your `PATH` to make it accessible from external terminals. Read more [in this StackOverflow response](https://stackoverflow.com/questions/50636898/how-to-setup-the-kotlin-compiler). _Note: If you installed the IDE using the Toolbox App, the location is different. Look for: `/Users/<username>/Library/Application Support/JetBrains/Toolbox/apps/IDEA-C/ch-0/203.5981.155/IntelliJ IDEA CE.app/Contents/plugins/Kotlin/kotlinc/bin`_ where `<username>` is your Mac login.

 * **2. Install from scratch:** Follow [this tutorial](https://kotlinlang.org/docs/tutorials/command-line.html). On Mac, I used the [Homebrew](https://kotlinlang.org/docs/tutorials/command-line.html#homebrew) install since it makes it easier to manage updates later with `brew upgrade kotlin`. This also takes care of installing the `openjdk` dependency by default - if you want to use _that_ JDK installation as your default, the install process also provides a `PATH` update recommendation.

!!! tip "Configure Visual Studio Code to use the CLI"

You can also now use it with a text editor or IDE - including my favorite: VS Code. VS Code has community-built extensions to support Kotlin CLI usage - but you won't get the rich tooling of IntelliJ IDEA. Instead, you get a lightweight way to do quick code fixes, command-line builds and deploys, while staying within your familiar IDE.

I followed [the approach recommended here](https://kotlin-code.com/ide/visual-studio-code/setup/) to setup my VS Code:

 * Install the [Kotlin Language Plugin](https://marketplace.visualstudio.com/items?itemName=mathiasfrohlich.Kotlin)
 * Install the [Code Runner plugin](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)
 * Verify you have `java` and `kotlin` binaries accessible at command line. 
    
Now, open your Kotlin text file (e.g., `test.kt`) in VS Code. The [Kotlin Language](https://marketplace.visualstudio.com/items?itemName=mathiasfrohlich.Kotlin) extension activates syntax highlighting and code snippets.

You now have two options to build and run your code:
 
 1. Open the VS Code terminal and use `kotlinc ` directly.
 2. Use shortcut `Ctrl+Alt+N` or `F1 => Run Code` to activate CodeRunner to do this for you.


!!! tip "Validate CLI usage with a simple program"

Revisit the [CLI tutorial](https://kotlinlang.org/docs/tutorials/command-line.html#homebrew) and run your first program. Check out my ["First App" post](/posts/kotlin-002-firstapp/) for more details.