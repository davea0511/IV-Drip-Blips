# IV-Drip-Blips
Mobile App that does simple conversion plus audio and visual output demonstrating an intravenous drip-rate to save lives

# SPECIAL NOTE ABOUT BEING SAFETY-MINDED WHEN USING THIS CODE
The intent of this app is to reduce hospital mistakes (see "PURPOSE" below), and thereby save lives.  It is offered under the MIT license in order to encourage wide use of this code *HOWEVER* there are specific safety reasons for designing it the PROGRAM FLOW (see below) in a way that might seem inefficient (for example, by not having a default drips/ml rate). So, PLEASE DO NOT change the core methodology (see PROGRAM FLOW below) that might open the door for more hospital errors.  Please be cognizant about how any change you make might result in more hospital errors, thereby reducing the original purpose of this code.

# PURPOSE
Worth a read: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3228265/
* Intravenous administration error rates are currently at 69.7%. That means
     that 2 out of every 3 someone gets an IV, something was wrong.
* "Wrong rate was the most frequent and accounted for 95 of 101 serious errors."
* "Serious error" were defined as:
   * Incident is likely to lead to permanent reduction in bodily functioning leading
        to, for example, increased length of stay; surgical intervention
   * Incident is likely to lead to a major permanent loss of function
   * Incident is likely to lead to death

**In short, the purpose of this app is to save lives.**

# PROGRAM FLOW
1. The nurse enters the desired rate in ml/hr.
    - In order to reduce the chance for mistakes (which is paramount, and the purpose of this app)
          there are *no* other units of measure allowed for input.
    - Since ml/hr is the most commonly used, that is the only unit of measure that is allowed.
2. The nurse is required to select the drips/ml (also called gtt/ml), from a list.
    - Again in order to reduce the chance for mistakes, the most clear and obvious units of measure
              are drips/ml, not gtt/ml, so drips/ml will be used.  Medical-speak egos be damned.
    - The units of gtt/ml are also indicated in parenthesis, as this is more likely to be
                     indicated on the infusion set, prompting the user to quickly identify the proper rate.
                     eg. **"Please select the infusion set drips/ml (gtt/ml):"**
    - The list shoule include: 10, 15, 20, and 60.  For safety purposes there will not
              be a default setting, and the user must select one in order to proceed.
    - Since indicating a
              default (or preferred value) might introduce error, the app does not indicate a default,
              or preferred, or most commonly used value.
3) The nurse must validate that they selected the right infusion set (step 2), as a safety measure, with a message  
    **"Are you sure? Mismatcing the infusion set can result in the wrong rate and can have serious, even fatal, consequences"**
4) The entered ml/hr rate is converted to drips per second, which rate will be shown on the screen.
5) A large portion of the screen will visually demonstrate the drip rate with a continuous visual pulse animation until stopped.
6) The user will have to option to also hear an audible signal for each drip, which is normally silenced.
