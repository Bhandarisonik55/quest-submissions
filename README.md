# Sonik quest-submissions

## chapter 1 day 1 quest

Here are some answers;
 1. Blockchain is a decentralized network in which users across the world with data being distributed among them in the type of shared database. Blockchain is a type of digital ledger techonolgy that consists of growing lists of records which are called blocks that are securely linked through cryptography.
 
 2. Smartcontracts are programs that allows us to specify some functionality that user can interact with. 
 
 3. Scrpit means veiw or read the datas stored in blockchain without any costs and it do not change the original blockchain. 
     while Transaction is a process of making changes in datas by costing you money and changes the status of blockchain.
     
     
## chapter 2 day 2 quest

1. 5 cadence language pillars are;
      a. Saftey and Security: Because of its insanely strong type system, separation between contracts and transactions, and Resource Oriented Programming cadence maintains highest level of saftey and security.
      b. Clarity: Making the code declarative and allowing the developer to express their intentions directly cadence makes code easy to read, especially Smart Contract code so that we, as users, can verify it is safe.
      c. Approachability: Cadence is written is very familiar to other programming languages, making it easy to transition to if you have prior experience.
      d. Developer Experience: Cadence makes error message very clear so that developer donot gets frustated.
      e. Resource Oriented Programming
      
2. Because it consist of all the requirements of a safe and trustworthy program as listed on the pillars.

## chapter 2 day 1 quest

1.  
```cadence
pub contract jacobtucker {

    pub let is: String

    init() {
        self.is = "the best!"
    }
}
   ```

2.     import jacobtucker from 0x03

pub fun main(): String {
    return jacobtucker.is
}

## chapter 2 day 2 quest

1.
   Because it’s making changes in the BlockChain, it has to be done in the transactions not in the scripts as the scripts are just meant for viewing the data.
   

2.
     AuthAccount is a type that allows us to access the data in the user’s account to sign the transaction and verify it.

3.
    Prepare phase is to access the information/data in the user's account whereas the execute phase can’t access the information in the user's account. The execute phase is where the actual modification on data takes place.  




4.    pub contract jacobtucker {

   //account templete//
    pub let is: string
    pub var mynumber: int

    pub fun updatemynumber(newnumber: int) {
        self.mynumber = newnumber
    }

    init() {
        self.is = "the best"
        self.mynuber =0
    }
}

//Script template//
  import jacobtucker from 0x03
  
  pub fun main(): int{
      return jacobtucker.mynumber
  }
  
  // transaction template//
  
  import jacobtucker from 0x03
  transaction(mynewnumber: int) {

  prepare(acct: AuthAccount) {}

  execute {
    jacobtucker.updatemynumber(newnumber: mynewnumber)
  }
}


## chapter 2 day 3 quest

1.
   pub fun main(): int{
    var S:[string]=["mom","dad","brother"]
    log(S)
    return 1
    }
    

2.
    pub fun main(){
     let S:{string:Uint64}={"facebook":1,"instagram":3,"youtube":2,"reddit":5,"linkedin":4}
     }
     
  
  

  3.
     force unwrap operator (!) unwraps an optional type by saying :"if this nil,panic! if it's not nil we're fine, but get rid of optional type".
       for example;
                          Pub fun main(): String {
                          Let example: {Int: String} = {5: “bmw”, 20: “audi”, 30: “merceds"}
                          Return example[5]!   //The value “bmw” is no longer an optional type. It now becomes the type string and we won’t have any errors in compilation.
}

4.
  We are getting the error because of a mismatch in the declared return type of the function and the returned type that is actually being returned. 
 We can fix it using the force-unwrap operator.
 

## chapter 2 day 4 quest

1,2 & 3:
                 pub contract travel {

    pub var traveldocs: {string: travelplan}
    
    pub struct travelplan {
        pub let traveller: String
        pub let destination: String
        pub let duration_in_days: int
        pub let budget: int

        
        init(_traveller: String, _destination: String, _duration_in_days: int, _budget: int) {
            self.traveller = _string
            self.destination = _string
            self.duration_in_days = _int
            self.budget = _int
        }
    }

    pub fun addtraveller(traveller: String, destination: String, duration_in_days: int, budget: int) {
        let newtraveller = travelplan(_traveller: traveller, _destination: destination, _duration_in_days: duration_in_days, _budget: budget)
        self.traveldocs[traveller] = newtraveller
    }

    init() {
        self.traveldocs = {}
    }

}


 4.
        import travel from 0x01

transaction(traveller: String, destination: String, duration_in_daysy: int, budget: int) {

    prepare(signer: AuthAccount) {}

    execute {
        travel.addtraveller(traveller: traveller, festination: destination, duration_in_days: duration_in_days, budget: budget)
        log("We're done.")
    }
}

 5.
   import travel from 0x01

pub fun main(traveller: string): travel.traveller {
    return travel.traveldocs[travel]
}



