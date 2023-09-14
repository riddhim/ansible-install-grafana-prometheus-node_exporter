Issues encountered and Lesson learned:

TASK [grafana : change admin password for grafana gui] *********************************************************************************************************************
fatal: [65.1.112.138]: FAILED! => {"msg": "The task includes an option with an undefined variable. The error was: 'abc1234' is undefined\n\nThe error appears to be in '/home/ubuntu/ansible/roles/grafana/tasks/main.yml': line 42, column 3, but may\nbe elsewhere in the file depending on the exact syntax problem.\n\nThe offending line appears to be:\n\n\n- name: change admin password for grafana gui\n  ^ here\n"}


Resolution-->As provided grafana password without passing variable

The error appears to be in '/home/ubuntu/ansible/roles/grafana/tasks/main.yml': line 2, column 3, but may
be elsewhere in the file depending on the exact syntax problem.

The offending line appears to be:

---
- grafana_admin_password: "abc1234"

Resolution-->Define grafana admin password in grafana_admin_password
