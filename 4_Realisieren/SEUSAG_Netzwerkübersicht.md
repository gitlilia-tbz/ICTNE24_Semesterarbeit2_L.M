Seusag / Netzwerkübersicht

| 🤖 Disclamer: Diese Grafik durch Claude-AI gestützt                        |
| -------------------------------------------------------------------------- |
| [Siehe diesen Link für weitere Informationen](../Quellen_und_Disclamer.md) |


```mermaid
graph TB
    subgraph Host[Local Machine]
        subgraph Docker[Docker Engine]
            subgraph Network [Docker Network: 172.20.0.0/16]
                subgraph Zabbix[Zabbix]
                    style Zabbix fill:#ffcccc,color:#000000
                    mysql[MySQL<br>172.20.0.2]
                    zserver[Zabbix Server<br>172.20.0.3<br>Port 10051]
                    zweb[Zabbix Web<br>172.20.0.4<br>Port 8082:8080]
                    zagent[Zabbix Agent<br>172.20.0.5<br>Port 10050]
                end
                
                subgraph Target[Monitoring Target]
                    style Target fill:#ffe6cc,color:#000000
                    ubuntu[Ubuntu Server<br>172.20.0.6<br>Port 10055:10050]
                end
                
                subgraph Zammad[Zammad]
                    style Zammad fill:#d6f5d6,color:#000000
                    postgres[PostgreSQL<br>172.20.0.10]
                    elastic[Elasticsearch<br>172.20.0.11]
                    redis[Redis<br>172.20.0.12]
                    init[Zammad Init<br>172.20.0.13]
                    rails[Rails Server<br>172.20.0.14]
                    scheduler[Scheduler<br>172.20.0.15]
                    websocket[Websocket<br>172.20.0.16]
                    nginx[Nginx<br>172.20.0.17<br>Port 8083:8080]
                end
            end
        end
    end
    
    %% Main Service Connections
    zserver --> ubuntu
    zserver --> nginx
    linkStyle 0,1 stroke:#000000
    
    %% Internal Zabbix Connections
    mysql --> zserver
    zserver --> zweb
    zserver --> zagent
    linkStyle 2,3,4 stroke:#000000
    
    %% Internal Zammad Connections
    postgres & elastic & redis --> rails
    rails --> nginx
    linkStyle 5,6,7,8 stroke:#000000
```


```mermaid
flowchart TD
    subgraph docker[Docker Network zabbix-net]
        subgraph zabbix[Zabbix Environment]
            mysql[MySQL Server<br>172.20.0.2]
            zserver[Zabbix Server<br>172.20.0.3:10051]
            zweb[Zabbix Web<br>172.20.0.4:8082]
            zagent[Zabbix Agent<br>172.20.0.5:10050]
        end

        subgraph monitored[Monitored System]
            ubuntu[Ubuntu Server<br>172.20.0.6:10055]
        end

        subgraph zammad[Zammad Environment]
            postgres[PostgreSQL<br>172.20.0.10]
            elastic[Elasticsearch<br>172.20.0.11]
            redis[Redis<br>172.20.0.12]
            zrails[Zammad Rails<br>172.20.0.14]
            zsched[Scheduler<br>172.20.0.15]
            zwebsock[Websocket<br>172.20.0.16]
            znginx[Nginx<br>172.20.0.17:8083]
        end

        %% Database connections
        mysql --> zserver
        postgres --> zrails
        elastic --> zrails
        redis --> zrails
        redis --> zwebsock

        %% Zabbix connections
        zserver --> zweb
        zagent --> zserver
        ubuntu --> zserver

        %% Zammad connections
        zrails --> znginx
        zwebsock --> znginx
        zsched --> zrails

        %% Integration flow
        zserver -->|Creates ticket on alert| zrails
    end

    classDef database fill:#000080,stroke:#fff,color:#fff
    classDef cache fill:#800000,stroke:#fff,color:#fff
    classDef search fill:#ff8c00,stroke:#000,color:#000
    classDef monitoring fill:#006400,stroke:#fff,color:#fff
    classDef application fill:#000066,stroke:#fff,color:#fff
    classDef server fill:#8b0000,stroke:#fff,color:#fff

    class mysql,postgres database
    class redis cache
    class elastic search
    class zserver,zagent,zweb monitoring
    class zrails,zsched,zwebsock,znginx application
    class ubuntu server
```