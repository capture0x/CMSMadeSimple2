# Exploit Title: CMS Made Simple Version: 2.2.19 - SSTI
## Date: 2024-21-02
## Exploit Author: tmrswrr
## Vendor Homepage: https://www.cmsmadesimple.org/
## Version: 2.2.19
## Tested on: https://www.softaculous.com/demos/CMS_Made_Simple

## Description
This exploit targets CMS Made Simple version 2.2.19 and demonstrates a Server-Side Template Injection (SSTI) vulnerability.

## Steps to Reproduce:
1. Log in as admin and navigate to Layout > Design Manager > Breadcrumbs.
2. Click edit and insert the following SSTI payloads: `{7*7}`, `{$smarty.version}`, `{{7*7}}`.
3. Click Apply, then Submit.
4. Visit the home page: `https://127.0.0.1/CMS_Made_Simple/index.php?page=templates-and-stylesheets`.
5. Observe the result: `49 class="breadcrumbs"`.

## Notes:
- This exploit confirms the presence of SSTI vulnerability in CMS Made Simple 2.2.19.
- The payloads are utilized to evaluate expressions and verify the SSTI.
- Use responsibly and with proper authorization; unauthorized use of this exploit may lead to legal consequences.
