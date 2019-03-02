socket input
===================

Input event message should end with new line (`\n`).

## Synopsis

```
{
	"input": [
		{
			"type": "socket",

			// Socket type. Must be one of ["tcp", "udp", "unix", "unixpacket"].
			"socket": "tcp",

			// For TCP or UDP, address must have the form `host:port`.
			// For Unix networks, the address must be a file system path.
			"address": "localhost:9999",

			// (optional) SO_REUSEPORT applied or not, default: false
			"reuseport": false,

			// (optional) The packet size to read from the network, default: 4096
			"buffer_size": 4096,

			// (optional) The socket receive buffer size in bytes.
			"receive_buffer_bytes": 0
		}
	]
}
```

> Note: at the moment, UNIXGRAM socket are not supported.
