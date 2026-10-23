# UCLA Departments

A JSON list of UCLA Departments. Since 2026-10 it is generated from the UCLA General Catalog department list (<https://catalog.registrar.ucla.edu/>, retrieved 2026-10-23), plus names that appear only in the original 2021 list derived from <https://grad.ucla.edu/>. This is used to soruce a select field in the Library's LibCAl instance for registration forms. The goal is to standardize the Department terms in event planning and reporting.

Corrections, additions and de-dpulications appreciated. 


## How to use in libcal

1. Go to <https://calendar.library.ucla.edu/cal_reg_forms.php>
1. Edit or create your registration form
1. Add a question and choose **Remote data source drop-down** selection type
2. Copy and past the raw `departments.json` url <https://raw.githubusercontent.com/ucla-data-science-center/ucla-departments/master/departments.json> into the **Data url** field
2. Add a title and save. 
1. You can live preview your work  on the right. 


## Files

- `departments.json`: the dropdown list (flat array of names).
- `departments-aliases.json`: old or variant spellings mapped to the name used in `departments.json` (for example `"Classics Department"` to `"Classics"`). Use it to clean historical registration data. It does not apply to names from the 2021 list that have no catalog match.

## Changes in the 2026 refresh

- Names follow the General Catalog spelling ("and", not "&").
- Duplicates and program variants from the 2021 list ("Statistics - Master of Applied Statistics", "Economics Department") are folded into one name and recorded in the aliases file.
- Entries that are not in the current catalog (for example "Library") are kept so existing forms keep working.
- This is a department list, not a Humanities Division list. Classifying units by division is done elsewhere.
