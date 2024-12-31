# command-line flags 

### 1. **Ansible Command-Line Flags**

Ansible is a powerful automation tool used for configuration management, application deployment, and task automation.

- **`-i`**: Specifies the inventory file.
  ```bash
  ansible-playbook -i inventory_file playbook.yml
  ```

- **`-u`**: Specifies the user to connect as.
  ```bash
  ansible-playbook -u username playbook.yml
  ```

- **`-b`**: Runs commands with `sudo` privileges (become).
  ```bash
  ansible-playbook -b playbook.yml
  ```

- **`-K`**: Asks for the `sudo` password.
  ```bash
  ansible-playbook -K playbook.yml
  ```

- **`--check`**: Runs a dry run without making any changes.
  ```bash
  ansible-playbook --check playbook.yml
  ```

- **`-v`, `-vv`, `-vvv`**: Increases the verbosity of the output.
  ```bash
  ansible-playbook -v playbook.yml
  ```

- **`--limit`**: Limits execution to a specific group or host.
  ```bash
  ansible-playbook --limit host1 playbook.yml
  ```

- **`--tags`**: Runs specific tasks tagged in the playbook.
  ```bash
  ansible-playbook --tags install playbook.yml
  ```

---

### 2. **Git Command-Line Flags**

Git is a version control system for tracking changes in code and files.

- **`-b`**: Creates a new branch.
  ```bash
  git checkout -b new-branch
  ```

- **`-m`**: Specifies a commit message.
  ```bash
  git commit -m "Commit message"
  ```

- **`--amend`**: Amends the previous commit.
  ```bash
  git commit --amend
  ```

- **`-a`**: Stages all changes before committing.
  ```bash
  git commit -a -m "Commit message"
  ```

- **`-u`**: Sets the upstream branch for tracking.
  ```bash
  git push -u origin master
  ```

- **`--global`**: Sets global Git configuration.
  ```bash
  git config --global user.name "Name"
  ```

- **`--hard`**: Resets the working directory to match the commit.
  ```bash
  git reset --hard HEAD
  ```

- **`-d`**: Deletes a branch.
  ```bash
  git branch -d branch-name
  ```

---

### 3. **Docker Command-Line Flags**

Docker is used for containerizing applications and running them in isolated environments.

- **`-d`**: Runs containers in detached mode (in the background).
  ```bash
  docker run -d image-name
  ```

- **`-p`**: Maps container ports to host ports.
  ```bash
  docker run -p 80:80 image-name
  ```

- **`-v`**: Mounts a volume.
  ```bash
  docker run -v /host/path:/container/path image-name
  ```

- **`--name`**: Assigns a custom name to a container.
  ```bash
  docker run --name my-container image-name
  ```

- **`--rm`**: Automatically removes a container when it stops.
  ```bash
  docker run --rm image-name
  ```

- **`-e`**: Sets environment variables.
  ```bash
  docker run -e VAR=value image-name
  ```

- **`docker-compose`**:
  - **`-f`**: Specifies the Compose file.
    ```bash
    docker-compose -f docker-compose.yml up
    ```

  - **`-d`**: Runs in detached mode.
    ```bash
    docker-compose up -d
    ```

---

### 4. **Kubernetes (kubectl) Command-Line Flags**

Kubernetes is a system for automating the deployment, scaling, and management of containerized applications.

- **`get`**: Retrieves resources (e.g., pods, deployments).
  ```bash
  kubectl get pods
  ```

- **`-n`**: Specifies the namespace.
  ```bash
  kubectl get pods -n namespace-name
  ```

- **`-f`**: Specifies the YAML file for a resource.
  ```bash
  kubectl apply -f deployment.yaml
  ```

- **`create`**: Creates a resource from a YAML file.
  ```bash
  kubectl create -f deployment.yaml
  ```

- **`-o`**: Specifies the output format (e.g., `json`, `yaml`, `wide`).
  ```bash
  kubectl get pods -o wide
  ```

- **`--dry-run`**: Simulates an operation without making any changes.
  ```bash
  kubectl apply -f deployment.yaml --dry-run
  ```

---

### 5. **Terraform Command-Line Flags**

Terraform is an open-source IaC (Infrastructure as Code) tool for managing cloud infrastructure.

- **`plan`**: Previews the actions Terraform will take.
  ```bash
  terraform plan
  ```

- **`-var`**: Sets a variable value.
  ```bash
  terraform plan -var "instance_type=t2.micro"
  ```

- **`apply`**: Applies the changes defined in the Terraform configuration.
  ```bash
  terraform apply
  ```

- **`-auto-approve`**: Skips the approval prompt for `apply`.
  ```bash
  terraform apply -auto-approve
  ```

- **`destroy`**: Destroys the infrastructure managed by Terraform.
  ```bash
  terraform destroy
  ```

---

### 6. **Linux Command-Line Flags**

Linux provides numerous commands with various flags for system administration.

- **`-r`**: Recursively remove directories and files (used with `rm`).
  ```bash
  rm -r directory_name
  ```

- **`-f`**: Force an operation (used with commands like `rm` or `cp`).
  ```bash
  rm -f file_name
  ```

- **`-h`**: Displays help for a command.
  ```bash
  ls -h
  ```

- **`-a`**: Shows hidden files (used with commands like `ls`).
  ```bash
  ls -a
  ```

- **`-l`**: Shows detailed listing (used with commands like `ls`).
  ```bash
  ls -l
  ```

---

### 7. **Shell Script Flags**

Shell scripts often accept flags as input parameters.

- **`$1, $2,...`**: Positional parameters (arguments passed to the script).
  ```bash
  # Example of accessing the first argument
  echo $1
  ```

- **`-e`**: Causes the script to exit on errors.
  ```bash
  set -e
  ```

- **`-x`**: Enables debugging and prints each command.
  ```bash
  set -x
  ```

---

### 8. **AWS CLI Command-Line Flags**

The AWS Command Line Interface (CLI) is used to interact with AWS services from the terminal.

- **`--profile`**: Specifies a named AWS CLI profile.
  ```bash
  aws s3 ls --profile myprofile
  ```

- **`--region`**: Specifies the AWS region.
  ```bash
  aws ec2 describe-instances --region us-east-1
  ```

- **`--output`**: Specifies the output format (e.g., `json`, `table`, `text`).
  ```bash
  aws ec2 describe-instances --output json
  ```

- **`--query`**: Filters the output using JMESPath queries.
  ```bash
  aws ec2 describe-instances --query "Reservations[*].Instances[*].InstanceId"
  ```

- **`--no-paginate`**: Disables pagination for large outputs.
  ```bash
  aws ec2 describe-instances --no-paginate
  ```

---

### Conclusion

These command-line flags across different DevOps tools allow users to modify, control, and automate various tasks efficiently. Flags help customize command executions, whether you're managing infrastructure, configuring software, or automating deployments. Familiarity with these flags will greatly enhance your productivity in a DevOps environment.
