// save the exercise file as exercise.js so the script below works
<br>
// run the below script in browser(preferrably IE10+)
<br>
// script below calls up the exercise source file and runs 8 markuptester() tests on various input possibilites
<br>
// markupstester function itself is already present in exercise.js, no need to load up jasmine
<br>
<!DOCTYPE HTML> 
	<html> 
	<head> 
	<title>Nulogy Exercise</title> 
	</head> 
	 <body> 
	 <script src="exercise.js" type="text/javascript">
	 </script>
	 <script>
	 		
		markuptester(markupcalc("$1299.99", "3 people", "food"), "$1591.58", 1, "testing 1st given example");

	</script>
	<br>
	 <script>
		
		markuptester(markupcalc("$5432.00", "1 person", "drugs"), "$6199.81", 2, "testing 2nd given example");
	</script>
	<br>
	 <script>
		
		markuptester(markupcalc("$12456.95", "4 people", "books"), "$13707.63", 3, "testing 3rd given example");
	</script>
	<br>
	
	 <script>
		
		markuptester(markupcalc("$555", "39 people", "Pharma"), "$899.18", 4, "testing 39 people, Pharma, $555");
	</script>
	<br>

	 <script>
		
		markuptester(markupcalc("$555", "39 people", "parma"), "$855.48", 5, "testing 39 people, parma-counts as other category, $555");
	</script>
	<br>
	
	 <script>
		
		markuptester(markupcalc("$555", "39 people", "other"), "$855.48", 6, "testing 39 people, other category, $555");
	</script>
	<br>
	 <script>
		
		markuptester(markupcalc("555", "39 people", "other"), "$84.78", 7, "testing 39 people, other category, 555--wrong input on first variable");
	</script>
	<br>
	 <script>
		
		markuptester(markupcalc("$555", "39", "other"), "$855.48", 8, "testing 39-without people-still correct but unexpected second variable format, other category, $555");
	
	</script>
	<br>
	 <h1> Tests completed </h1> 
	<br>
	
	
	 </body> 
	</html> 
