# binding kubernetes admission polices

This Helm chart automates the creation of `ValidatingAdmissionPolicyBinding` resources. It loops through a user-defined array of policies in the values.yaml file, allowing for scalable and efficient policy management.



## Library items (policies)
| Enabled | Control ID | Name | Policy name | Notes | Description |
| --- | --- | --- | --- | --- | --- |
| [x] | PSS-C-001 | Deny Privilege escalation | [pss-privilege-escalation](https://github.com/vap-library/vap-library/blob/main/policies/pss-privilege-escalation/policy.yaml) | Small edits on expression and labels | Prevent privilege escalation in containers |
| [x] | PSS-C-002 | Deny run as user root | [pss-running-as-non-root-user](https://github.com/vap-library/vap-library/blob/main/policies/pss-running-as-non-root-user/policy.yaml) | Small edits on expression and labels | Ensure containers run as non-root users |
| [x] | PSS-C-003 | Deny run as root | [pss-running-as-non-root](https://github.com/vap-library/vap-library/blob/main/policies/pss-running-as-non-root/policy.yaml) | Small edits on expression and labels | Ensure containers do not run as root user (UID 0) |
| [x] | [C-0017](https://kubescape.io/docs/controls/c-0017/) | Immutable container filesystem | [kubescape-c-0017-deny-resources-with-mutable-container-filesystem](https://github.com/kubescape/cel-admission-library/blob/main/controls/C-0017/policy.yaml) | | Ensure containers use read-only root filesystem |
| [x] | [C-0057](https://kubescape.io/docs/controls/C-0057/) | Privileged container | [kubescape-c-0057-privileged-container-denied](https://github.com/kubescape/cel-admission-library/blob/main/controls/C-0057/policy.yaml) | | Deny privileged container |
| [x] | AS-C-001 | Container should DROP all capabilities | as-c-001-should-drop-all-capabilities |
