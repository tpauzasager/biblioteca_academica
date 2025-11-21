```bash
//Replace all <filter_word> contained in <file_name> 
awk '/<filter_word>/ {print "<replacement_text>"}' <file_name>

```