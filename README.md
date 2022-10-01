# getNodes

``getNodes`` is a Python-based command-line tool to get list of idle nodes on Shaheen supercomputer in a user-friendly manner.

## Installing getNodes

To install ``getNodes``, you need to only clone the git repository into your local machine

`git clone https://github.com/roshansamuel/getNodes.git`

## Using getNodes

The executable Python script can be moved to a folder which is included in the PATH environment variable (like ``/usr/local/bin/`` or ``$HOME/local/bin/``), so that the tool is available at the command-line.

The command-line arguments used by getNodes are:

```
usage: getNodes [-h] [-a]

options:
  -h, --help  show this help message and exit
  -a          print all available nodes in comma separated form
```

## Using the node-list in sbatch

The nodes listed by the app can be located in the Shaheen cluster using the data provided [here](http://home.iitk.ac.in/~anandogc/nid_marker.html).

After identifying the required nodes, specify them in the ``sbatch`` job script using the following directive:

`#SBATCH --nodelist=nid000[00-51],nid00[100-243]`

The job will run only if the number of nodes specified in the node-list matches the number of nodes requested with the ``--nodes`` directive.
