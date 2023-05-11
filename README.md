
## Rafi_Smart_Contract_3
### Basic Errors and Warnings

Here is a code that contains errors.<br>
```
//SPDX-License-Identifier: MIT
pragma solidity ^0.8.7;

contract rafiSimplestorage {
  // basic data types: boolean, uint,int,address,bytes
  //uint(unsigned integer only positive),int both pos and neg
  //address is the address of the account
  //string are secretly byte objects only for text
  //bytes32 is a bytes objects whre 32 represent how many bytes we want them to be,max size is 32
  //byte objects look like 0xsdsysydggt
  //unint256 here 256 is bit (8,16,32 upto 256 we can use)
  uint256 goodNumber;//remove public so that we don't get duplicate functions at the moment we will just get the retrieve function
   //if we have whole bunch of variables inside the contract rafiSimplestorage those actually get indexed
   //here 'uint256 goodNumber' will get index to 'zero'
  
//Below we have created a new type in our solidity that holds both good number and name 
  struct People{
    uint256 goodNumber;//this get indexed to 0
    string name;// this get indexexd to 1
//whenever we have list of variables inside an object they automatically get indexed

}


//here below we want an array of People we give it visibility of public and variable name people
  People[] public people; //it is automatically giving a view function and it will give nothing if it is empty and in it's button the value that it wants is gonna be the index of the object
// array above is a dynamic array because size of the array is not given at it's initialization if we don't add any size it can be any size and here we gonna work with dynamic array

//pasing parameter of type uint256 and made the function public
  function store(uint256 _goodNumber) public{
     goodNumber = _goodNumber;
    
  }

  function retrieve() public view returns(uint256){
    return goodNumber;
  }

  //now we will create a function that is going to add individuals to Individual array
  function addCustomer(string memory _name, uint256 _goodNumber) public {
      
      people.push(People(_goodNumber,_name))//Here we have created a push function which is available in our People object
      // I have remove the semicolon from the above code 
      //Here in the above inside the push function we have created a new People object that will take good number and name. 
  //push People in our people array ,we can also do in this way
  }


  
}

```
<br><br>

It will show the following output.<br>

![C6](https://github.com/MdRafidulIslam/rafi-smart-contract3/assets/86659473/deb93a55-0a63-443b-8451-108ba200e9d7)

Figure1:Here ```red color 1``` will show which means error occured and our code is not compiling as expected.


Here is a code that shows warning.<br>
```
// I remove the software license

pragma solidity ^0.8.7;

contract rafiSimplestorage {
  // basic data types: boolean, uint,int,address,bytes
  //uint(unsigned integer only positive),int both pos and neg
  //address is the address of the account
  //string are secretly byte objects only for text
  //bytes32 is a bytes objects whre 32 represent how many bytes we want them to be,max size is 32
  //byte objects look like 0xsdsysydggt
  //unint256 here 256 is bit (8,16,32 upto 256 we can use)
  uint256 goodNumber;//remove public so that we don't get duplicate functions at the moment we will just get the retrieve function
   //if we have whole bunch of variables inside the contract rafiSimplestorage those actually get indexed
   //here 'uint256 goodNumber' will get index to 'zero'
  
//Below we have created a new type in our solidity that holds both good number and name 
  struct People{
    uint256 goodNumber;//this get indexed to 0
    string name;// this get indexexd to 1
//whenever we have list of variables inside an object they automatically get indexed

}


//here below we want an array of People we give it visibility of public and variable name people
  People[] public people; //it is automatically giving a view function and it will give nothing if it is empty and in it's button the value that it wants is gonna be the index of the object
// array above is a dynamic array because size of the array is not given at it's initialization if we don't add any size it can be any size and here we gonna work with dynamic array

//pasing parameter of type uint256 and made the function public
  function store(uint256 _goodNumber) public{
     goodNumber = _goodNumber;
    
  }

  function retrieve() public view returns(uint256){
    return goodNumber;
  }

  //now we will create a function that is going to add individuals to Individual array
  function addCustomer(string memory _name, uint256 _goodNumber) public {
      
      people.push(People(_goodNumber,_name));//Here we have created a push function which is available in our People object
      // I have remove the semicolon from the above code 
      //Here in the above inside the push function we have created a new People object that will take good number and name. 
  //push People in our people array ,we can also do in this way
  }


  
}
```
It will show the following output.<br>

![Capture77](https://github.com/MdRafidulIslam/rafi-smart-contract3/assets/86659473/9b2ecf54-44b7-4f6e-b59a-14131cbb35a7)

Figure:Here ```the yellow color 1``` shows warnings which will not stop our code from working but it is actually a good idea to check them out.<br>

<br><br>

