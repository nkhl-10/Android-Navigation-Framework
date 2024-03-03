# Android-Navigation-Framework-


# [https://developer.android.com/guide/navigation#typesa](Key%20concepts)
* Host
* Graph 
* Controller


# Benefits and features

## The Navigation component provides a number of other benefits and features, including the following:

* Animations and transitions: Provides standardized resources for animations and transitions.
* Deep linking: Implements and handles deep links that take the user directly to a destination.
* UI patterns: Supports patterns such as navigation drawers and bottom navigation with minimal additional work.
* Type safety: Includes the Safe Args Gradle plugin which provides type safety when navigating and passing data between destinations.
* ViewModel support: Enables scoping a ViewModel to a navigation graph to share UI-related data between the graph's destinations.
* Fragment transactions: Fully supports and handles fragment transactions.
* Back and up: Handles back and up actions correctly by default.


# dependency

## To include navigation support in your project, add the following dependencies to your `app's build.gradle` file:
`val navVersion ="2.7.2"
implementation ("androidx.navigation:navigation-fragment-ktx:$navVersion")
implementation ("androidx.navigation:navigation-ui-ktx:$navVersion")`

# [https://developer.android.com/guide/navigation/use-graph/pass-data#Safe-args](Use Safe Args to pass data with type safety)


## The Navigation component has a Gradle plugin called Safe Args that generates simple object and builder classes for type-safe navigation and access to any associated arguments. Safe Args is strongly recommended for navigating and passing data, because it ensures type safety.

## If you are not using Gradle, you can't use the Safe Args plugin. In these cases, you can use Bundles to directly pass data.

## To add Safe Args to your `project`, include the following classpath in your top level `build.gradle` file:

'
buildscript {
    repositories {
        google()
    }
dependencies {
    val nav_version = "2.7.7"
    classpath ("androidx.navigation:navigation-safe-args-gradle-plugin:$nav_version")
    }
}
'
## To generate Java language code suitable for Java or mixed Java and Kotlin modules, add this line to your app or module's build.gradle file:
'plugins {
    id ("androidx.navigation.safeargs")
}'


For more information on how to implement a navigation host and NavController, as well as detail on how they interact with Compose and other UI frameworks, see the following guides:

Create a navigation controller: Outlines how to create a NavController.
Create your navigation graph: Details how to create a navigation host and a navigation graph.
Navigate to a destination: Demonstrates how to use a NavController to move between the destinations in your graph.
