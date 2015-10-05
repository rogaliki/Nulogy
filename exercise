function markupcalc(base_price, num_people, category){
	//below we cut out the dollar sign from the base_price so we can turn it into a float
	var base_pricenodollar=base_price.substring(1);
	//below we turn this new string without the dollar sign into a float to 2 decimal places
	var base_pricefloat=parseFloat(base_pricenodollar,2);
	//below we calculate the flat markup as 5% on top of the base price floated to 2 decimal spots
	var flat_mark = base_pricefloat*1.05;
	//below we find the index of the first "p" inside the second input variable since both people and person start with "p"
	var pos_of_p_min2 = num_people.indexOf('p')-1;
	//now cut the string to a space before this and change to integer.  If "people/person" is ommitted, treat input still as correct
	var people;
	if (pos_of_p_min2>=0)
		people=num_people.substring(0,pos_of_p_min2);
	else
		people=num_people;
	//below we turn the leftover which is now just a number into a decimal base integer
	var num_peoples=parseInt(people,10);
	//below we calculate the people markup on top of the previously calculated flat 5% markup
	var people_mark = flat_mark * num_peoples* 0.012;
	//below we calculate the category markup, with allowance for different spelling of and usage of pharma/drugs/pharmaceutical/pharmaceuticals
	var type_mark=1;
	var category_uppercase=category.toUpperCase();
	if (category_uppercase =="FOOD")
		type_mark*=0.13;
	else if(category_uppercase =="ELECTRONICS")
		type_mark*=0.02;
	else if (category_uppercase == "DRUGS" || category_uppercase ==  "PHARMA" || category_uppercase == "PHARMACEUTICALS" || category_uppercase == "PHARMACEUTICAL")
		type_mark*=0.075;
	else type_mark=0;
	type_mark*=flat_mark;
	//below we calculate the total markup, still as a float
	var total = flat_mark+people_mark+type_mark;
	//below we round the resulting float to two decimal places and convert it to a string
	var total2=total.toFixed(2);
	var strtotal=total2.toString();
	//below we append the dollar sign to the front of the string to get ready for output return
	var dol="$";
	final_ret=dol+strtotal;
	// we finally return the dollar value of the final price with markup included
	return final_ret;
}


//below is a tester function that takes the markupcalc function with inputs as the first variable, expected result as second value, test number-trivial, and description of what the test does from the html script in the README file
function markuptester(value, expected_result, test_num, test_desc){
	//test_desc is a description of what the test is testing
	if (value==expected_result)
		document.write("test " + test_num + " passed... calculated value is: "+value+", expected value was: " +expected_result+".  This test was "+test_desc);
	else
		document.write("test " + test_num + " failed... calculated value is: "+value+", expected value was: " +expected_result+".  This test was "+test_desc);
	
}
