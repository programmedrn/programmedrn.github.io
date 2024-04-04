---
title: "Some Useful Queries for Postgresql"
categories: 
    - Postgresql
    - Postgres
    - sql
    - query
    - examples
excerpt: |
    Example queries for querying roles and accounts
feature_text: |
    ## Some Useful Queries for Postgresql
     Example queries for querying roles and accounts
feature_image: "/FirstBlog/assets/insertedImg/2024-04-04-postgresql-useful-queries/2024-04-04-09-17-32.png"
# aside: true
# heads: true
---

## Goal
Leaving some useful queries to control roles and accounts within postgresql.

### Queries
```sql
-- Whether an account holds a password or not
select * from pg_shadow
         where usename ilike '%smcp%';

-- Change password for an account
-- alter user @@@ with password '@@@@';
-- alter user smcp with password 'smcp';

-- Show roles
select rolname, rolsuper, rolcanlogin from pg_roles;

-- Show roles for each accounts
SELECT
    pg_user.usename AS username,
    pg_roles.rolname AS role,
    pg_roles.*
FROM
    pg_user
LEFT JOIN
    pg_auth_members ON pg_user.usesysid = pg_auth_members.member
LEFT JOIN
    pg_roles ON pg_auth_members.roleid = pg_roles.oid
WHERE
    pg_user.usename ilike '%smcp%';
-- SELECT
--     rolname,
--     rolsuper,
--     rolcreaterole,
--     rolcreatedb,
--     rolcanlogin,
--     CASE WHEN rolcanlogin THEN 'Can login' ELSE 'Cannot login' END AS login_permission,
--     CASE WHEN rolsuper THEN 'Superuser (can perform DDL and DML)' ELSE '' END AS ddl_dml_permission,
--     CASE WHEN rolcreaterole THEN 'Can create roles' ELSE '' END AS create_role_permission,
--     CASE WHEN rolcreatedb THEN 'Can create databases' ELSE '' END AS create_db_permission
-- FROM
--     pg_roles;


-- Change the name of an account
-- alter user @@@@ rename to @@@@;

-- Change options for an account
-- alter user @@@@ with option ...;

-- Delete an account
-- DROP USER [user_name];
```


## References
- [linkName](URL "tooltip")