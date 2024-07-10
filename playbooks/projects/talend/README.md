Playbook example command:

# ansible-playbook -i '10.65.100.111,' -e "integration_mounts_src=//mt2asvm9/k8s_int_tld_qa/IntegrationPlatform" -e "integration_env=DevQA" deploy-integration-cifs-mount.yml -u root -k
# ansible-playbook -i 'mt2a9vmf0075v.kxsrd.io,' -e "integration_env=Prod" deploy-integration-cifs-mount.yml -u adminpoleary -b -k

Key Variables:

integration_mounts_src: location of the CIFS share (defined in cifs-shares.yml or via extra vars on cmdline)
integration_mounts: all the subfolders in the mount that need to be created, dict format, file and dir mode have default values of 0766 and 0777
integration_env: specified as an extra variable on cmdline to dictate which ENV to deploy to. (folder structure will key off this)

