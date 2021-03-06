.. _install-minter:

Install Minter
==============

There are several ways you can install Minter Blockchain Testnet node on your machine:

Using binary
------------

Download Minter
^^^^^^^^^^^^^^^

Get `latest binary build <https://github.com/MinterTeam/minter-go-node/releases>`__ suitable for your architecture and
unpack it to desired folder.

Run Minter
^^^^^^^^^^

.. code-block:: bash
    :lineno-start: 13

    ./minter

Then open http://localhost:3000/ in local browser to see node's GUI.

Using Docker
------------

You'll need `docker <https://docker.com/>`__ and `docker compose <https://docs.docker.com/compose/>`__ installed.

Clone Minter source code to your machine
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: bash
    :lineno-start: 1

    git clone https://github.com/MinterTeam/minter-go-node.git
    cd minter-go-node

Start Minter
^^^^^^^^^^^^

.. code-block:: bash
    :lineno-start: 10

    docker-compose up

Then open http://localhost:3000/ in local browser to see node's GUI.

From Source
-----------

You'll need ``go`` `installed <https://golang.org/doc/install>`__ and the required
`environment variables set <https://github.com/tendermint/tendermint/wiki/Setting-GOPATH>`__

Clone Minter source code to your machine
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: bash
    :lineno-start: 1

    mkdir $GOPATH/src/github.com/MinterTeam
    cd $GOPATH/src/github.com/MinterTeam
    git clone https://github.com/MinterTeam/minter-go-node.git
    cd minter-go-node

Get Tools & Dependencies
^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: bash
    :lineno-start: 5

    make get_tools
    make get_vendor_deps

Compile
^^^^^^^

.. code-block:: bash
    :lineno-start: 7

    make install

to put the binary in ``$GOPATH/bin`` or use:

.. code-block:: bash
    :lineno-start: 8

    make build

to put the binary in ``./build``.

The latest ``minter version`` is now installed.

Run Minter
^^^^^^^^^^

.. code-block:: bash
    :lineno-start: 13

    minter

Then open http://localhost:3000/ in local browser to see node's GUI.

Troubleshooting
---------------

Too many open files (24)
^^^^^^^^^^^^^^^^^^^^^^^^

The default number of files Linux can open (per-process) is 1024. Tendermint is known to open more than 1024 files.
This causes the process to crash. A quick fix is to run ulimit -n 4096 (increase the number of open files allowed) and
then restart the process with gaiad start. If you are using systemd or another process manager to launch gaiad this
may require some configuration at that level.

`<https://easyengine.io/tutorials/linux/increase-open-files-limit/>`__
