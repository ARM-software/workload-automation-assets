Assets for Workload Automation
++++++++++++++++++++++++++++++

This repo provides external assets that are required to run some
of the workloads in `Workload Automation <https://github.com/ARM-software/workload-automation>`_.

Some of them are sizable files comparable to WA itself, so this avoids bloating
the main repository (and download size) for users that do not need the functionality.

To use this assets repository you will need to add the following line to your config.py file::

    remote_assets_url="https://raw.githubusercontent.com/ARM-software/workload-automation-assets/master/dependencies/index.json"

Contributing
============
When contributing assets to this repository you should update the `index.json`
with each commit that adds assets using the `index-assets` script. (run
`index-assets -h` for more details on how to use it)

To make this simpler we have provided a git hook that will do this automatically
when you make a commit that adds assets. To use this git hook, simply run::

    cp hooks/pre-commit .git/hooks/pre-commit
    chmod a+x .git/hooks/pre-commit

License
=======
Most of the assets within this repository are copyright ARM Ltd and are licensed
under the `Apache v2.0 License <http://www.apache.org/licenses/LICENSE-2.0>`_.
this repository may include third party assets, please see the coresponding
COPYING/LICENSE files for their licensing details.
