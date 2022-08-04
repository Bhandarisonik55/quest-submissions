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

## chapter 2 day 1

1.   pub contract jacobtucker {

    pub let is: String

    init() {
        self.is = "the best!"
    }
}

2.     import jacobtucker from 0x03

pub fun main(): String {
    return jacobtucker.is
}

## chapter 2 day 2
## chapter 2 day 4

4.    pub contract jacobtucker {

   //account templete
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

//Script template
  import jacobtucker from 0x03
  
  pub fun main(): int{
      return jacobtucker.mynumber
  }
  
  // transaction template
  
  import jacobtucker from 0x03
  transaction(mynewnumber: int) {

  prepare(acct: AuthAccount) {}

  execute {
    jacobtucker.updatemynumber(newnumber: mynewnumber)
  }
}


## chapter 2 day 3



