# Ansible ESXi Deployment

This project provides an Ansible playbook to deploy a virtual machine on an ESXi version 9 host. It utilizes roles to organize tasks and variables for a clean and maintainable structure.

## Project Structure

```
ansible-esxi-deploy
├── play.yaml                # Main Ansible playbook
├── roles
│   └── esxi_vm
│       ├── tasks
│       │   └── main.yaml    # Tasks to deploy the VM
│       └── vars
│           └── main.yaml     # Variables for the role
├── inventory                # ESXi hosts and connection details
└── README.md                # Project documentation
```

## Prerequisites

- Ansible installed on your control machine.
- Access to an ESXi version 9 host.
- Necessary permissions to create and manage virtual machines on the ESXi host.

## How to Run the Playbook

1. Update the `inventory` file with your ESXi host details.
2. Modify the `roles/esxi_vm/vars/main.yaml` file to set your desired VM configuration.
3. Execute the playbook with the following command:

   ```
   ansible-playbook -i inventory play.yaml
   ```

## Role Details

- **esxi_vm**: This role contains all tasks and variables necessary for deploying a virtual machine on the ESXi host.

## License

This project is licensed under the MIT License.