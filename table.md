| **Name** | **Value**  |
|:---|:--- |
| build_code | abc |
| cause | TRIGGERED_VIA_RAIPC |
| created_date | 2018-04-24T13:34:33.654759Z |
| dockertag_name | latest |
| id | 23028946 |
| last_updated | 2018-04-24T13:36:39.537606Z |
| name | my-image |
| repository | test/my-image |
| source | docker.hub |
| status | -1 |
| type | build |
| user | test |
| entity | docker.hub |
| rule data type | message |
| expression | (true &#124;&#124; elapsedTime(update_ms) < 24*60*60000)&#13;&& ( tags.status NOT IN ('0', '3', '10') &#13;  &#124;&#124; tags.status = '0' && (now.getMillis() - create_ms) > 60*60000 ) |
| rule_filter | type = 'build' && source = 'docker.hub' |
| severity | warning |
| alert_type | OPEN |
| timezone | MSK (+03:00) |
| event_time | 2018-04-27 00:16:31 |
| received_time | 2018-04-27 00:16:31 |
| alert_open_time | 2018-04-27 00:16:31 |
| create_ms | 1524576873654 |
| update_ms | 1524576999537 |
| st | -1 |
| status_desc | Failed |
| lnk | https://hub.docker.com/r/test/my-image/builds/abc |
| eps | 200392256 |
| var create_ms | milliseconds(tags.created_date) |
| var update_ms | milliseconds(tags.last_updated) |
| var st | tags.status |
| var status_desc | st = '-1' ? 'Failed' : (st = '0' ? 'Queued' : (st = '3' ? 'Pending' : (st = '10' ? 'Completed' : st))) |
| var lnk | 'https://hub.docker.com/r/' + tags.repository + '/builds/' + tags.build_code |
| var eps | elapsedTime(update_ms) |
