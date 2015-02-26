Warning: 
==============
This is probably not a good idea, and may be functionally impossible. 

Problem being solved:
==============
"Loading the dependencies for a single test file takes over ten seconds ...  reducing it to the near minimum possible would involve explicit requires in every file"

Therefore:
==============
a tool that 'guesses' what requires you need for a specific ruby test and puts the autogenerated answers (if successful) into a file. Not sure if it ever made it to prod-ready.

So if file A_spec has B.new() and C.new() it finds files A.rb and B.rb, drops them in spec_helper_requires_for_A.rb, and all the writer of A_spec has to do it 'require_relative spec_helper_requires_for_A'



Notes:

--require spec_helper