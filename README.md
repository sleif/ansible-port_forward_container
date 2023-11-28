# sleif.port_forward_container

This role runs a socat-based port forwarding in docker.

## Requirements

None

## Role Variables

- virtual_host (entry point hostname)
- remote_host
- remote_port


## Example Playbook

    - hosts: "server"
      user: root
      vars:
        docker_network_name: 'custom_docker_network'
      roles:
        - { role: sleif.nginx_docker, tags: "nginx_docker",
                                          virtual_host: "external-host.example.com",
                                          remote_host: "target-host.internal.excample.com",
                                          remote_port: "8080" }

## License

MIT

## Author Information

Created in 2021 by Sebastian Berthold
