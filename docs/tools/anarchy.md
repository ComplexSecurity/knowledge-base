"Username Anarchy" is a tool designed for generating username lists for use in penetration testing, particularly in situations where usernames need to be guessed, such as during [brute-force](../security/brute.md) login attempts. The tool generates usernames based on a set of rules and patterns that mimic common username conventions in various organizations and systems.

Given a list of full names, Username Anarchy can generate potential usernames by applying common username schemas, like using the first letter of the first name combined with the last name (e.g., `jdoe` for John Doe). It can create variations by including initials, numbers, or common separators (like dots or underscores).

Users can customize the generation process to align with specific username patterns they expect in the target environment.

Suppose you have a list of employee names from a company, and you want to generate possible usernames for a penetration testing exercise. The list might include names like:

- Jane Smith
- John Doe
- Emily Johnson

You would use Username Anarchy to process this list and generate a range of potential usernames. For example:

```bash
username_anarchy -n "Jane Smith John Doe Emily Johnson"
```

This might result in the following:

```bash
jsmith
jdoe
ejohnson
janes
john.doe
emilyj
smithj
doej
johnsone
```
