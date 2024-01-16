# Ovirt Ansible VM Deployment

This Ansible playbook automates the deployment of Ovirt virtual machines. It allows you to dynamically configure various parameters such as cluster number, VM state, memory size, CPU cores, and more.

## Prerequisites

Before running the playbook, ensure the following prerequisites are met:

- Ansible is installed on the control machine.
- Ovirt engine URL, username, password, and other configurations are correctly set in `vars/ovirt_config.yml` and `vars/ovirt_password.yml`.

## Usage

1. Clone this repository:

    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. Install required Ansible collections:

    ```bash
    ansible-galaxy collection install ovirt.ovirt
    ```

3. Run the Ansible playbook:

    ```bash
    ansible-playbook create_vm_instance.yml
    ```

4. Follow the prompts to enter the desired configuration parameters.

## Configuration Parameters

- **Cluster Number:** Enter the cluster number (e.g., 14, 17, 18, 19).
- **Sequence Start:** Enter the start value for the VM name sequence.
- **Sequence End:** Enter the end value for the VM name sequence.
- **VM State:** Choose the VM state [running(create), present, absent(delete)].
- **Format Name:** Enter the format name for the VM (e.g., ansible-vm-test).
- **Memory Size:** Enter the memory size in GiB for each VM (e.g., 4).
- **CPU Cores:** Enter the number of CPU cores for each VM.

## Example

Here is an example of how the playbook can be configured:

```bash
ansible-playbook ovirt_vm.yml

