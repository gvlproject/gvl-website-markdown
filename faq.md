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

## How do I upload large files to my server?

Files can be uploaded to your server using FTP or GenomeSpace.

### FTP

Files larger than 2GB can be uploaded to Galaxy only by FTP.

**From the Command Line** (e.g. in MS Windows, call up the Command Prompt. In Linux, ssh login).

*   Change to the directory containing your file;
*   Type `ftp <ipaddress>` e.g. `ftp galaxy-qld.genome.edu.au`
*   Enter your Galaxy user id and password; then
*   Type `put <filename>` e.g. `put CM10005.FASTA.`

The file is now in the Galaxy FTP directory under your user ID (no one else can see it)

*   Go to your Galaxy server e.g. [http://galaxy-qld.genome.edu.au/](http://galaxy-qld.genome.edu.au/)
*   Select *Get Data / Upload File*. Your file will be displayed in the list of "Files uploaded by ftp"; then
*   Select it, Execute.

**Using Internet Explorer**

*   Enter `ftp://<ipaddress>` into the browser e.g. `ftp://galaxy-qld.genome.edu.au`
*   Enter your Galaxy user ID and password to finish logging in to the FTP site
*   Select "Page" Menu drop-down within Internet Explorer;
*   Select "Open FTP site in File Explorer"; then
*   Login again

From another file explorer window, drag and drop your file into the ftp window. The file is now in the Galaxy FTP directory under your user ID (no one else can see it).

*   Go to your Galaxy server e.g. `http://galaxy-qld.genome.edu.au/`
*   Select *Get Data / Upload File*. Your file will be displayed in the list of "Files uploaded by ftp"; then
*   Select it, Execute

Galaxy will unpack compressed (.gz) files. Please do not upload many compressed files simultaneously by FTP because you may run out of the disk space in your allocation. Some organisations have very strict firewall settings that prevent FTP data transfer. To test FTP, upload a small compressed (.gz) file.


* * *

## How do I fix a broken/stuck file upload?

My files were stuck during upload (colored in blue). How do I delete these files?

Do the following:

*   From the History menu click on *Show Structure*
*   Delete files in the middle (working) window.


* * *


## Is there a way to import data from a password protected ftp site directly into Galaxy?

Yes, just put your username and password in the URL link:

`ftp://username:password@hostname/path_to_your_data/file.name`

Paste the link into *Get Data -> URL/Text window*

* * *


## How do I transfer Galaxy history between instances?

There is no nice clean way to do this in Galaxy because Galaxy zips it up and downloads it for you, but you cannot upload the archived history file to a new instance, you can only import a URL history archive. (Browsers can't upload files larger than 2GB and real histories are likely to be large).

Import from URL works, but it is fussy and it does not work immediately. It starts a background job that downloads and unzips the history archive. If there is a problem, you never find out. You only know it worked if you check back some time later and there is a new history in your list.

First, download the archive, then put it somewhere that it can be accessed by URL:

*   Select *Export to file* from the History menu (little cog icon at top of history)
*   A URL appears which doesn't yet work, because the history has to be archived first and this happens invisibly in the background (unless you've exported the history previously). If the history is already archived, then when you select 'Export to file' you don't get this link, you just get the downloaded file
*   After some indeterminate period related to the size of the history, the history archive will be available for download at this URL, or through the *Export to file*
*   Download the file, and copy or move it to a web-accessible store, for example:
    1.  A web server on the GVL (e.g. your html_public directory);
    2.  The Object Store and make it publicly available; or
    3.  Aarnet's CloudStor can also make a file available as a URL.


* * *

## How do I download files from my Galaxy server to a specific location?

You can save your datasets from Galaxy to any location using `curl` or `wget` commands. For curl do the following:

*   Open a UNIX terminal and navigate to the place you want to store your files
*   In Galaxy history > right mouse click on *Save* icon > *Copy Link Address*; then
*   In your UNIX terminal type: `curl link_to_your_file > name_of_destination_file`

Alternatively, you can download via your browser:

*   In Galaxy history > right mouse click on *Save* icon > *Copy Link Address*
*   Paste the URL into your web browser to download the file.

* * *

## How do I do De Novo transcript assembly with Trinity and read normalisation?

Trinity read normalisation improves the run time for transcript assembly, and it is recommended for large datasets.

*   Example of recommended transcript assembly with Trinity on [Galaxy-qld](http://galaxy-qld.genome.edu.au/): *Shared Data* > *Published Histories* > *De novo transcript assembly using Trinity package*.
*   The workflow for this procedure on [Galaxy-qld](http://galaxy-qld.genome.edu.au/): *Shared Data* > *Published Workflows* > *De novo transcript assembly using Trinity package*.
*   The workflow can be used with FASTQ data in *Shared Data* > *Published Histories* > *Data for Trinity*.

Note that the read normalisation does not like space characters in read names. Unfortunately, many public datasets do contains space characters in read names. To transform read names:

*   convert FASTQ to Tabular and split names in n+1 columns, where n = number of space character in read names
*   convert Tabular to FASTQ using only one column for read names.
*   Example of executing this transformation on [Galaxy-qld](http://galaxy-qld.genome.edu.au/): *Shared Data* > *Published Histories* > *Preparation of FASTQ reads for Trinity read normalisation*.
*   Workflow for this transformation on [Galaxy-qld](http://galaxy-qld.genome.edu.au/): *Shared Data* > *Published Histories* > *Preparation of FASTQ reads for Trinity read normalisation*.

* * *

## Is there a way to get the queue time and run time for a job in Galaxy?

Yes for run time, no for queue time. Do the following:

*   Click on the filename of one of the output files for the job of interest.
*   Click on the *information* button "i". The runtime (walltime) is listed near the bottom of the screen.

* * *

## Disk quotas for Australian researchers on Galaxy-qld

After registration on Galaxy-qld all new users are assigned 100 GB disk quota. Later we allocate more disk space for Australian and UQ users. This will usually happen within one working day after the registration. The disk quota can be seen in Galaxy under *User* > *Preferences*

* * *

### I used all quota on Galaxy-qld. Can you give me more disk space?

In some circumstances we can increase the user quota. However, Galaxy-qld is a public resource, and we can maintain the service only with efficient use of our resources, especially the storage. Please treat Galaxy-qld as a workbench. Researchers usually store their samples in fridges or freezers, solutions on shelfs etc. Work benches are used for experiments, and usually will be cleaned after the work. Use the same approach on Galaxy-qld.
  1. Plan your analysis first.
  2. Upload one or two samples and develop a workflow.
  3. Delete unneeded files. Delete temporary files such as SAM.
  4. Do not upload many (compressed) FASTQ files simultaneously. Galaxy will unzip uploaded files, and these files may fill up your allocation.
  5. By default, most alignments keep all reads including unaligned. There is no need to store FASTQ if you have an alignment.
  6. Download the results and delete files on Galaxy-qld

* * *

### I deleted many files but my usage is still shown as 100%. What is going on?

Galaxy uses a ‘soft delete’ option and the deleted files have to be purged: *History Menu* > *Purge Deleted Datasets*. The files have to be purged from each history separately. Use the *Delete Permanently* option for histories. To find deleted but not purged histories: *History Menu* > *Saved Histories* > *Advanced Search* > *Deleted*

* * *

## Is there a way to resume a partially complete workflow in Galaxy?

Sort of. You need to create a new workflow with non-completed steps and run it over the completed dataset.

  1.  Go to the workflows page via the *Workflows* menu
  2.  Click on the down arrow on the workflow you wish to resume to access its menu. Select *Copy*
  3.  Open the copy of the workflow by selecting *Edit* from its menu.
  4.  Remove the completed steps (click to select and then delete)
  5.  *Save* the modified workflow
  6.  *Run* the modified workflow with the datasets produced by the partially complete workflow.
  7.  You'll have to delete the non-completed 'grey' datasets from the first attempt.

* * *

## What GVL Version am I using?

A GVL analysis server consists of three components:

*   a *Machine Image*;
*   a *Galaxy File System*; and
*   Genome Index reference data

GVL periodically releases new versions of the *Machine Image* and the *Galaxy File System*, as new features are added to the GVL.

*   The *Machine Image version* is chosen as an Advanced Option on the launch page ([launch.genome.edu.au](https://launch.genome.edu.au)). You can see what version you have on the NeCTAR dashboard display of your Instances.
*   You don't have control of the Galaxy File System version. You can see what version you have from the banner on your Galaxy (e.g. "Galaxy / GVL 3.05")
*   Genome Index reference data is a shared file system amongst all GVLs: versioning does not apply.

For more information refer to [GVL versions](/get/#Version_change_log)

* * *

## When accessing my NeCTAR instance via SSH, why am I getting a permission denied (publickey) error?

A permission denied (publickey) error typically means the private key is not a correct match for the public key.

When creating a keypair on NeCTAR, only the most recent downloaded version of the private key is correct. Please ensure you only use this version of the private key.
