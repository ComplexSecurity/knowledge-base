HTML encoding is a method used to convert characters into a format that can be safely transmitted or displayed in a web environment. This process is essential because certain characters have special meanings in HTML and might cause issues if used directly in HTML code.

[[HTML]] uses specific character sets like [[ASCII]] or [[Unicode]]. However, characters like "<", ">", and "&" have special meanings in HTML (as tags or entities). To display these characters as regular text, they must be encoded.

Special characters are encoded using character references. These references can take two forms:

- **Named Character References**: These are readable names that represent characters, like `&lt;` for the less-than sign ("<").
- **Numeric Character References**: These use a number to represent a character, like `&#60;` for the less-than sign.
