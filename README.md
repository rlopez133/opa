# Open Policy Agent Install Collection 

## What This Collection Does
This Ansible collection installs and configures an Open Policy Agent (OPA) server on OpenShift ready to receive policies and evaluate data for policy decisions.


## How to Run this Collection

Within AAP, create a Job Template with the following content. Notice that you will need to get a OpenShift Bearer Token as your Credential. This Bearer Token can be captured from the top right corner of your OpenShift Console selecting 'admin' and then selecting 'Copy login command' which will give you the server and token that you will need to create the credential. 

![image](https://github.com/user-attachments/assets/4d6d4203-be5d-4630-a293-14e4850dbb19)


## How do I add additional policies?

Within the [roles/opa/defaults/main.yml](https://github.com/rlopez133/opa/blob/main/collections/ansible_collections/rlopez/opa/roles/opa/defaults/main.yml) file you can append additional policies and re-run the Ansible playbook to get them added.


These are example policies that are available and currently part of the OPA
install when you run the playbook.yml

```
# OPA policies to load from Git repository
opa_policies:
  - name: allowed_false
    url: "https://raw.githubusercontent.com/TheRealHaoLiu/example-opa-policy-for-aap/main/aap_policy_examples/allowed_false.rego"
  - name: extra_vars_validation
    url: "https://raw.githubusercontent.com/TheRealHaoLiu/example-opa-policy-for-aap/main/aap_policy_examples/extra_vars_validation.rego"
  - name: extra_vars_whitelist
    url: "https://raw.githubusercontent.com/TheRealHaoLiu/example-opa-policy-for-aap/main/aap_policy_examples/extra_vars_whitelist.rego"
  - name: global_credential_allowed_false
    url: "https://raw.githubusercontent.com/TheRealHaoLiu/example-opa-policy-for-aap/main/aap_policy_examples/global_credential_allowed_false.rego"
  - name: maintenance_window
    url: "https://raw.githubusercontent.com/TheRealHaoLiu/example-opa-policy-for-aap/main/aap_policy_examples/maintenance_window.rego"
  - name: mismatch_prefix_allowed_false
    url: "https://raw.githubusercontent.com/TheRealHaoLiu/example-opa-policy-for-aap/main/aap_policy_examples/mismatch_prefix_allowed_false.rego"
  - name: superuser_allowed_false
    url: "https://raw.githubusercontent.com/TheRealHaoLiu/example-opa-policy-for-aap/main/aap_policy_examples/superuser_allowed_false.rego"
  - name: team_based_extra_vars_restriction
    url: "https://raw.githubusercontent.com/TheRealHaoLiu/example-opa-policy-for-aap/main/aap_policy_examples/team_based_extra_vars_restriction.rego"
```
