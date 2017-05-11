<style type="text/css">
  #gvl-launch-button,
  #gvl-launch-button:active,
  #gvl-launch-button:visited {
    font-size: 30px;
    height: 80px;
    width: 200px;
    padding: 25px;
    border-radius: 5px;
    background: #31A3DD;
    text-align: center;
    color: white;
    display: block;
    margin: auto;
  }
  #gvl-launch-button:hover {
    background: #2a6496 !important;
    color: white;
  }
  td {
    text-align: left !important;
  }
  td ul {
    padding-left: 20px;
  }
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


Use the launch page to launch your own private server on the cloud, with the GVL pre-installed.

You can launch a new server instance on a public cloud, such as NeCTAR/OpenStack or Amazon/EC2 (the default for most users). You can also build and deploy the GVL on a private cloud.

-----

## Launch a GVL

#### 1. Launch your server on a public cloud (most users)

Use the [launch page](http://launch.genome.edu.au) to launch your own private server on the cloud, with the GVL pre-installed. You can launch a new server instance on an existing cloud, such as NeCTAR/OpenStack or Amazon/EC2 (the default for most users).

Instructions on how to launch an instance can be found [here](http://vlsci.github.io/lscc_docs/tutorials/gvl_launch/gvl_launch/).

<a id="gvl-launch-button" href="http://launch.genome.edu.au">Launch</a>


#### 2. Launch your server on a private cloud (specialised usage)

To launch your server on a private cloud, you must build the GVL manually on your cloud. At present, OpenStack and EC2 compatible clouds are supported. If you are using OpenStack, you must have the EC2 compatibility layer enabled.

You can find source code and instructions to build a GVL image in our [repository](https://bitbucket.org/gvl/gvl-image-playbook).

-----

## What is a private GVL Server?

A private GVL server is a virtual machine running on the cloud and contains a pre-installed suite of tools for performing bioinformatics analyses. It differs from public GVL servers by providing full administrative access to the server, as well as the full suite of GVL services, whereas public GVL servers provide restricted access for security reasons. For example, public GVL servers do not provide access to the Ubuntu desktop, the Linux command line, JupyterHub, RStudio etc. at present.

Private GVL servers may be launched on a public cloud of your choice (at present, Amazon and OpenStack based clouds). These can be as simple as servers which provide individual access, to more complicated institutional access servers over which you will have full control. You will require access credentials to a public/community cloud to launch a private GVL server. Accessing the GVL server is completely free on the Australian NeCTAR Research Cloud, provided that you have a suitable account with NeCTAR. On Amazon, while the GVL software itself is free, you may have to pay Amazon usage charges.

-----

## Flavours

##### What is a flavour?

Flavours are versions of the GVL with slightly customised toolsets. These toolsets are optimised for different usage patterns. For example, the Tutorial flavour is intended for running the GVL tutorials, and the Microbial flavour is optimised for Microbial workflows.



| Flavour   | Description                                                                                                                                                                                                                  | Preinstalled Tools                                                                                       | Optionally Installable                                                                                                                       |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| Base      | A basic GVL flavour with all options available for configuration. Use this option if you want to configure custom storage options, and individualy select which components to install.                                       | Galaxy - with the standard GVL toolset, Cloudman, VNC, Command line access                               | RStudio, JupyterHub, PacBio's SMRT Analysis, Public Health Canada's IRIDA, WebApollo, Pathway Tools, LOVD, Cpipe, Pancancer BWA-Mem Workflow |
| Tutorial  | The tutorial flavour of the GVL contains all the tools required for the GVL tutorials preinstalled. Choose this option when your main purpose is educational and you want to follow the GVL tutorials with the least hassle. | Galaxy - with the standard GVL toolset, Cloudman, VNC, Command line access, RStudio, JupyterHub          | PacBio's SMRT Analysis, Public Health Canada's IRIDA, WebApollo, Pathway Tools, LOVD, Cpipe, Pancancer BWA-Mem Workflow                      |
| Microbial | GVL Microbial is similar to GVL base, but Galaxy and command line tools have been optimised for microbial workflows.                                                                                                         | Galaxy - with microbial tools (e.g. SPAdes, Prokka, Artemis, Snippy), Cloudman, VNC, Command line access | Same as base                                                                                                                                 |

-----

## Version change log

<table>
<thead>
<tr>
<th>Version</th>
<th>New Features</th>
<th>Deprecated features</th>
</tr>
</thead>

<tbody>
<tr>
<td>4.1.0</td>
<td>
<ul>
<li>Galaxy updated to 16.04</li>
<li>Updated list of tools and tool revisions</li>
<li>Easier import/export of files from/to GenomeSpace</li>
<li>SMRT portal uses distributed jobs and has better space management</li>
<li>New installable packages for Web Apollo, IRIDA</li>
<li>User accounts are now synchronised across the whole cluster.</li>
<li>X-Forwarding support</li>
<li>Increased space in root partition and reduced virtual image size</li>
</ul>
</td>
<td></td>
</tr>

<tr>
<!--<td>4.0.0 Beta1</td>-->
<td>4.0.0</td>
<td>
<ul>
<li>GVL now supported on Amazon EC2</li>
<li>Image updated to Ubuntu 14.04 LTS</li>
<li>A new Ansible based build process to replace the old Fabric based one</li>
<li>Job management software has been switched from SGE to SLURM, as SGE does not support Ubuntu 14.04</li>
<li>New installable packages for cpipe, lovd and SMRT-Analysis</li>
<li>Support for GVL flavours</li>
<li>Overhauled list of Galaxy tools for each flavour</li>
</ul>
</td>
<td>
<ul>
<li>SGE is no longer available and has been replaced with SLURM.</li>
</ul>
</td>
</tr>

<tr>
<td>3.04</td>
<td>
<ul>
<li>Introduction of the GVL Dashboard as a portal for other GVL services</li>
<li>Security and package updates to Ubuntu 12.04 LTS</li>
<li>Stability and bug fixes</li>
</ul>
</td>
<td></td>
</tr>
</tbody>
</table>
