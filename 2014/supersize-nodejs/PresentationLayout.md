Introduction [GB]

    M&E Cloud Services Context
    Deployment Goals
       - Easy deployment (Sync and run script)
       - Deployment as code (Sync branch and deploy) (Source Control)
       - Small pieces to build something big
       - "Developer-centric" environment
       - Developement is deployment agnostic

Architecture [GB]

    Architecture Oversight
        - Scalable Nodes
        - Dynamic Layouting of Roles (Decouple dev from deployment, save cash)
    How Node.js tinted the architecture
        - Node.js encourage development of small services
    Amazon

Deployment (Architecture as base thread) [DR]

    Deployment as code
    Cloud Formation
    Publish
        Git
        Node.js Modules
        Decoupling from npm registry
    Provisioning
        Roles and Chef
        Rebuild (native modules)
        Upstart
        Chronology Diagram (Step by Step)
    Vagrant?
        - Cookbook testing

From Development to Production [DR]

    Stack Family
        Route53
            - DNSing
            - Low delay end-point switching
            - Alias
        Data Migration
            - From family to family
            - Data conversion
    Stack Monitoring
        Sysadmin Portal
            - Monitor Page
            - Logs
            - Tracing
    Stack Diagnostic and Debugging
        Back door
            - VPC
            - IP Filtering
            - SSH port
        Stack Scripts
            - Tunneling to any instance
            - Tunneling to MongoDB (Robomongo)
            - Remote debugging

M&E Cloud Services - The Bad Parts [GB]

    Chef Server
    Mustache
        - We identified the right problem; wrong solution
        - Troposphere?
    Private npm registry
        - We still dream of it; not there yet
        - Git protocol for node modules works, but it is slow
        - Middleground solution with npm lazy, workspace
   
M&E Cloud Services - The Good Parts [GB]

    nconf
    Deployment from day 1
    Put a lot of effort on development/deployment tools
    Local deployment
        - Vagrant
        - Cross platform technology
        - "Full" Java Script stack