# Ansible Role: ansible-apps_oxidized_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_oxidized_exporter.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_oxidized_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_oxidized_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_oxidized_exporter)
[![GitHub tag](https://img.shields.io/badge/version-0.1.0-blue?style=flat)](https://github.com/lotusnoir/ansible-apps_oxidized_exporter/releases/tag/0.1.0) 

Deploy [oxidized_exporter](https://github.com/momorientes/oxidized_exporter) to expose oxidized metrics to prometheus.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `oxidized_exporter_port` | 9120 | port to expose prometheus metrics |
| `oxidized_web_url` | https://oxidized.example.net | web url of the oxidized application |

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
