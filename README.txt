The LinuxCNC WebSocket Server is a lightweight web server customized to provide information and control of a running LinuxCNC machine control system.

The server is based on the Tornado open source web server framework.  Tornado is written in Python, and the LinuxCNC Web Socket Server is also written using the Python programming language.

The interface to the LinuxCNC system uses the Python API for LinuxCNC.  Documentation for this API is at http://www.linuxcnc.org/docs/devel/html/config/ini_config.html#_emc_section_a_id_sub_emc_section_a

The server also uses the halcmd program, a part of LinuxCNC which can access and configure the HAL layer of LinuxCNC.

To communicate with the LinuxCNC WebSocket Server, a client application opens a WebSocket with the server, and sends text commands.  All commands result in an immediate reply, such as the result of executing the command or some status information. Some commands will also send further replies, such as notifying the client when a watched status variable has changed.

Using this WebSocket based interface, a remote program can query status, send commands, and otherwise control the running LinuxCNC machine controller.

All commands and replies are formatted using JSON (JavaScript Object Notation).  This is a text based, human readable format which is widely supported in many programming platforms.
