This repo contains all files required to run through a demonstration of the Flyway Community pipeline.

To run you will require 2/3 Azure SQL Databases for Dev (Optional), CI and Prod, I went with:

- DMDatabase_Dev (Optional)
- DMDatabase_CI
- DMDatabase_Production

You will also need the variables for your pipeline:

ciJDBC: "jdbc:sqlserver://[yourserver].database.windows.net:1433;database=[yourcidatabase]"
prodJDBC: "jdbc:sqlserver://[yourserver].database.windows.net:1433;database=[yourproddatabase]"
FLYWAY_BUILDTESTPATH: $(Build.Repository.LocalPath)/migrations
FLYWAY_SCRIPTS: $(Build.Repository.LocalPath)/migrations/Scripts
userName: [yoursqlauthusername]
password: [yoursqlauthpassword]
