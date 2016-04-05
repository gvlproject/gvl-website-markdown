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

## Launch a GVL instance on the cloud

A GVL instance is a server, usually running as a virtual machine in a cloud environment. You can find an overview of supported clouds and how to launch an instance on the [Launch page](launch).

In particular, a step-by-step guide to launching an instance on the Australian Research Cloud (NeCTAR) can be found [here](https://vlsci.github.io/lscc_docs/tutorials/gvl_launch/gvl_launch/).

* * *

## Use and administer your instance

Your GVL instance runs your own Galaxy server as well as several other services, including CloudMan, RStudio Server and IPython Notebook, and an underlying Ubuntu linux environment. These services are described on the [Workbench Services page](/workbench-services).

On GVL versions older than 4.0, some services will not be available until installed. Instructions on doing this can be found on [v3.05 of the README](https://github.com/gvlproject/gvl_commandline_utilities/blob/release_GVL_3.05/README.md) in our GitHub repository.

When you first create your instance, you will be given an IP address which you can access in a web browser. At the home page of your instance you should find your [GVL Dashboard](/workbench-services), with a list of Workbench Services and login instructions.

Documentation on some common GVL administration tasks, including CloudMan, Galaxy and Research Cloud tasks, can be found in this [GVL administration](https://docs.google.com/document/u/1/d/1x88f1Eyg_hJLUw-pI0zCUMv6EJI32pLnUOOeVkGdA3Q/pub) guide.

For general documentation on using Galaxy itself, the best source is the [Galaxy Project website](https://galaxyproject.org/). This site includes documentation on [Galaxy Administration](https://wiki.galaxyproject.org/Admin/Interface).

Instructions for command-line utilities administration can be found in the GVL commandline utilities [GitHub repository](https://github.com/gvlproject/gvl_commandline_utilities). These include instructions for:

*   Adding a new linux or RStudio Server user
*   Updating the environment modules to reflect changes in tools installed from the Galaxy Toolshed
*   Using galaxy-fuse to directly mount Galaxy Datasets for command-line access

* * *

## Build a custom GVL

"Building" a GVL refers to creating a new, custom cloud image, which can be used to launch new instances. Most users will not need to do this.

Reasons to build a new GVL image include:

*   You would like to port the GVL to a cloud environment where it is not already available.
*   You would like to make custom modifications which you can't make after launch, or create a modified image, tailored to your research domain, from which your own research community to can launch instances.

The ansible playbook used to build the GVL image and GVL filesystem, and instructions for using it, can be found in our [GVL image bitbucket repository](https://bitbucket.org/gvl/gvl-image-playbook/). These scripts are heavily reliant on the Galaxy CloudMan playbook, which you will find referenced in the README.
