# LionVelocity
is a velocity plugin that provides basic functions allowing vanilla-style player management for the whole network. <br>
> <strong>This description is outdated. Look [here](https://github.com/LionCraft08/LionVelocity/blob/master/README.md) for an updated version</strong>

# Features 
<details><summary>
lvc (Player Management)
</summary>
Basic commands are provided via arguments of the /lvc command.
This includes:
- Bans (with duration)
- Whitelist
- Operator permission
</details>
<details><summary>Backend sync</summary>
Synchronisation with backend servers.<br>
This includes ways paper servers can request the data of connected backend servers,
Player data (Operator status of lvc, statistics and data that can be modified)
and ways backend servers can dynamically handle communication to the proxy and other backend servers. (see connection setup for more)
</details>
<details><summary>
shutdown</summary>
relying on a connection to backend servers, the velocity can shut down backend servers (with lionAPI installed).
This allows you to shutdown the whole network with the /shutdown command 
(note that servers will only shut down if a connection is active, see connection setup)
</details>

# Connection Setup 
For many features, a connection to the backend server is required.<br>
To connect a backend server to the proxy, follow these guidelines: <br>
0. If you haven't already, create the connection in velocity's config (see velocity docs)
1. Find the configuration: 
- Paper: plugins/lionAPI/config.yml
- Velocity: plugins/lionvelocity/servericons (optional)
2. Create the configuration: Find the configuration server-connection.velocity
<br> Fill in the type:
- If you select player, the servers communicate using a player's connection. This requires no additional setup, however, the servers cannot communicate if no player is connected to the targeted backend. This is useful for when you cannot use additional ports, but means, for example, a server will not shutdown with the /shutdown command when no player is connected.
- If you select 

