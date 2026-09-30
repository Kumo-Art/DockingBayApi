//--------------PilotsController Bugs-----------------//

Syntax Error,on line 13, needed a s on the end of Pilots in PilotsController, I added an s to fix the error




//----------------ShipService Bugs-----------//

syntax error on line 10, there was a comma missing after "Iron Comet", I added the comma.

Logic error on line 54, refuel was add 100 to ship.FuelPercent due to += EX. ship.FuelPercent += 100;, I removed the plus sign so that it is just equals 100.






//--------------ShipsController Bugs-------------//

Syntax error on line 32, there was a closing bracket missing at the end of [HttpGet("{id}")], I added the bracket at the end

Logic error on line 37, if statement was if(ship != null) when it should have been if(ship == null), I removed the ! and added another = sign.

Logic error on line 49, return type was Ok, when it should have been CreatedAtAction, I changed it to match that

Logic error on line 74, HttpDelete if statement was if(!deleted) and was giving internal server error, changed if statement to if(deleted == false)



//-------------Ship Model Bugs--------------//

Syntax error on line 6, there was a semicolon missing at the end of string.Empty








//---------------IPilotService Bugs------------//

Syntax error on line 9, the l in List should be uppercase, I changed it to be uppercase




//--------------------PilotServices Bugs--------------//

Logic error on line 40, created pilot was setting hours to zero, commented out pilot.FlightHours = 0;

Runtime error on line 50, needed an if statement to check if null, added
if(pilot == null)
{
    
    return false;
}




//---------------------Program.cs Bugs------------------//

Runtime error on line 8, needs an AddScoped for IPilotServices and PilotServices, Changed it to reflect that




### Reflection

Answer each in 2–3 sentences at the bottom of your bug log.

1. Which bug took you the longest to find? What finally led you to it? 
- **probably the runtime errors, especially the 2 i didn't find**
 
2. Pick one runtime error. What exception did it throw, and how did the message help you find the line? 
- **The AddScoped runtime error, i don't remember the exact wording of the error but, i did go and check the program.cs file to make sure it was good**

3. DELETE /api/ships/3 crashed with Collection was modified . Why can't a foreach loop keep
going after you remove something from the list it's looping over? - **Because the number of ships changes after one is removed**

4. Every /api/pilots request crashed until you fixed one line in Program.cs . What was dependency
injection trying to do, and why did it fail? - **It was implementing IShipService and ShipService twice**

5. Several logic bugs were one character, like != versus == or < versus <= . Why doesn't the compiler
catch those? - **Because they are logic errors not runtime or syntax error**

6. Some bugs hid until you fixed a different one. Give one example.-**I Can't think of one, maybe its one of the errors i didn't find**