<div align="center">
    <img alt="logo" data-is-relative="true" src="./assets/img/logo.png" width="250" height="250"/>
    <h1>dbt-toolkit-continued 🧰</h1>
    <img alt="GitHub Workflow Status" src="https://github.com/moseswynn/dbt-toolkit/actions/workflows/build.yml/badge.svg?branch=main">
</div>

<br>

> [!WARNING]
> This is a  fork of [ramonvermeulen/dbt-toolkit](https://github.com/ramonvermeulen/dbt-toolkit), which has been archived by its original author. The goal of this fork is to continue supporting new dbt and JetBrains IDE versions and accept community contributions.

![Lineage Example](./assets/img/sample.gif)

<!-- Plugin description -->
The dbt-toolkit is a plugin designed to enhance your experience working with [**dbt-core**](https://github.com/dbt-labs/dbt-core)
projects within JetBrains IDEs. It currently supports lineage rendering, dbt documentation, compiled SQL preview, and more!
Providing a more streamlined and integrated approach to managing your dbt projects in Jetbrains IDEs. The dbt-toolkit is inspired by the
well-known VSCode plugin [**vscode-dbt-power-user**](https://github.com/AltimateAI/vscode-dbt-power-user), and aims to become an alternative
for JetBrains IDEs.

> _Note: For larger dbt projects (e.g. hundreds of models) the performance might not be as good._


## Features
* **Lineage Rendering**: Visualize the dependencies and relationships between your dbt models directly in your IDE. 
This feature helps you understand the impact of changes and the flow of data in your project. Besides that it offers a 
quicker way to navigate through your dbt project.
* **dbt Documentation**: Access your dbt documentation within your IDE, eliminating the need to constantly switch between
   your browser and IDE.
* **Preview compiled SQL**: Preview the compiled SQL of a dbt model quickly in your IDE, and recompile a single model on
  the fly.
* **Preview data**: Preview the output data of a dbt model directly in your IDE.

## Prerequisites
* For IntelliJ users, it is required to have the [**Python**](https://plugins.jetbrains.com/plugin/631-python) plugin installed so that you can configure a venv via:
<br>`File` > `Project Structure` > `SDK` > `Select Python` > `Select New Virtual Environment`
<br>![Set-up venv](./assets/img/settings.jpg)
* It is recommended to install [**dbt-core**](https://pypi.org/project/dbt-core/) and the required adapters within the configured venv.
* Supported/Tested dbt versions are: `>=1.7.0`

If there is a venv configured within the IDE, the plugin will automatically try to use the dbt executable from the venv. 
If there is no venv configured the plugin will use the globally installed dbt version.

## Installation
Install from disk by downloading the latest zip from the [releases page](https://github.com/moseswynn/dbt-toolkit/releases) and choosing `Install Plugin from Disk` in the IDE plugin settings.

## Setting environment variables
If your dbt project requires environment variables (e.g. `DBT_SOME_ENV_VAR`), please set them via the plugin settings.
`File` > `Settings` > `dbtToolkit` > `Environment Variables`

There is also support for `.env` files, the plugin automatically checks for a `.env` file in the root of your project.
Via the plugin settings, you can also specify a custom path to the `.env` file.
> _Note: The global plugin environment variables will overwrite any environment variable with the same key in your 
> `.env` files_
<!-- Plugin description end -->

## Releases
Releases can be found under the repository's [releases section](https://github.com/moseswynn/dbt-toolkit/releases).
To install, download the zip file (e.g. `dbt-toolkit-continued-<version>.zip`) and in the IDE Plugin window choose `Install from disk`.

## Feedback and Contributions
Feel free to report bugs, issues, or suggest features through the GitHub repository's issue tracker.

## Troubleshooting
Experiencing issues after upgrading the plugin? Try deleting your `.idea/dbtToolkitSettings.xml` file. If you're still experiencing 
problems, feel free to open a GitHub issue.

---
Originally based on the [IntelliJ Platform Plugin Template][template]. Forked from [ramonvermeulen/dbt-toolkit](https://github.com/ramonvermeulen/dbt-toolkit).

[template]: https://github.com/JetBrains/intellij-platform-plugin-template
