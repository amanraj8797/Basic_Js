/*
Assessment Requirements
1. Create a variable that can hold a number of NFT's. What type of variable might this be?
2. Create an object inside your mintNFT function that will hold the metadata for your NFTs. 
   The metadata values will be passed to the function as parameters. When the NFT is ready, 
   you will store it in the variable you created in step 1
3. Your listNFTs() function will print all of your NFTs metadata to the console (i.e. console.log("Name: " + someNFT.name))
4. For good measure, getTotalSupply() should return the number of NFT's you have created
*/

//  Create a variable to hold the number of NFTs

let totalNFTs = [];

/*  This function will take in some values as parameters, create an
    NFT object using the parameters passed to it for its metadata, 
    and store it in the variable above. */

function mintNFT(_name, _desc, _color, _bling) {
    const newNFT = {
        name: _name,
        description: _desc,
        color: _color,
        bling: _bling
    };
    totalNFTs.push(newNFT);
    return newNFT;
}

/* create a "loop" that will go through an "array" of NFT's
   and print their metadata with console.log() */

function listNFTs() {
    for (let i = 0; i < totalNFTs.length; i++) {
        console.log("NFT " + (i + 1) + ":");
        console.log("Name: " + totalNFTs[i].name);
        console.log("Description Color: " + totalNFTs[i].description);
        console.log("Color: " + totalNFTs[i].color);
        console.log("Bling: " + totalNFTs[i].bling + "\n");
    }
}

// print the total number of NFTs we have minted to the console

function getTotalSupply() {
    return totalNFTs.length;
}

// call your functions below this line

mintNFT("Aman", "Triangular Shape", "Red", "Gold Chain");
mintNFT("Raj", "Rectangular shape", "Green", "Diamond Ring");

listNFTs();

console.log("Total NFTs minted: " + getTotalSupply());
