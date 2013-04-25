RemotePowerShell
================

Use powershell remotely from linux (or any other) host

Windows host
-------------------------

On Windows Server host run::

    > python.exe serve.py

Don't forget to open 42000 port for inbound connections.

Remote host
-------------------------

You can call powershell commands with::

    $ python rps.py -s "echo 'Hello world'" -h 25.84.118.43

Python module
--------------------

You can use powershell in python modules like::

     >>> import serve
     >>> rps = serve.RemotePowerShell("example.com")
     >>> print rps("echo HELLO")
     HELLO
