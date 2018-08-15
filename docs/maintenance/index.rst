Maintaining the website
=======================
Keeping the website up to date improves performance by fixing bugs.

Modules
-------

- Keep modules up to date. This fixes security issues and fixes bugs
- Reduce number of modules i.e. try to keep only key modules and remove those that perform a single task that can be done by a different design

Views
-----

- Views can give negative impact in your site performance because of complex join queries.
- Enable views caching on pages or blocks that don't need to be updated in real time.
- Simplify views e.g. by improving content type structures.
- Remove utf8_decode from data export because it significantly slows down exports.

Errors
------

- Resolve error logs. Pantheon provides developers direct access to numerous resources for debugging site execution problems, including slow site performance and PHP errors.
- Debugging sites with log files, including how to retrieve them → https://pantheon.io/docs/logs/ 
- Debugging slow performance → https://pantheon.io/docs/debug-slow-performance/ 
- PHP errors and exceptions → https://pantheon.io/docs/php-errors/ 
- Pantheon server errors and responses → https://pantheon.io/docs/errors-and-server-responses/ 
- New Relic → profiles and tracks application performance over time – https://pantheon.io/docs/new-relic-analysis/
- Perform site audit: https://pantheon.io/docs/drupal-launch-check/#troubleshooting

Database design
---------------
- Make sure all tables are in InnoDB format and not MyISAM: https://pantheon.io/docs/myisam-to-innodb/
- Keep PHP version up to date: https://www.pantheon.io/docs/php-versions/
- Database 4 byte UTF-8 support: https://www.drupal.org/node/2754539

.. toctree::
   :maxdepth: 1

   Drupal core updates <drupal-core>
   Pantheon updates <pantheon>
   Contributed modules updates review <contrib>
   Check views <views>
   Check rules <rules>
