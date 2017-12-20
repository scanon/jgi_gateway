
# jgi_gateway

(A [KBase](https://kbase.us) module generated by the [KBase SDK](https://github.com/kbase/kb_sdk).)

A KBase dynamic service serving as a gateway to the JGI JAMO search service (JJS). 

## Features

### Persistent Staging Log

The JGI JAMO Search service (JJS) provides an api call to request the transfer of a file from the JAMO system to the KBase staging area for a given user. The file transfer request is associated with a job id, which is returned by the api call. JJS also provides an api call to provide the current status of that request. However JJS does not provide a way of providing any query of the transfer job queue. Therefore, the gateway cannot obtain a list of jobs per user, or jobs overall. Since all transfer requests are routed through the gateway, however, it can be used to provide a persistent searchable collection of all job requests, by user or over all.

Implementation

The gateway transfer database is implemented as a simple mongodb collection



