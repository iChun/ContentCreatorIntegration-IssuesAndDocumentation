Read File Condition
============= 

## Description

Gets the lines of a file. Each line will be in variable `$<file_name>_<line>`, eg `$file_1`, `$file_2`. Total lines will be in `$<file_name>_count`, eg `$deathcounts.txt_count`. Fails if the file doesn't exist or there is an error reading the file.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `readFile`       |         Not seen in the Editor.        |
| *`fileName`* | String |      File Name. File must be in your profile directory.      |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
