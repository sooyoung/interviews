# Exercise 2

Now we will implement row-level security (RLS) and role-based access control (RBAC). The goal is to define several types of roles for different user groups.

ROLES

- super_admin
- admin
- regular

POLICIES

- update, insert, select, delete on all tables + rows for super_admin role
- update, insert, select on all tables + rows for admin role
- update on Employees table where employee id = authenticated user for regular role
- anonymous users cannot access any tables


References

- https://www.youtube.com/watch?v=kwoKmi6inAw&t=0s
- 
