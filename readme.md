## Kibana
### Description
This role is designed to install kibana on VMs running docker to be used in conjunction with docker-elasticsearch role.

### Testing
This role was tested on the below versions
- Ubuntu 20.04
- Docker Version 20.10.5
- Elasticsearch 7.12
- Kibana 7.12

### Variables
Below are the variables used by this role;  

- **docker_network_name**  
The name of the docker network that will be associated with your kibana containers.

- **kibana_certs_dir**
Local persistent directory on VM which will store certificates used for SSL.

- **kibana_conf_dir**
Local persistent directory for Kibana config file.

- **kibana_hostname**
The name of your container.

- **kibana_image**
The image and version of Kibana you want to deploy.

- **kibana_username**
The Kibana username to connect with.

- **kibana_password**
The kibana password to connect with.

- **docker_log_max_size**
The maximum json file size before the log is rolled.

- **docker_log_max_file**
The maximum number of log files that can be present.

- **kibana_server_port**
The port to serve Kibana on.

- **kibana_server_host**
The IP address to which the Kibana server will bind.

- **groups['elastic_cluster_hosts']**
This is a required host group consisting of the elasticsearch cluster to connect Kibana to.

- **kibana_index_name**
The index name to store kibana specific data in such as saved searches and dashboards.

- **kibana_username**
The kibana username to connect to elasticsearch with.

- **kibana_password**
The kibana password to connect to elasticsearch with.

### Tags
- kibana
This tag will target all tasks related to this role.

### Additional Resources
https://docs.docker.com/config/containers/logging/local/
https://docs.ansible.com/ansible/latest/collections/community/docker/docker_network_module.html
https://docs.ansible.com/ansible/latest/collections/ansible/builtin/file_module.html
https://docs.ansible.com/ansible/latest/collections/ansible/builtin/template_module.html
https://docs.ansible.com/ansible/latest/collections/ansible/builtin/copy_module.html
https://docs.ansible.com/ansible/latest/collections/community/docker/docker_container_module.html