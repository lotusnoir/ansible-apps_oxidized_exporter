# Ansible Role: ansible-apps_oxidized_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_oxidized_exporter.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_oxidized_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_oxidized_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_oxidized_exporter)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_oxidized_exporter?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52260)
[![downloads](https://img.shields.io/ansible/role/d/52260)](https://galaxy.ansible.com/lotusnoir/apps_oxidized_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_oxidized_exporter.svg)](https://github.com/lotusnoir/ansible-apps_oxidized_exporter/releases/) 
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_oxidized_exporter&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_oxidized_exporter)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_oxidized_exporter&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_oxidized_exporter)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_oxidized_exporter&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_oxidized_exporter)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_oxidized_exporter&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_oxidized_exporter)


Deploy [oxidized_exporter](https://github.com/momorientes/oxidized_exporter) to expose oxidized metrics to prometheus.

## Role variables

| Name                     | Default Value                | Description                           |
| ------------------------ | ---------------------------- | --------------------------------------|
| `oxidized_exporter_port` | 9120                         | port to expose prometheus metrics     |
| `oxidized_web_url`       | https://oxidized.example.net | web url of the oxidized application   |

## Examples

	---
	- hosts: apps_oxidized_exporter
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_oxidized_exporter
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}


## Grafana Dashboard

You can find a grafana dashboard [here](https://grafana.com/grafana/dashboards/13556)


## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
