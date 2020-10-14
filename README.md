# The Base Setup
<pre>
#----------------------------------------------------------------------------------------#
#- Ping Identity DG Training Stack                                                      -#
#-                                                                                      -#
#-         rest                                                                         -#
#-         5443                                                                         -#
#-          |                                                                           -#
#-   +----------------+                                                                 -#
#-   | PingDataGovPAP |                                                                 -#
#-   +----------------+                                                                 -#
#-                                                                                      -#
#-     login  console            console         rest    ldaps            rest          -#
#-     8031   8999               7443            4443    4636             6443          -#
#-      |      |                  |                |       |                |           -#
#-   +---------------+    +---------------+    +---------------+    +---------------+   -#
#-   | PingFederate  |    |PingDataConsole|    | PingDirectory |    |  PingDataGov  |   -#
#-   +---------------+    +---------------+    +---------------+    +---------------+   -#
#-                                                                                      -#
#-   +------------------------+-------------------------------------------------------+ -#
#-   |  Product Console/App   | URL                                                   | -#
#-   |                        |   username: administrator                             | -#
#-   |                        |   password: 2FederateM0re                             | -#
#-   +------------------------+-------------------------------------------------------+ -#
#-   |  PingFederate          | https://localhost:8999/pingfederate/app               | -#
#-   |  PingDirectory         | https://localhost:4443/  (REST and Consent API)       | -#
#-   |  PingDataGovernance    | https://localhost:6443/  (Gateway, SCIM, and PDP API) | -#
#-   |  PingDataGovernancePAP | https://localhost:5443/login                          | -#
#-   |  PingDataConsole       | https://localhost:7443/console  (Admin Console for    | -#
#-   |                        |                                  PingDirectory and    | -#
#-   |                        |                                  PingDataGovernance)  | -#
#-   +------------------------+-------------------------------------------------------+ -#
#----------------------------------------------------------------------------------------#
</pre>
Variables required to point to base in (server-profiles) and out for images
    DG81_TRG_IN_BASE
    DG81_TRG_OUT_BASE

    Example:
        export DG81_TRG_IN_BASE-/_devOps/dg81-lab-setup-project/dg81-lab-setup/server-profiles/
        export DG81_TRG_OUT_BASE-/_devOps/docker-volumes/
    
