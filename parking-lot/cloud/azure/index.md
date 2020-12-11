# Hello Azure! 

Welcome to the "Azure For Kotlin Developers" section of this site! The objective here is to go from understanding broad cloud computing concepts to actively integrating them using an existing cloud provider - namely Microsoft Azure. 

???+ quote "Hands-On Learning"

    At the end of this [602 Azure](/home/roadmap/#602-microsoft-azure) trail we will know the following:

    - [X] *Introduction* | What is Azure? 
    - [ ] *Architecture* | How do we architect mobile-relevant solutions on Azure?
    - [ ] *Services* | What are the mobile-relevant services and what features do they provide?
    - [ ] *Setup: Account* | How do we setup an Azure account? 
    - [ ] *Setup: Tooling* | How do we setup and use: Azure Portal, Azure CLI, IDE
    - [ ] *Setup: SDK* | How to setup & validate development environment using an Azure SDK
    - [ ] *Quickstart: Services* | How to invoke an Azure service (multiple options) using the SDK
    - [ ] *Tutorial: Basic* | Design and build a simple mobile solution (architecture, multiple services)

??? info "Disclosure"
    I'm a [Senior Cloud Advocate](https://twitter.com/azureadvocates) on the Developer Relations team at Microsoft. I'll use this section to explore Azure support for Kotlin/Android development. [Feedback](/#information) always welcome! I'm maintaining this page in the style of an FAQ. Expand each section for details.

    Welcome to the Azure section of the Cloud integrations trail.

---

## Azure Overview

??? info "Introduction: What is Azure?" 

    Azure is Microsoft's cloud computing and AI platform. It has **200+ products or services** spanning **22 categories** - including `AI+Machine Learning`, `Compute`, `Databases`, `Mobile`, `Security`, `Web`, `Storage` and more. A category contains multiple products, and a product can belong to multiple categories.

    * Website | [Architecture & Solutions](https://azure.microsoft.com/?WT.mc_id=mobile-9644-ninarasi) 
    * Docs | [Services & Categories](https://azure.microsoft.com/en-us/services/?WT.mc_id=mobile-9644-ninarasi)

    *I've identified a subset of services that are likely to be of initial interest to a mobile or web Kotlin developer - and will explore concepts and usage in more detail in th subsections identified in the navigation menu (to left)*

???+ info "Architectures: How do we architect mobile-relevant solutions on Azure"

    A well-architected Azure solution has five pillars:  _cost optimization, operational excellence, performance efficiency, reliability, and security_. This [Learning Path](https://docs.microsoft.com/en-us/learn/paths/azure-well-architected-framework/?WT.mc_id=mobile-9644-ninarasi) teaches you how to build such a solution with Azure.
    
    From a technology area standpoint, architectures are about the components (integrations) and data workflows (interactions) required to implement common app scenarios or workloads on Azure.


    The [Azure Architecture Center](https://docs.microsoft.com/en-us/azure/architecture/?WT.mc_id=mobile-9644-ninarasi) has a rich collection of best practices and patterns for building diverse applications - for different technology areas (or categories) - on Azure.

    The [Build great solutions with the Microsoft Azure well-architected framework] learning path gives a comprehensive overview of the five pillars of a well-architected Azure solution:
    For example: 
     

      * Docs | [Azure Solutions](https://azure.microsoft.com/en-us/solutions/?WT.mc_id=mobile-9644-ninarasi)
      * Docs | [Azure Solutions: Mobile](https://azure.microsoft.com/en-us/solutions/mobile/?WT.mc_id=mobile-9644-ninarasi)
      * Solution | [Build a Task-Based Consumer Mobile App](https://docs.microsoft.com/en-us/azure/architecture/solution-ideas/articles/task-based-consumer-mobile-app?WT.mc_id=mobile-9644-ninarasi)
      * Solution | [Build a Social App for Mobile/Web, with Authentication](https://docs.microsoft.com/en-us/azure/architecture/solution-ideas/articles/social-mobile-and-web-app-with-authentication?WT.mc_id=mobile-9644-ninarasi)

    _Check out the subset of scenarios defined for the [mobile category](https://docs.microsoft.com/en-us/azure/architecture/browse/#mobile).


??? info "Solutions: Where can I use Azure?"

    Solutions describe proven combinations of Azure products and services used to tackle business problems. For example the [Task-Based Consumer Mobile App](https://docs.microsoft.com/en-us/azure/architecture/solution-ideas/articles/task-based-consumer-mobile-app?WT.mc_id=mobile-9644-ninarasi) solution describes the architecture, service components and data flows required to:

     * support authentication with multiple social identity providers
     * store (app) data and sync it later - for offline access
     * send push notifications - for real-time alerts



??? info "SDKs: What are my programming options for Azure?" 

    Azure supports a number of [Languages and Tools](https://docs.microsoft.com/en-us/azure/?product=all#languages-and-tools&WT.mc_id=mobile-9644-ninarasi) out of the box including _Java_, _JavaScript_, _.NET_, _Python_ and _Go_ -- but not yet for Kotlin. View the [latest SDK releases](https://azure.github.io/azure-sdk/releases/latest/index.html&WT.mc_id=mobile-9644-ninarasi) to see the status of product-specific support in that language.

    As a Kotlin developer, it's worth looking at two different releases:

    * [Azure SDK for Java](https://azure.github.io/azure-sdk/releases/latest/java.html) - comprehensive coverage, can be [used with Android API 26+](https://github.com/Azure/azure-sdk-for-java/wiki/Android-Support) or [desugared to API 21](https://github.com/Azure/azure-sdk-for-java/wiki/Android-Support#steps-to-desugar-down-to-api-level-21)
    * [Azure SDK for Android](https://azure.github.io/azure-sdk/releases/latest/android.html) - limited coverage and also in Java, but tailored for Android workflows (API 21+).

    Given that the SDKs use Java, it's worth reviewing the [Kotlin For Android Java developers](https://developer.android.com/kotlin/first) guidance or taking a [related course](http://127.0.0.1:8000/home/roadmap/#102-complete-courses) to figure out how to use existing Java code from your Kotlin app, or migrate the existing Java samples to Kotlin for consistency.


## Azure Services

I use the terms Services and Products interchangeably in this context.


## Azure Quickstart

---

## Learning Resources

??? example "MSDocs: 8 Sites To Bookmark"

    - [Azure Documentation](https://docs.microsoft.com/en-us/azure/?product=featured&WT.mc_id=mobile-9644-ninarasi) 
    * [Azure Architecture Center](https://docs.microsoft.com/en-us/azure/architecture?WT.mc_id=mobile-9644-ninarasi) | [Solutions](https://azure.microsoft.com/en-us/solutions/?WT.mc_id=mobile-9644-ninarasi) 
    * [Getting Started with Azure](https://docs.microsoft.com/en-us/azure/guides/developer/azure-developer-guide?WT.mc_id=mobile-9644-ninarasi)
    * [Mobile Developers Hub](https://docs.microsoft.com/en-us/azure/developer/mobile-apps?WT.mc_id=mobile-9644-ninarasi) | [Solutions](https://azure.microsoft.com/en-us/solutions/mobile/?WT.mc_id=mobile-9644-ninarasi)
    * [Microsoft Learn](https://docs.microsoft.com/en-us/learn/azure/?WT.mc_id=mobile-9644-ninarasi) | [Certifications](https://docs.microsoft.com/en-us/learn/certifications/browse/?products=azure&WT.mc_id=mobile-9644-ninarasi)


???+ example "MSLearn: 15 Learning Paths To Complete"

    Complete this [curated collection](https://docs.microsoft.com/en-us/users/microsoftazuretrainingandcertifications/collections/m6d0hn5nn3edn3?WT.mc_id=mobile-9644-ninarasi) of 15 learning paths (~27 hours). It provides a comprehensive review of Azure fundamentals, data concepts and machine learning usage - also perfect prep for the [AZ-900 Certification](https://docs.microsoft.com/en-us/learn/certifications/exams/az-900?WT.mc_id=mobile-9644-ninarasi) exam.

    - `Azure Fundamentals`
        - [ ] []() | modules
        - [ ] []() | modules
        - [ ] []() | modules
        - [ ] []() | modules
        - [ ] []() | modules
        - [ ] []() | modules
    - `Azure Data Fundamentals`
        - [ ] []() | modules
        - [ ] []() | modules
        - [ ] []() | modules
        - [ ] []() | modules
    - `Azure AI/ML Fundamentals`
        - [ ] []() | modules
        - [ ] []() | modules
        - [ ] []() | modules
        - [ ] []() | modules
        - [ ] []() | modules