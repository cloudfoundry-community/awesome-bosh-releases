# awesome-bosh-releases
Directory of bosh releases, with meta-data

# intro

In the spirit of https://github.com/stefanbuck/awesome-browser-extensions-for-github this page provides a community-maintained list of bosh releases, with additional qualitative meta-data. Hopefuly, this should fade out in favor of [bosh hub](http://bosh.io/releases) when it becomes possible to attach meta-data to bosh releases or to bosh-hub.

# releases

| release name               | category   | sub-type                | tech. version   | url                                                                      | maturity                           | main contributors   | maintained   | Backlog                                                 | HA in AZ   | Multi-az   | Broker included ??  | app usage  | comment                                                                              | Backup/restore ? |
| -------------------------- | ---------- | ----------------------- | --------------- | ------------------------------------------------------------------------ | ---------------------------------- | ------------------- | ------------ | --------                                                | ---------- | ---------- | ------------------- | ---------- | ---------                                                                            | ---------------- |
| P-mysql                    | service    | RDBMS                   | Mysql + galera  | https://github.com/cloudfoundry/cf-mysql-release                         | commercial                         | pivotal             | yes          | [url](https://www.pivotaltracker.com/n/projects/969486) | yes        | yes        | yes                 | dev        | schema as a service (isolation w.r.t. other workloads)                               | N                |
| Postgres-docker            | service    | RDBMS                   | pgsql           | http://github.com/cloudfoundry-community/postgresql-docker-boshrelease   | poc                                | Stark & wayne       | ?            |                                                         | no         | no         |                     | dev        |                                                                                      | N                |
| Cassandra                  | service    | NOSQL                   | Cassandra 1.2.3 | https://github.com/emc-cloudfoundry/cassandra-cf-service-boshrelease     | runs-in-prod                       | Emc-content         | semi         |                                                         | yes        | yes        |                     | prod       |                                                                                      | N                |
| Riak-cs                    | service    | Object storage          |                 | https://github.com/cloudfoundry/cf-riak-cs-release                       | commercial                         | pivotal             | yes          | [url](https://www.pivotaltracker.com/n/projects/969486) | yes        | planned    | yes                 | prod       |                                                                                      | N                |
| P-redis                    | service    |                         | redis           |                                                                          | commercial                         | pivotal             | yes          |                                                         | yes        |            | yes                 | prod       |                                                                                      | N                |
| Memcache-hazelcast         | service    | Caching                 | hazelcast       | https://github.com/cloudfoundry-community/memcache-release               | runs-in-prod                       | lds                 | yes          |                                                         | yes        |            | yes                 | prod       |                                                                                      | N                |
| Swift                      | service    | Object storage          |                 | https://github.com/emc-cloudfoundry/swift-boshrelease                    | runs-in-prod                       | Emc-content         | semi         |                                                         | yes        |            | no                  | prod       |                                                                                      | N                |
| P-rabbit                   | service    |                         | Rabbit-mq       | https://github.com/pivotal-cf/cf-rabbitmq-release                        | commercial                         | pivotal             | yes          | [url](https://www.pivotaltracker.com/n/projects/969486) | yes        |            | yes                 | prod       |                                                                                      | N                |
| Mongo-db service contrib   | service    |                         |                 |                                                                          | runs-in-prod                       | pivotal             | no           |                                                         | no         |            | v1                  | dev        | [alternative broker](https://github.com/pivotalservices/cf-logsearch-service-broker) | N                |
| Log-search                 | service    | Log & metrics storage   | ELK             | http://logsearch.io/                                                     | runs-in-prod                       | city bank           | yes          |                                                         | yes        |            | no                  | dev        |                                                                                      | N                |
| hadoop                     | service    | BIG DATA                | Hadoop 2.2.0    | http://bosh.io/releases/github.com/cf-platform-eng/hadoop-boshrelease    | poc                                |                     | no           |                                                         | yes        |            | no                  |            |                                                                                      | N                |
| gemfire                    | service    | NOSQL                   | gemfire         | https://github.com/Pivotal-Field-Engineering/gemfire-bosh-release        | poc (commercial version private)   | pivotal             | no           |                                                         |            |            |                     |            |                                                                                      | N                |
| crate                      | service    | nosql                   | crate           | https://github.com/cloudfoundry-community/crate-boshrelease              | poc                                | pivotal             | semi         |                                                         | ?          |            |                     | dev        |                                                                                      | N                |
| consul                     | service    | discovery               | consul          | https://github.com/cloudfoundry-community/consul-boshrelease             | Opensource,??                      | stark & wayne       | yes          |                                                         | ?          |            |                     |            |                                                                                      |                  |
| HANA                       | service    | db                      |                 | https://github.com/cloudfoundry-community/cf-hanadb-broker               | ?                                  | SAP                 | no           |                                                         |            |            |                     |            |                                                                                      |                  |
| clam-av                    | service    | anti-virus scanner      |                 | https://github.com/emc-cloudfoundry/clamav-boshrelease                   |                                    | Emc-content         |              |                                                         |            |            |                     |            |                                                                                      |                  |
|                            |            |                         |                 |                                                                          |                                    |                     |              |                                                         |            |            |                     |            |                                                                                      |                  |
| concourse                  | ci         |                         | consourse       |                                                                          |                                    |                     |              |                                                         |            |            |                     |            |                                                                                      |                  |
| jenkins                    | ci         |                         | jenkins         | https://github.com/cloudfoundry-community/jenkins-boshrelease            | Opensource,??                      | rakuten,            | yes          |                                                         |            |            |                     |            |                                                                                      |                  |
|                            |            |                         |                 |                                                                          |                                    |                     |              |                                                         |            |            |                     |            |                                                                                      |                  |
| docker                     | infra-frmk |                         |                 | https://github.com/cf-platform-eng/docker-boshrelease                    | poc                                | pivotal             |              |                                                         |            | no         | yes                 | n/a        |                                                                                      |                  |
| mesos                      | infra-frmk |                         |                 | http://bosh.io/releases/github.com/cf-platform-eng/mesos-boshrelease     | poc                                | pivotal             |              |                                                         |            |            |                     |            |                                                                                      |                  |
|                            |            |                         |                 |                                                                          |                                    |                     |              |                                                         |            |            |                     |            |                                                                                      |                  |
| admin-ui                   | running-cf |                         |                 |                                                                          | runs-in-prod                       |                     |              |                                                         |            |            |                     |            |                                                                                      |                  |
| deployment-vm-boshrelease  | running-cf | cf ops CLIs             |                 | https://github.com/emc-cloudfoundry/deployment-vm-boshrelease            | runs-in-prod                       | Emc-content         |              |                                                         |            |            |                     |            |                                                                                      |                  |

# Classification details

Some details on the semantics of columns in the table above

category:
  * service: suiteable for appearing in cf market place
  * infra-frmk: infrastructure to build something else. Unrelated to CF
  * running-cf: useful when running/operating a CF instance

maturity:
  * poc: proof of concept
  * runs-in-prod: runs in production by some folks, ask them for more. Not necessary support production workloads (may be suppporting dev activities, see app use cases)
  * commercial: commercial product with support provided

app usage: for services, is the service ready for supporting development or production ?


# faq

## I can't see the whole table, its truncated

On chrome, consider installing https://github.com/stefanbuck/awesome-browser-extensions-for-github#githubexpandinizr-

Otherwise, scroll right with keyboard or gesture on touch screens

Finally, look at the [raw markdown](https://raw.githubusercontent.com/cloudfoundry-community/awesome-bosh-releases/master/README.md)

## Should this be moved to cf-contrib wiki ?

Was tried, the side bar makes it harder to scroll and eats up some screen space. What about pointing to this repo from cf-contrib instead ? 

## How can I sort, filter this table ?

No, you can't.

May be we could convert the table in json format and have a CSS stylesheet do the rendering ?

Should this be moved to a google spread sheet ?

## Why are you contributing this ?

Some colleagues of Guillaume Berche asked for a summary of services states. He started as a private spread sheet and then thought it might be useful to others. Let's see if this is the case. If not, we might delete this repo to avoid polutting the cf-community repo namespace.

## Contributing and opinions

Some of this content, such as maturity, is subjective and deserves healthy constructive discussions and debates? Let's have them on the [cf-bosh](mailto:cf-bosh@lists.cloudfoundry.org) mailing list of through issues.

Otherwise, as usual, the cf community is invited to improve this repo through which ever is easier
*  direct git pushes (e.g. edit github button) if you're member of the community
*  PRs 

## How to productively edit this huge table ?

You may want to give a try to intellij ultimate cucumber plugin which natively supports table formatting. This makes it easy to reformat the table. In addition, the multi-cursor support, allows to edit the while column.

Not convenient? Would you prefer to contribute with something else ? (google spready sheet, others) ? Lets discuss that over issues

It was bootstraped from csv-formatted spreadsheet to markdown with http://www.tablesgenerator.com/markdown_tables



