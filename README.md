<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Ibel</h3>
  <p align="center">
    A suite of open source business apps!
    <br />
    <a href="https://docs.ibel.app"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://demo.ibel.app">View Demo</a>
    ·
    <a href="https://github.com/Ibel-technology/ibel/issues">Report Bug</a>
    ·
    <a href="https://github.com/Ibel-technology/ibel/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About Ibel</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About Ibel

[![Product Name Screen Shot][product-screenshot]](https://example.com)

Ibel is a suite of web based open source business apps.

The main Ibel Apps include an <a href="https://www.ibel.app/page/crm">Open Source CRM</a>,
<a href="https://www.ibel.app/page/website-builder">Website Builder</a>,
<a href="https://www.ibel.app/page/e-commerce">eCommerce</a>,
<a href="https://www.ibel.app/page/warehouse">Warehouse Management</a>,
<a href="https://www.ibel.app/page/project-management">Project Management</a>,
<a href="https://www.ibel.app/page/accounting">Billing &amp; Accounting</a>,
<a href="https://www.ibel.app/page/point-of-sale">Point of Sale</a>,
<a href="https://www.ibel.app/page/employees">Human Resources</a>,
<a href="https://www.ibel.app/page/lead-automation">Marketing</a>,
<a href="https://www.ibel.app/page/manufacturing">Manufacturing</a>,
<a href="https://www.ibel.app/#apps">...</a>

Ibel Apps can be used as stand-alone applications, but they also integrate seamlessly so you get a full-featured <a href="https://www.ibel.app">Open Source ERP</a> when you install several Apps.


### Built With

Ibel is a new <a href="https://github.com/odoo/odoo">Odoo</a> distribution created by <a href="https://github.com/Ibel-technology">Ibel technology</a> from <a href="https://github.com/OCA/OCB">Odoo Community Backport (OCB)</a> and a collection of open source community modules gathered in the <a href="https://github.com/Ibel-technology/ibel_addons">ibel_addons</a> repository. These add-ons improve the user interface and fill in the features missing in Odoo community edition. Ibel even adds features that do not exist in Odoo enterprise.

Ibel therefore wants to be a 100% open source alternative to Odoo enterprise.
* [ibel](https://github.com/Ibel-technology/ibel)
* [ibel_addons](https://github.com/Ibel-technology/ibel_addons)


<!-- GETTING STARTED -->
## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Prerequisites

This is an example of how to list things you need to use the software and how to install them.
* npm
  ```sh
  npm install npm@latest -g
  ```

### Installation

#### configure Git & Fetch the source 
##### Install & configure Git

The very first step of the installation process is to install the git version control system because the Ibel source code is managed on GitHub. Once installed, you can set your name and email:
```bash
   $ sudo apt install git
   $ git config --global user.name "Your full name"
   $ git config --global user.email "xyz@ibel.app"
   ```
##### Fetch the sources 
All the Odoo sources will be located in $HOME/src/
```sh
   $ mkdir -p $HOME/src
   $ cd $HOME/src
   $ git clone https://github.com/Ibel-technology/ibel.git -b 14.0 --single-branch --depth 1
   $ git clone https://github.com/Ibel-technology/ibel_addons.git -b 14.0 --single-branch --depth 1
   ```
#### Install the dependencies

##### Install wkhtmltopdf

wkhtmltopdf is a library to render HTML into PDF. Odoo uses it to create PDF reports. wkhtmltopdf is not installed through pip and must be installed manually in version 0.12.5 to support headers and footers.
```sh
   $ sudo apt install gdebi
   $ cd /tmp/
   $ sudo wget https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.focal_amd64.deb
   $ sudo gdebi --n wkhtmltox_0.12.5-1.focal_amd64.deb
   $ sudo ln -s /usr/local/bin/wkhtmltopdf /usr/bin
   $ sudo ln -s /usr/local/bin/wkhtmltoimage /usr/bin
   ```
##### Right-to-left interface support
In order to support right-to-left (RTL) languages, we need rtlcss to convert the CSS files:
```sh
   $ sudo apt-get install nodejs npm
   $ sudo npm install -g rtlcss
   ```

##### Install Postgresql

Ibel uses PostgreSQL as database management system. Use your package manager to download and install PostgreSQL (supported version: 10.0 and later).

On Debian/Unbuntu, it can be achieved by executing the following:
```sh
   $ sudo apt install postgresql postgresql-client
   ```
By default, the only user is postgres but Odoo forbids connecting as postgres, so you need to create a new PostgreSQL user:
```sh
   $ sudo -u postgres createuser -s $USER
   $ createdb $USER
   ```
*****Note:***** Because your PostgreSQL user has the same name as your Unix login, you will be able to connect to the database without password.

##### Python
Odoo requires Python 3.6 or later, if your computer is up-to-date you should already be at this version or higher.

You can check your Python version with:
```sh
   $ python3 --version
   ```

##### Install pip3 and libraries
For libraries using native code, installation of development tools and native dependencies is required before installing the Python dependencies of Ibel.

```sh
   $ sudo apt install python3-pip python3-dev libxml2-dev libxslt1-dev libldap2-dev libsasl2-dev libssl-dev libpq-dev libjpeg-dev
   ```
##### Create python virtual environments
It can be preferable to not mix python modules packages between different instances of Odoo or with your system. You can use virtualenv to create isolated Python environments.

```sh
   $ python3 -m venv ibel-env 
   ```
This will create the ibel-env directory if it doesn’t exist, and also create directories inside it containing a copy of the Python interpreter, the standard library, and various supporting files. 

Once you’ve created a virtual environment, you may activate it.
```sh
   $ source ibel-env/bin/activate 
   ```
Activating the virtual environment will change your shell’s prompt to show what virtual environment you’re using, and modify the environment so that running python will get you that particular version and installation of Python. 
```sh
   (ibel-env) $ 
   ```
##### Install Ibel requirements in virtual env
```sh
   (ibel-env) $ pip3 install -r ibel/requirements.txt
   ```
### Run the server
#### Running odoo-bin
Once all dependencies are set up, Ibel can be launched by running odoo-bin, the command-line interface of the server.

1. To generate a configuration file for your Odoo instance, run the following
command:
```sh
   (ibel-env) $ python3 ibel/odoo-bin --config ibel.conf --addons-path ibel/addons,ibel_addons --save --stop-after-init
   ```
You can add additional options, and their values will be saved in the generated file. All the unset options will be saved with their default value set. To get a list of possible options, use the following command:
```sh
   (ibel-env) $ python3 ibel/odoo-bin --help
   ```
This will provide you with some help about what the various options perform.

_Also refer to the [Documentation](https://www.odoo.com/documentation/14.0/developer/misc/other/cmdline.html#reference-cmdline-server)_

2. Then, to start the server with the saved options, run the following command:
```sh
   (ibel-env) $ python3 ibel/odoo-bin --config ibel.conf 
   ```
#### Log in to Odoo

Open [!http://localhost:8069/] on your browser. We recommend you use: Firefox, Chrome (Chromium the open source equivalent) or any other browser with development tools.

To log in as the administrator user, you can use the following credentials:

email = admin

password = admin
<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://www.odoo.com/documentation/14.0/developer/misc/other/cmdline.html#reference-cmdline-server)_



<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/othneildrew/Best-README-Template/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Your Name - [@your_twitter](https://twitter.com/your_username) - email@example.com

Project Link: [https://github.com/your_username/repo_name](https://github.com/your_username/repo_name)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Img Shields](https://shields.io)
* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Pages](https://pages.github.com)
* [Animate.css](https://daneden.github.io/animate.css)
* [Loaders.css](https://connoratherton.com/loaders)
* [Slick Carousel](https://kenwheeler.github.io/slick)
* [Smooth Scroll](https://github.com/cferdinandi/smooth-scroll)
* [Sticky Kit](http://leafo.net/sticky-kit)
* [JVectorMap](http://jvectormap.com)
* [Font Awesome](https://fontawesome.com)





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/abdawone/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/abdawone/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
