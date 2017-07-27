# Testing with Rspec on Lynda 

## Configuring Rspec 
 - Project specifically you can create a `.rspec` file that has the configurations in it that checks into source code or github
 - Locally you can create a `.rspec-local` file that has your custom settings others may not want to use.  
 - Command line is an option and there are others as well.

## Setting up Rspec 
 - `rspec --init` 
 - Creates two files the .rspec adn the spec_helper.rb
 

## Running Test
`rspec spec` will run all tests inside of the spec folder that ends in spec.rb.  Most helpers will be ignored because they typcially are written as spec_helper.rb

## Test Doubles, aka data stubs,mocks,etc.  
These are where you add mock data or mock classes to the spec tests.  The idea is that for methods that make large database calls, or generate random data have a more controlled and testabled data set.  Another use case is when you have to make a server call, but don't want to waste that time or require an internet connection to run the tests.  

## Messages 
Sending and returning data to methods or functions.  You can tell an aboject to be allowed to recive and return data or you can expect it to recieve and return data.  

Example:  This can also be found in the code samples car_project used to follow along with the lynda tutorial series. 
```
it "allows setting data" do 
  dbl = double("ClassName")
  allow(dbl).to recieve(:param).and_return("result")
  expect(dbl.param).to eq("result)
end 
``` 

## Code Samples provide in lesson tutorials of how rspec works. 