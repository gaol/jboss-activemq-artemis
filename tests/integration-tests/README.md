# Reproducer for https://issues.apache.org/jira/browse/ARTEMIS-506

This contains a byteman rule to skip deleting page complete record.

To reproduce the failure, in `tests/integration-tests`, run:

    $ mvn clean -DskipIntegrationTests=false test -Dtest=org.apache.activemq.artemis.tests.integration.client.PagingTest#testDeletePhysicalPages

> **Note**
> 
> This reproducer can only be used to verify solution at PR: https://github.com/apache/activemq-artemis/pull/495
> 
