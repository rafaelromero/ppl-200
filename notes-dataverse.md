

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
Relationships: (1:*, *:1), *:* (many to many uses intersect table, examples: recipe <-> ingredients, books <-> authors)

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



















