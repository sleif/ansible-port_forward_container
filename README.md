# sleif.port_forward_container

This role runs a socat-based port forwarding in docker.

## Requirements

None

## Role Variables

- virtual_host (entry point hostname)
- REMOTE_HOST
- REMOTE_PORT


## Example Playbook

    - hosts: "server"
      user: root
      vars:
        docker_network_name: 'custom_docker_network'
      roles:
        - { role: sleif.nginx_docker, tags: "nginx_docker",
                                          virtual_host: "external-host.example.com",
                                          REMOTE_HOST: "target-host.internal.excample.com",
                                          REMOTE_PORT: "8080" }

## License

MIT

## Author Information

Created in 2021 by Sebastian Berthold
