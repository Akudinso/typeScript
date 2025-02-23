# typeScript


Changes made to filterPersons:

- Restricted personType to 'user' | 'admin': Initially PersonType was generally a string allowing invalid values. Now it accepts 'user' | 'admin' explicitly preventing incorrect usage.
- Made criteria type-specific and excluded type Field: The old version used unknown, meaning any property could be passed. This esures filtering is only based on valid properties without allowing filtering type
- Ensured proper return type: The onld function returned unknown[], making it unclear whether it returned users or admin. Now, it dynamically returns User[] when personType is 'User' and 'Admin[]' when 'admin', ensuring typed results.