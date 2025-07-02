environment types: sandbox, developer, trial and production
developer environment: does not support dataflows, 750 flow runs per month, 2gb size
environment conversion paths: sandbox -> production
environnent operations:
change environment type: (prod -> sandbox), (sandbox -> prod), (trial -> prod)
reset environment: you cannot reset a production environment!
copy environment: everything or customizations and schema only, must be in same tenant and region,cannot copy to production environment, only solution aware components, cannot copy to and from a trialto a default environment
backups: automatically (7 day retention (for non dynamics apps environments)), can be changed with powershell to 7,14,21 or 28 days, trial environments are not backed up
manual - backed up on updates of environment, production and sandbox can be backed up, developer environments can be backed up, default cannot be backed up
restore environment: to restore a production environment, you must first change its type to sandbox
administration mode: supported by sandbox, production and trial

database creation reserves up to 1gb
dataverse storage capacity types: database, file and log
default capacity: 3gb database, 3gb file and 1gb log
storage capacity extensions are available - lasts 30 days, can extend up to 3 times.

types of tables: standard, custom, virtual, elastic (for millions of rows -> cosmos db)
Auditing enablement levels: environment, table, column
Relationships: (1:_, _:1), _:_ (many to many uses intersect table, examples: recipe <-> ingredients, books <-> authors)

Dual write: two way sync - CRUD operations
Virtual tables: external data - CRUD operations

columns-suppoted-types: plain-text/text (single-line 4k characters max), text-area (4k characters), multiple lines of text (supports more than 4k characters), rich-text, email, phone-number, ticker-symbol, url
multi-lines of text: max length of 1,048,576 . default is 2k.
Number-types: none(default), duration, time-zone, language code.
Number ranges: -2,147,483,648 to +2,147,483,647 .
Number ranges (BIG): -100,000,000,000 to +100,000,000,000
Float: floating point with up to 5 decimal points
float ranges: 0 to +1,000,000,000
language code: whole number,
duration: whole number for minutes
currency: currency (numeric), currency(Base) read-only, lookup of currency, exchange rate (decimal column that provides the exchange rate used for the selected currency)
file-types: file (default is 32 mb), max is 131 mb), image displays a single image for each record in app, default size is 10240 kb, max is 30,720kb

ways to import data: admin center import wizard, model driven apps import, power apps maker porta import, data-flows.

admin center import wizard: supports only 10-20 records at a time, supports csv, txt, xml, excel and zip (with file in it), maps choices with label
model driven app: csv, xml, excel, maps choices with label for Excel.
maker portal data import: csv, excel, only simple column mapping only
dataflows: clean and transform data, does not support mapping of lookup columns
export data in model driven apps: can export up to 100k at a time.
export data in maker portal: exports a zip with a csv in it.
export data with power automate
export data with azure snapse link

---

Permissions

3 types of environments - development, test, production
dataverse table actions: create, read, write, delete, append, append to, assign, share

business units: user can be assigned to one bu, a default team is assocated with each bu
teams: you cannot add or remove members from the default team
types of teams: owning teams and access teams
dataverse tables have a matrix of permissions based on privelages and access levels
dataverse table permissiona are same as table actions above
dataverse table access levels: parent-child, organization, user, business unit, none
dataverse privelages and access levels make up role based access control (RBAC) in dataaverse
types of hieararchy security models: manager and postion hierarchy
manager hierarchy is based on the management chain or direct reporting structure
manager can have full access to direct reports
manager has read-only for non directy reports
position hierarchy allows you to define various positions in the organization and arrange the hierarchy by using the Position table
both models require atleast read-only access to the table being used in a hierarchy approach
performance tips: keep hierarchy to 50 users or less, use depth to reduce read only level access, create minimum number of business units
datavesre supports two types of record ownership: organization owned and user or team owned.
user and team-owned records access levels: organizational, business unit, business unit and child, only the users own records
dataverse record should be used an exception, since security models are not always fully implemented environment wide when used
dataverse record sharing with teams is more efficient, access teams is another more advanced option that auto creates the team and share record access.

---

views
types of views: System (quick find, advanced find, associated, lookup), public, personnel
user can save their own view
single column sort by selecting column in view which will lead to saving a personnel view
sort view: can only sort on columns in view

---

## templates

ways to create word teplates: advanced settings (by admins and system customizers), from a specific record (main form) or list(view) as personal views

anyone can create personnel templates
you may need to refersh an excel template if the pivot table shows outdated information
you must select a record in order to use word templates

model driven app export options: open in excel online, static worksheet, static worksheet (page only), dyanmic worksheet
, dynamic pivot table
100k is max row limit on static worksheets , unless the page only version of static worksheet is selected
edit in exel is also an option, but you need to have the excel power apps add in installed

-------------------
## dataverse and azure tools
----------------------
dataverse can be linked with Azure synapse analytics for full sql, big data apache spark engin, scalable, similar to data factory integrations, continous replication, transformation layer, big data analytics
list of tables to use is defined in the power portal link definition

xrmtoolbox - can be used for configuration, documentatino, migration and reporting

https://www.xrmtoolbox.com/

