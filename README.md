# IV-Drip-Blips
Mobile App that does simple conversion plus audio and visual output demonstrating an intravenous drip-rate to save lives

# SPECIAL NOTE ABOUT BEING SAFETY-MINDED WHEN USING THIS CODE
The intent of this app is to reduce hospital mistakes (see "PURPOSE" below), and thereby save lives, and provide a way to make sure the person setting up the IV is avoiding errors.  It is offered under the MIT license to encourage open use of this code *HOWEVER* there are specific safety reasons for designing it in a way that some people might consider inefficient (for example, not having a default drips/ml rate) so PLEASE DO NOT change the core methodology (see METHOD below) that might open the door for possible error.  Please include this in your own app, but please be cognizant about how each change you make could allow greater error, and thereby reduce error opportunities as much as humanly possible.

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

In short, the purpose of this app is to save lives.

# METHODOLOGY
(1) The nurse enters the desired rate in ml/hr.

    Note: In order to reduce the chance for mistakes (which is paramount, and the purpose of this app)
          there are *no* other units of measure allowed for input.
          Since ml/hr is the most commonly used, that is the only unit of measure that is allowed.

(2) The nurse is required to select the drips/ml (also called gtt/ml), from a list.

    Notes: a. Again in order to reduce the chance for mistakes, the most clear and obvious units of measure
              are drips/ml, not gtt/ml, so drips/ml will be used.  Medical-speak egos be damned.
                  - the units of gtt/ml are also indicated in parenthesis, as this is more likely to be
                     indicated on the infusion set, prompting the user to quickly identify the proper rate.
                     eg. "Please select the infusion set drips/ml (gtt/ml):"
           b. The list shoule include: 10, 15, 20, and 60.  For safety purposes there will not
              be a default setting, and the user must select one in order to proceed.  Since indicating a
              default (or preferred value) might introduce error, the app does not indicate a default,
              or preferred, or most commonly used value.
(3) The nurse must validate that they selected the right infusion set (step 2), as a safety measure, with a message
     "Selecting the wrong infusion set can result in the wrong rate and can have serious, even fatal, consequences"     
(4) The entered ml/hr rate is converted to drips per second, which rate will be shown on the screen.
(5) A large portion of the screen will visually demonstrate the drip rate with a continuous visual pulse signal until stopped.
(6) The user will have to option to also hear an audible signal for each drip, which is normally silenced.
