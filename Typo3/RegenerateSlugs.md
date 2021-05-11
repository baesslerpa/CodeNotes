# 1. Remove all Slugs

Entfernt alle bereits generierten Slugs aus der Datenbank

```sql
UPDATE `pages` SET `slug` = NULL where 1
````

# 2. Regenerate

Upgrade > Run Upgrade Wizard > ** Introduce URL parts ("slugs") to all existing pages **