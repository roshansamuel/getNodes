# getNodes

``getNodes`` is a Python-based command-line tool to get list of idle nodes on Shaheen supercomputer in a user-friendly manner.

## Installing getNodes

To install ``getNodes``, you need to only clone the git repository into your local machine

`git clone https://github.com/roshansamuel/getNodes.git`

## Using getNodes

The executable Python script can be moved to a folder which is included in the PATH environment variable (like ``/usr/local/bin/``), so that the tool is available at the command-line.

Now update the ``.bashrc`` file with the following alias:

`alias sin='sinfo -p workq -t idle --format=%n > nodeInfo.txt; getNodes; rm nodeInfo.txt'`

The above alias performs 3 steps - create the list of available nodes in the file ``nodeInfo.txt``, parse this file with Python and print the output, and finally delete the file ``nodeInfo.txt``.

After sourcing the ``.bashrc``, typing the command ``sin`` on the command-line should produce the necessary output.
