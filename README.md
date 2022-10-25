# SQL-Murder-Mystery
SQL Project found online designed to test experienced users ability of SQL.


-- Query used to find the crime scene report. 
/*
SELECT
	*
FROM
	crime_scene_report
WHERE
	date = 20180115
	AND
	city = 'SQL City'
	AND 
	type = 'murder'
*/

--  Query used to find witness 1
/*
SELECT
	*
FROM
	person
WHERE
	address_street_name = 'Northwestern Dr'
ORDER BY
	address_number DESC
*/

-- Query used to find witness 2
/*
SELECT
	*
FROM
	person
WHERE
	address_street_name = 'Franklin Ave'
	AND
	name LIKE 'Annabel %'
*/

-- Query used to find both witnesses testimony
/*
SELECT
	*
FROM
	interview
WHERE
	person_id = 16371 OR person_id = 14887
*/
	 
--Query used to investigate id 14887's testimony
/*
SELECT
	*
FROM
	get_fit_now_member
WHERE
	id LIKE '48Z%'
	AND membership_status = 'gold'
*/
-- Query used to incorpate id 16371's testimony. (Useless query)
/*
SELECT
	*
FROM
	get_fit_now_check_in
WHERE
	membership_id = '48Z7A' OR membership_id = '48Z55'
	AND check_in_date = 20180109
*/
-- Query used to pull license ID for easier identification
/*
SELECT
	name, id, license_id
FROM
	person
WHERE
	name = 'Joe Germuska' OR name = 'Jeremy Bowers'
*/
-- Query used to determine who had plate number that included H42W
/*
SELECT
	*
FROM
	drivers_license
WHERE
	plate_number LIKE '%H42W%'
	AND id = 423327 OR id = 173289
*/
-- The person who committed the murder was Jeremy Bowers
