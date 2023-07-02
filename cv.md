1.**Name** _Dmytro Yakushchenko_
2.**email:** _dmytro.iakushchenko@nure.ua_
**discord:** _Dmitry Yakushchenko_
3._I am second-year student of Kharkiv National University of Radioelectronics, I am studying on Computer Engineering and Control faculty. I am interested in coding and solving_ _various problems related to programming. I found interesting to find and correct different errors and create solutions for various tasks in my head. I like studying in university_ _because I find interesting communication with lecturer. It helps me to understand the subject, and lecturer is also glad to hear the quetions on the lecture._
_Also I studied javascript before by myself, but I want to improve my skills in this programming language and build a career later._
4.Skills
MySQL
C++
VHDL
Javascript

5.Example of javascript code:
```let salaries = {
Manager: { 
	salary: 35000,  // salary after tax; should be integer; min: 100, max: 100000
	tax: "25%" // 'tax' is integer; min: "0%", max: "99%"
},
Builder: {
	salary: 50000, 
	tax: "30%"
}
};

let team = [
{
	name: "Adrew", 
	specialization: "Manager" 
},
{
	name: "Helena",
	specialization: "Builder"
},
{
	name: "Markus",
	specialization: "Builder"
},
{
	name: "Harry",
	specialization: "Trader"
},
];




function calculateTeamFinanceReport(salaries, team) {

let specs = Object.keys(salaries);
let result = {
	errorMessage: "",
	data: null,
	isSuccess: false,
};
if (team.length > 100 || team.length < 1)
  	{
  	result.errorMessage = "The team is out of the given range";
  	return result;
  	}

if (specs.length > 10 || specs.length < 1)
	{
  	result.errorMessage = "The specializations are out of the given range";
  	return result;
  	}

for (let i = 0; i < specs.length; i++) {
	  
	  let parsedSal = salaries[specs[i]].salary;
	  if (isNaN(parsedSal) || parsedSal > 100000 || parsedSal < 100)
	    {
	    	result.errorMessage = "The " + specs[i] + "'s salary is out of the given range";
	    	break;
	    }
	  let parsedTax = +salaries[specs[i]].tax.replace("%", "");
	  if (
	  	isNaN(parsedTax) ||
	    parsedTax < 0 ||
	    parsedTax > 99
	  )
	  {
	  	result.errorMessage = "The " + specs[i] + "'s tax is out of the given range";
	  	break;
	  }
}
if(result.errorMessage.length > 0) return result;

function calculateSpecializationFinance(a) {
  return Math.round(
    (salaries[specs[a]].salary * 100) /
      (100 - +salaries[specs[a]].tax.replace("%", ""))
  );
}

function countSpecializationMembers(a) {
	let b=0;
	for(let i=0;i<team.length;i++) {
		if(team[i].specialization===a) b++;
	}
	return b;
}

let obj = {
  totalBudgetTeam: null,
};
for (let i = 0; i < specs.length; i++) {
  obj["totalBudget" + specs[i]] =
    calculateSpecializationFinance(i) *
    countSpecializationMembers(specs[i]);
  obj.totalBudgetTeam += obj["totalBudget" + specs[i]];
}
result.isSuccess = true;
result.data = obj;
return result; // If you need only the object with totalBudget, use return result.data
}

console.log(calculateTeamFinanceReport(salaries, team));
```
I have completed English courses at B2 level in Poland, and have a certificate to confirm it.