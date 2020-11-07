# Elastic Architectures

This directory provides a series of layouts for Elasticsearch clusters.  The goal is to share architectures of various data flows for environments using the Elastic Stack.

## Architecture #1

A relatively standard pattern of having one Elastic cluter per environment, with each environment having its own Kibana instance.  Each cluster is ingesting data from data sources only from its environment.

![architecture-1.png](images/architecture-1.png)

## Architecture #2

A pattern involving one Elastic cluter per environment, but consolidating Kibana activity to a single Kibana CCS Head for all environments.  Typically, this Kibana instance can be read-only for the majority of users accessing it.  A read-write Kibana instance can be deployed into a lower environment that gives users read-write permissions to create & edit Dashboards, ML jobs, etc.

Pros:

- Having a Kibana CCS Head allows you to see across all environments to compare behavior

![architecture-2.png](images/architecture-2.png)

### Contribute

You can add an architecture if it is new or a variant of an existing one.  To do so, fork the repo, increment the last architecture number, and submit a pull request.

For example, if the last architecture is labeled #23, submit yours and label #24.  This makes it easy to uniquely identify a specific architecture.  Update the REAME.md to include your architecture with a short description about it.