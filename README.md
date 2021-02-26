# Miscellany
Intended to be a repository for miscellaneous scripts and tools from Datadog to be shared with the public.

## Disclaimer
These projects are not a part of Datadog's subscription services and are provided for example purposes only. They are NOT guaranteed to be bug free and are not production quality. If you choose to use to adapt them for use in a production environment, you do so at your own risk.

## Contributing
When adding a new script/tool, be sure to do the following:
- Open a PR for review
- Add a link and description to one of the tables above

We encourage creating a subfolder with a separate README that gives more details on the script/tool.

## Scripts & Tools
These scripts and tools live in this repo, some scripts/tools have their own README in their subfolder with further explaintation and usage.

| Name                                                                      | Language    | Function                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [count_hosts_by_tag](./count_hosts_by_tag.py)                             | Python      | This script will return the number of hosts with a given tag applied. If the tag is only the `key` of a `key:value` pair, all related values will be counted.                                                                                                                        |
| [mute_monitors_with_tags](./monitors/mute_monitors_with_tags.py)          | Python      | This script mutes all monitors that are tagged with a set of monitor tags                                                                                                                                                                                                            |
| [linux_odfs_API](./linux_odfs_API.sh)                                     | Bash        | Script to capture linux open file descriptor metrics                                                                                                                                                                                                                                 |
| [query_freshness](./query_freshness.py)                                   | Python      | Report the "freshness" (how long ago a metric was submitted) of a metric. See this [KB](https://help.datadoghq.com/hc/en-us/articles/115001360786-How-to-track-the-freshness-of-a-metric-) for more info                                             |
| [custom_check_shell](./custom_check_shell)                                | Python/Bash | Spins up a VM using vagrant that installs the Datadog agent on it with a simple custom check using shell                                                                                                                                                                             |
| [empty_dash](./empty_dash)                                                | Python      | Creates an empty dashboard for test purposes                                                                                                                                                                                                                                         |
| [get_all_boards](./get_all_boards)                                        | Python      | Gets all boards for a given organization and print out their json. Useful for malformed boards created via the API                                                                                                                                                                   |
| [Remove old dashboards & monitors](./remove_old_dash_monitors)            | Python      | Will remove all old dashboards and monitors from an account belonging to the email as specified in the script's parameter.                                                                                                                                                           |
| [get_hostname_agentversion](./get_hostname_agentversion)                  | Python      | Gets the version of the agent running for each host                                                                                                                                                                                                                                  |
| [s3_permissions](./s3_permissions)                                        | Python      | Checks S3 bucket ACL permissions for read/write access and reports a metric to Datadog                                                                                                                                                                                               |
| [uptime](./uptime)                                                        | Python      | Custom check to track uptime. At the time that this check was written, it wasn't possible to view a monitor's uptime on a dashboard or via the API, or to view uptime with multiple decimals of precision, but please check if those features are available before using this check. |
| [api_limits_as_custom_metrics](./api_limits_as_custom_metrics.py)         | Python      | Gets the Datadog API rate limits from the Datadog API and submits them as metrics                                                                                                                                                                                                    |
| [cross-org-metric-broker](./cross-org-metric-broker.py)                   | Python      | Takes metrics from one account (org) and posts them to another account (org)                                                                                                                                                                                                         |
| [csvmod](./csvmod.py)                                                     | Python      | Example script of grabbing a timeseries and dumping to a CSV                                                                                                                                                                                                                         |
| [dashconverter](./dashconverter)                                          | Python      | Convert from screenboard to timeboard and vice versa                                                                                                                                                                                                                                 |
| [metric_usage_report](./metric_usage_report)                              | Python      | Enter a list of metrics, and receive a report showing where the metrics are used in your account                                                                                                                                                                                                                              |
| [dd_public_ip](./dd_public_ip.sh)                                         | Bash        | Script to run from an AWS instance that will add a tag for the public ip                                                                                                                                                                                                             |
| [fullmetrics_dash](./fullmetrics_dash.py)                                 | Python      | Creates a dashboard for a given integration with all metrics being reported through that integration                                                                                                                                                                                 |
| [hosts_with_aws_without_agent](./hosts_with_aws_without_agent.py)         | Python      | List of ec2 instances without the datadog-agent installed                                                                                                                                                                                                                            |
| [merge_screenboards](./merge_screenboards)                                | Python      | Takes two screenboards and combines them into one                                                                                                                                                                                                                                    |
| [migrate_dashboard](./migrate_dashboard.py)                               | Python      | Migrate a screenboard from one account (or org) to another                                                                                                                                                                                                                           |
| [migrate_monitors](./migrate_monitors.py)                                 | Python      | Migrate monitors by query from one account (or org) to another                                                                                                                                                                                                                       |
| [dash_to_json](./dash_to_json.py)                                         | Python      | Convert Dashboard to JSON and Create Dashboard from JSON                                                                                                                                                                                                                             |
| [import_screenboard](./Dashboards/import_screenboard.py)                  | Python      | Creates a new screenboard from json                                                                                                                                                                                                                                                  |
| [export_screenboard](./Dashboards/export_screenboard.py)                  | Python      | Exports a single screenboard to a json file                                                                                                                                                                                                                                          |
| [base_scripts](./base_scripts)                                            | Python      | A collection of generic scripts that can be used as a starting point for creating your own custom scripts                                                                                                                                                                            |
| [remove_lingering_aws_host_tags](./remove_lingering_aws_host_tags.py)     | Python      | This is a tool for removing AWS host-level tags from your infrastructure in Datadog. It is intended for users who have removed their EC2 instances from their AWS integration and if they no longer want to see AWS tags associated with the hosts that still run datadog-agents.    |
| [remove_single_tag_tmp](./remove_single_tag_tmp.py)                       | Python      | Removes a single tag from a host                                                                                                                                                                                                                                                     |
| [update_multiple_monitors_example](./update_multiple_monitors_example.py) | Python      | example of how to update multiple monitors at once                                                                                                                                                                                                                                   |
| [create_monitor](./create_monitor)                                        | Python      | simple example of creating metric query monitor with thresholds                                                                                                                                                                                                                      |
| [weatherExample](./custom_agent_checks/weatherExample.py)                 | Python      | Example script that submits the temperature and wind speed from the Wunderground API to Datadog as metrics                                                                                                                                                                           |
| [sql_redacted](./custom_agent_checks/sql_redacted.py)                     | Python      | Submits a metric based on a SQL query                                                                                                                                                                                                                                                |
| [multi_org_create_users](./multi_org_create_users)                        | Python      | Creates multiple Datadog users across multiple Datadog Orgs                                                                                                                                                                                                                          |
| [create_monitor_terraform](./create_monitor_terraform)                    | Terraform   | Creates a monitor using Terraform                                                                                                                                                                                                                                                    |
| [query hosts and create tags](./query_hosts_create_tags.py)               | Python      | queries hosts api using pagination and creates new tags                                                                                                                                                                                                                              |
| [get all groups in a monitor](./monitors/get_groups_in_monitor.py)               | Python      | queries for all groups in a monitor and outputs a list of them                                                                                                                                                                                                                |
| [create a csv file with a list of log in handles](./create_email_list.py)     | Python       | creates a CSV file in the same directory as the script containing a list of all user log in handles                                                                                                                                                                            |
| [Powershell script to call JSON REST endpoint, pass those key-value pairs to DogstatsD](./requester.ps1)     | Powershell       | A Powershell script which will call a given HTTP GET endpoint, and then submit the key-value pairs found in the resulting JSON body to DogsStatsD. Resource endpoint must be a non-nested JSON body ({"a":"1","b":"2"} -> custom metrics: a\|1, b\|2                                                                                                                                                                                                            |
| [Dogmover](./Dogmover)							| Python	| Migrate screenboards, timeboards and monitors from one organization to another (supports migrations between US>EU instances.)                                                                                                                                                                                                  |
| [Update Host Tags with Host Metadata (example)](./update_host_tags_using_metadata_example.py)							| Python	| Queries the host API then creates tags based off of the gohai (or other) metadata.                                                                                                                                                                      |
| [Historic usage to CSV](./historic_usage_to_csv.py)							| Python	| This script is meant to pull historical usage metrics and export them to CSV.                                                                                                                                                                      |
| [dd_aws_add_account.py](./dd_aws_add_account.py)							| Python	| script for creating aws integration                                                                                                                                                                 |
| [Send_filesystem_events](./send_filesystem_events)                        | Python    | This script uses inotify to send an event to the event stream when it detects a change in files or folders in a given directory.   |
| [create_users_and_emails_list.py](./create_users_and_emails_list.py)							| Python	| script to get a list of user emails as csv                                                                          |
| [DD User Report (JSON)](./dd-user-report-json)							| Python	| Generates various different user reports and pretty prints the json for further processing -- useful for large orgs with 100s or 1000s or users  |
| [Get All Public Dashboards](./all_dash_public)							| Python	| Gets a full list (returned as JSON) of all dashboards that are public for a given organization  |
| [Get All Child Orgs](./get_all_child_orgs)							| Python	| Gets a full list (returned as JSON) of all child organizations for a given organization  |
| [PySNMP-MIB-Parser](./PySNMP-MIB-Parser)							| Python	| Converts a MIB file (in PySNMP format) to a yaml file that can be used by Datadog's [SNMP agent integration](https://docs.datadoghq.com/integrations/snmp/)  |
| [aws_hosts_without_agent.py](./aws_hosts_without_agent.py)	| Python	| Gets a list of hostnames and IPs for AWS hosts not running the agent |
| [DD Example](./dd-example)	| N/A	| Spins up a k8s cluster using Minikube with a simple app and database, showcasing the Datadog daemonset, has APM, Logs, and Metrics |
| [Packer Image Build + Terraform Deploy with AWS Secrets Manager and Datadog Agent](./agent_bootstrapping/README.md) | N/A | A guide that helps you to build an AMI with updates + Datadog Agent preinstalled using Packer, and deploy to AWS using Terraform while storing your Datadog API key in AWS Secrets Manager and using an IAM Instance Profile to retrive it at deployment time. |

## Additional tools
These are some additional tools and scripts written by Datadog.

| Name                                                    | Language | Function                                     |
|---------------------------------------------------------|----------|----------------------------------------------|
| [csv_exporter](https://github.com/DataDog/csv_exporter) | Python   | Exports a given metric from Datadog as a csv |

## Getting started
For any Python code, you'll want to run:
```
pip install datadog
```
