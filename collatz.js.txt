
const points = []

function getNumber(number) { 
 points.push(number)

 if(par(number)) {
 	number = number / 2
 } else {
 	number = (number * 3) + 1
 }
 
 if (number == 1) {
 	console.log('Finally..', points)
  console.log(`It was ${points.length} points`)
  
  return
 } else {
 	console.log('Number', number)
 	getNumber(number)
 }
}

function par(number) {
	return number%2==0
}


getNumber(27)