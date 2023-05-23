# ansible-apps_oxidized_exporter

[![Galaxy Role](https://img.shields.io/badge/galaxy-apps_oxidized_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_oxidized_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_oxidized_exporter.svg)](https://github.com/lotusnoir/ansible-apps_oxidized_exporter/releases/latest)
[![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_oxidized_exporter?color=orange&style=flat)](https://galaxy.ansible.com/lotusnoir/apps_oxidized_exporter)
[![downloads](https://img.shields.io/ansible/role/d/52260)](https://galaxy.ansible.com/lotusnoir/apps_oxidized_exporter)
[![Ansible Quality Score](https://img.shields.io/ansible/quality/52260)](https://galaxy.ansible.com/lotusnoir/apps_oxidized_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)

## Description

Deploy [oxidized_exporter](https://github.com/momorientes/oxidized_exporter) to expose oxidized metrics to prometheus.
## Requirements

none

## Role variables

See [variables](/defaults/main.yml) for more details.

## Examples

        ---
        - hosts: apps_oxidized_exporter
          become: true
          become_method: sudo
          gather_facts: true
          roles:
            - role: ansible-apps_oxidized_exporter

## Grafana Dashboard

You can find a grafana dashboard [here](https://grafana.com/grafana/dashboards/13556)

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.

## Author Information

- [Philippe LEAL](https://github.com/lotusnoir)
