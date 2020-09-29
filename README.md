# Ansible Role: ansible-apps_oxidized_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_oxidized_exporter.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_oxidized_exporter)[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__oxidized_exporter-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_oxidized_exporter/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_oxidized_exporter/tags)

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
	  gather_facts: no
	  roles:
	    - role: ansible-apps_oxidized_exporter
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
