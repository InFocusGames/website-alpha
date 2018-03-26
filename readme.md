#Server Notes

Indizr is served using a two-machine setup, one running Nginx and one running a series of Node mini-apps that are, in effect, microservices. (They're not containerized yet, but we'll handle that in a subsequent project.

A rough schematic of the architecture...

                                        ----------------------------------
Archie1 Server (Nginx)                  |  API Gateway: Handles HTTPS     |
                                        |  requests from users & reverse- |
                                        |  proxies to Node apps as needed.|
                                        -----------------------------------
                                          /         |           |      \       
                                         /          |           |       \      
                                        /           |           |        \   
Archie2 Server (Node)             knight(80)  site(8080)   posts(1229)   river(1337)   




Editor app should run natively via the site. We shall see...
