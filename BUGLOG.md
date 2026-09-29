//--------------PilotsController Bugs-----------------//

Syntax Error,on line 13, needed a s on the end of Pilots in PilotsController, I added an s to fix the error




//----------------ShipService Bugs-----------//

syntax error on line 10, there was a comma missing after "Iron Comet", I added the comma.

Logic error on line 54, refuel was add 100 to ship.FuelPercent due to += EX. ship.FuelPercent += 100;, I removed the plus sign so that it is just equals 100.






//--------------ShipsController Bugs-------------//

Syntax error on line 32, there was a closing bracket missing at the end of [HttpGet("{id}")], I added the bracket at the end

Logic error on line 37, if statement was if(ship != null) when it should have been if(ship == null), I removed the ! and added another = sign.

Logic error on line 49, return type was Ok, when it should have been CreatedAtAction, I changed it to match that



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