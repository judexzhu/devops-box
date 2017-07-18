# DevOps box
* A vagrant project with an ubuntu box with the tools needed to do DevOps

# tools included
* Terraform
* AWS CLI
* Ansible
* Packer
---

Typing `vagrant` from the command line will display a list of all available commands.

Be sure that you are in the same directory as the Vagrantfile when running these commands!

# Common Vagrant Commands
- `vagrant up`          -- starts vagrant environment (also provisions only on the FIRST vagrant up)
- `vagrant status`      -- outputs status of the vagrant machine
- `vagrant halt`        -- stops the vagrant machine
- `vagrant reload`      -- restarts vagrant machine, loads new Vagrantfile configuration
- `vagrant provision`   -- forces reprovisioning of the vagrant machine
- `vagrant ssh`         -- connects to machine via SSH
- `vagrant destroy`     -- stops and deletes all traces of the vagrant machine

# Tips
- `vagrant -v`                    -- Get the vagrant version
- `vagrant global-status`         -- outputs status of all vagrant machines
- `vagrant global-status --prune` -- same as above, but prunes invalid entries
- `vagrant suspend`               -- Suspends a virtual machine (remembers state)
- `vagrant resume`                -- Resume a suspended machine (vagrant up works just fine for this as well)
- `vagrant reload --provision`    -- Restart the virtual machine and force provisioning
- `vagrant provision --debug`     -- Use the debug flag to increase the verbosity of the output
- `vagrant push`                  -- Yes, vagrant can be configured to [deploy code](http://docs.vagrantup.com/v2/push/index.html)!
- `vagrant up --provision | tee provision.log`  -- Runs `vagrant up`, forces provisioning and logs all output to a file

# Notes
- If you are using [VVV](https://github.com/varying-vagrant-vagrants/vvv/), you can enable xdebug by running `vagrant ssh` and then `xdebug_on` from the virtual machine's CLI.
