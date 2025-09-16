Phone number and email address extraction leverages **regular expressions (regex)**—formal patterns that match strings of text based on predefined rules.

***

### Phone Number Extraction Theory:

- **Regex Pattern Design**:  
  Phone numbers vary widely in format (country codes, area codes, separators like spaces, dashes, periods, parentheses, extensions). A robust regex covers:  
  - Optional country code (e.g., `+91`, `+1`)  
  - Optional area code (e.g., `(123)` or `123`)  
  - Main number split by spaces, dashes, or dots  
  - Optional extensions (e.g., `ext 1234`)

- **Pattern Components and Examples**:  
  - `\+?` — Optional plus for country code  
  - `\d{1,3}` — 1 to 3 digit country code  
  - `[-. (]*` — Optional separators  
  - `\d{3}` — Area code or prefix  
  - `\d{3}` and `\d{4}` — Local number segments  
  - Word boundary markers (`\b`) ensure accurate token matching.[1][4][5]

- **Finding Matches**:  
  The regex engine scans input text to find all substrings matching this pattern, extracting these substrings as phone numbers.

***

### Email Address Extraction Theory:

- Emails follow a general format: `username@domain.extension`. Regex components:  
  - Username: alphanumeric and some symbols like `.`, `_`, `%`, `+`, `-`  
  - Domain: alphanumeric and `.` separators  
  - Extension: 2 or more alphabet characters (like `.com`, `.org`)

- A typical regex describes this structure and matches email substrings in input text.

***

### Extraction Process Summary:

1. Define regex patterns for phone numbers and emails.  
2. Use programming language regex functions (e.g., Python’s `re.findall()`) to scan text and **extract all matches**.  
3. Matches can be collected, formatted, and utilized as needed (e.g., copied to clipboard, saved to files).


[7](https://ihateregex.io/expr/phone/)
[8](https://www.geeksforgeeks.org/dsa/validate-phone-numbers-with-country-code-extension-using-regular-expression/)
[9](https://codemia.io/knowledge-hub/path/how_to_validate_phone_numbers_using_regex)
