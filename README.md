# BioPharmSoft R Style Guide


This project is the begining of the development of style guide for R from the Biopharamaceutical Sotware Working Group (http://biopharmnet.com/biopharmsoft/).  

This file will all be used to collect quesiton (at least for now).

A couple question I have and if you have a preference let me know.  Saying “Either is fine” is also acceptable and we could include it that way.  Main reason for asking now is some of these impact more of the guide. 

**Question 1:**
Spacing – Tidyverse recommends that you don’t put a leading or trailing space in function calls, vector or matrix subscripts. 
For example,

    Tidyverse recommends the following as Good
    x[, 1] 
    mean(x, na.rm = TRUE)  
    
    #must have a space between if (
    if (debug) {
      show(x)
    }
    
    And the following are bad
    
    x[ , 1 ]                 # Additional space before , and after the 1 
    mean( x, na.rm = TRUE )  # Additional space before x and after the TRUE 
    
    Thoughts?
    Kyle - I like the extra space as it is easy to miss the , when you have [, 1]
    
    # Bad because additional spaces around debug and x
    if( debug ) {
      show( x )
    }
    Thoughts?
    Kyle - I prefer this approach because that the recomendation is always that there is not 
    a space before a (  but the added spaces make it easire to read. 
    
    # Bad because there is no space between if and the ()
    if(debug){
       show(x)
    }

    Thougths?
    Kyle - Agree I don't like this approach.  
    
    
    mean (x, na.rm = TRUE )   # Bad because you can’t have a space after function name
    Thoughts?
    Kyle - agree I don't like a space after a function name or before a () when it is used as a 
    function call or logic control like if.  A space in front of () in an equation is good, eg x + 2* ( y^2 + 24 + z )



I have always included extra spaces  and think the following is easier to read.  So I have always recommended and done

    x[ , 1]     # Good – including extra spaces is easier

    # good – space around debug but no space between if and (.  
    # This is consistent with calling a function
    if( debug ) {
        show( x )
    }
    
    mean( x, na.rm = TRUE )  # Good, the extra spaces make it more readable.  


**Question 2:** 
Where do we place the {

Which is better or do you prefer:

    Option 1 
    if( debug )
    {
        show( x )
    }
    
    for( i in c( 1, 2, 3 ) )
    {
        show( x )
    }
    
    Option 2
    if( debug ){
        show( x )
    }
    
    for( i in c( 1, 2, 3 ) ){
        show( x )
    }

