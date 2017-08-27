# mod_stream_mgmt_s2s

## Introduction

This module is an implementation of server-to-server Stream Management ([XEP-0198](https://xmpp.org/extensions/xep-0198.html)). Stanza acknowledgement and stream resumption are implemented for stream management.

## Options

For server-to-server stream management following options are available: `resume_timeout`, `max_resume_timeout`, `queue_type`, `max_ack_timeout` and `connection_timeout`. For description of `resume_timeout`, `max_resume_timeout`, `queue_type` and `max_ack_timeout`  see `mod_stream_mgmt`.

`connection_timeout: Seconds`: If an outgoing connection is lost and queue with unacknowledged stanzas isn't empty, server will try to reconnect to remote server and resume session. If reconnection to remote server fails, server will retry for N seconds. This option configures the number of seconds during which the server will retry to establish connection with remote server to resume previous session. The default value is `300`.