Workarea Upgrade
================================================================================

Workarea Upgrade makes it easier to upgrade your application to use newer
versions of Workarea and Workarea plugins. Use this plugin to:

* View a report to help you determine the effort required to upgrade.
* Migrate your database.
* Diff any two Workarea versions (back to version 0.8.0) and filter the
results to show only the changes affecting your application.
* View lists of files added and removed between versions of Workarea.


Step 1: Install the Plugin
--------------------------------------------------------------------------------

Add the plugin to your application's Gemfile:

    gem 'workarea-upgrade', source: 'https://gems.weblinc.com', group: 'development'

Update your bundle. Use `bundle update` to get the latest version:

    cd path/to/your_app
    bundle update workarea-upgrade


Step 2: View Help
--------------------------------------------------------------------------------

Run `workarea_upgrade` without arguments to view help:

    cd path/to/your_app
    bundle exec weblinc_upgrade

Use `help` to get detailed help for a specific command:

    cd path/to/your_app
    bundle exec weblinc_upgrade help report

Step 3: Install Target Gems
--------------------------------------------------------------------------------

Install each Gem that you will be upgrading to.
gem install example-gem -v UPGRADE_VERSION

Step 4: View Report & Begin Upgrade
--------------------------------------------------------------------------------

Start by viewing an upgrade report. The report will summarize the work required
to upgrade to specific versions of Workarea and Workarea plugins.

The report will suggest next steps for your upgrade.


Step 5: Migrate Your Database
--------------------------------------------------------------------------------

If upgrading to a major or minor version of Workarea, a database migration may
be available.

First, update your bundle to use the newer version of Workarea and use the tools
described above to help achieve compatibility with the newer version.

Then run the database migration:

    cd path/to/your_app
    bin/rake workarea:upgrade:migrate

[See more information on migrating from version 2 to 3](v3_database_migration.md)

Copyright & Licensing
--------------------------------------------------------------------------------

Copyright Weblinc 2017. All rights reserved.

For licensing, contact sales@workarea.com.
