<style>
  code {
    color: #777777;
  }
  body {
    line-height: 2;
    font-family: "Helvetica";
  }
  hr {
    border-top: 3px solid #C0C0C0;
  }
</style>

Each GVL instance comes with pre-installed bioinformatics tools and reference data, which can be used through several different interfaces. 

The various platforms and analysis environments installed on each GVL instance are described below.

Each of these services is accessible from your instance's GVL Dashboard.

On GVL version 4.0 and later, these components should all already be installed. On earlier versions such as 3.05, Galaxy and CloudMan will already be installed, but you will need to activate some other utilities by following the instructions in [v3.05 of the README](https://github.com/gvlproject/gvl_commandline_utilities/blob/release_GVL_3.05/README.md) in our GitHub repository

* * *

## GVL Dashboard

The GVL Dashboard is the home page of your GVL instance. You can find it by directing your web browser to the IP address or URL or your launched instance.

It shows the status of each service and gives a link to each running service, together with login details for that service.

* * *

## CloudMan

CloudMan gives you administrative control over your virtual machine. It also allows you to add worker nodes to your instance to build a virtual cluster-in-the-cloud. You can find your instance's CloudMan interface at `http://<your_instance_IP>/cloud`.

You can find out more about CloudMan [here](http://cloudman.irb.hr/).

* * *

## Galaxy

Galaxy is a web-based platform for biomedical research. Each launched GVL instance comes with its own Galaxy server, which you can find at `http://<your_instance_IP>/galaxy`.

Or, if you are an Australian researcher, you can [use one of our Galaxy servers](/use) instead. You can find out more about Galaxy at the [Galaxy Project site](https://galaxyproject.org/).

* * *

## Ubuntu Linux 14.04

Your GVL instance runs on linux, which you have full administrative access to. Many Galaxy-installed bioinformatics tools are also accessible from command line.

For ordinary use, ssh in with `ssh researcher@<your_instance_IP>` or for administrative purposes, ssh in with `ssh ubuntu@<your_instance_IP>`.

* * *

## VNC Desktop

VNC desktop is a browser-based remote desktop for linux. You can log in using your linux credentials, as user *researcher* for research purposes, or user *ubuntu* for administrative purposes.

You can find your VNC interface at `http://<your_instance_IP>/vnc`.

* * *

## RStudio Server

RStudio Server gives browser-based access to RStudio, the popular programming and analysis environment for the R programming language. You can find your RStudio interface at `http://<your_instance_IP>/rstudio`.

You can find out more about RStudio [here](http://www.rstudio.com/), and the R programming language [here](http://r-project.org).

GVL instances come with many R packages from the [Bioconductor Project](http://www.bioconductor.org/) pre-installed.

* * *

## IPython Notebook

IPython Notebook is an interactive programming and analysis environment for the Python programming language, capable of producing interactive analysis documents.

Currently IPython Notebook on your GVL instance is a single-user process, which must be launched by the *researcher* linux user via ssh or VNC. Instructions can be found [here](http://gvlproject.github.io/gvl_commandline_utilities/).
