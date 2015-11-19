# Rancher Cassandra

This container is an extension of the official Docker [Cassandra](https://hub.docker.com/_/cassandra/) image which adds support for running in Rancher.
Specifically, this container allows setting the `CASSANDRA_LISTEN_ADDRESS` and `CASSANDRA_BROADCAST_ADDRESS` environment variables to a value of `rancher`.
Setting this value cause the container to discover the container's IP address using the Rancher [metadata service](http://docs.rancher.com/rancher/metadata-service/).
Specifically, the environment variable will be set to the value of the `private_ip`property in the metadata service.
