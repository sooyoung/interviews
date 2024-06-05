# Exercise 1 Instructions

1. View the supplied dbml file to view the starting database schema in a tool like https://dbdiagram.io
2. Create this schema in [Supabase](https://supabase.com/dashboard/org/wjomoigtnqntixpaieak/general) using the free tier
3. Implement Supabase Auth by linking the Employees table to Supabase's auth.users table. See the code snippet below for sample usage.


```
create function handle_new_user() 
returns trigger as $$
begin
  insert into profiles (id) values (new.id);
  return new;
end;
$$ language plpgsql;

create trigger on_auth_user_created
after insert on auth.users
for each row execute function handle_new_user();
```

4. Create mock data to insert data into all four tables using ChatGPT or Mockaroo.com

   
