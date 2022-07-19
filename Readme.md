## Farmacias del Ahorro - Harness Delegates Intsllation

### How to run the playbook [Local Testing]

change the values for the --extra-vars variables
- cdcg_delegate_url: url is a one time download; generate a new download link from the harness platform
- gitlab_secret_id: be aware of gitlab_application_id set on `group_vars/macos.yml`

```bash
ansible-playbook local-test.yml -i inventory -K \
    --extra-vars="cdcg_delegate_url=https://app.harness.io/gratis/api/setup/delegates/docker?accountId=tNj0VHWCSYK3Qk9ryqi6Fg&token=eyJhbGciOiJIUzI1NiJ9.eyJyZXNvdXJjZSI6ImRlbGVnYXRlLnROajBWSFdDU1lLM1FrOXJ5cWk2RmciLCJpc3MiOiJIYXJuZXNzIEluYyIsImV4cCI6MTY1ODI1NzMwOCwiaWF0IjoxNjU4MjUzNzA4fQ.CD9JOO8l0zmY1KdoiHjTAo_4ShRGfvONzb17XMXiKYQ&delegateName=test&delegateProfileId=DwTp4l0iQEyeD_e9vryClQ&tokenName=default" \
    --extra-vars="gitlab_secret_id=98fb822ef185899202af62b5551b2c225dd3332ced6ee6ce354287a1120d1621"
```

### How to run the playbook [Farmacias del Ahorro Environment]

set the values for the --extra-vars variables
- cdcg_delegate_url
- gitlab_secret_id

```bash
$ ansible-playbook main.yml -u alejandro.talamantes -kK \
    --extra-vars="cdcg_delegate_url=" \
    --extra-vars="gitlab_secret_id="
```