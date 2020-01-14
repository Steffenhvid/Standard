# Conventions

## Database Conventions
### Prefixes
* Tables: None
* Stored Procedures: p_
* Views: v_
* All objects that are not tables, should have a header in the following structure:
		
		/** 
		ProcedureName: <p_name>
		Parameters: <param1 datatype>, <param2 datatype> ... (i.e @input NVARCHAR(4))
		Returns: <returns>
		Author: <author>
		Description: <description>
		Changelog: 	
					<date>, <changes>
					<date>, <changes>
					...
		**/
	This is used for automatic documentation

* All objects be backed up in:
	* Database\StoredProcedures
	* Database\Views
	* ...
* Install and update scripts should be placed in
	* Database\install.sql
	* Database\updates\update_<year>_<month>_<RunningVersion>.sql (i.e Update_2020_01_1.sql)