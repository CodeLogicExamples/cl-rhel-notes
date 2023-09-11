# cl-rhel-notes
# Acquire new package:
wget http://repo.codelogic.com/redhat/RPMS/noarch/codelogic-23.14.11.noarch.rpm

# Uninstall agents:
sudo dnf erase codelogic-java codelogic-sql

# Uninstall previous version:
sudo dnf erase codelogic

# Install Codelogic:
sudo dnf install -y ./codelogic-23.14.11.noarch.rpm

# Run pre-install script, then answer questions.
sudo /opt/codelogic/pre_start_codelogic.sh

# Log into UI, and apply license file.
![image](https://github.com/CodeLogicExamples/cl-rhel-notes/assets/89859574/66233cef-8627-43b7-b549-bebb99aacd69)

# Install agents:
wget http://<codelogic-host>/codelogic/server/packages/install_agents.tar \n
tar -xvf install_agents.tar \n
./install_agents.sh -d codelogic_host \n

# Approve agents in CodeLogic UI:
![image](https://github.com/CodeLogicExamples/cl-rhel-notes/assets/89859574/5d11f911-81b8-44cd-9a51-389fb11badb7)


