## Mengullo JavaScript CODE

## CODE

// John Xyriz E. Mengullo | 2.3BSIT

/*
Assessment Requirements
1. Create a variable that can hold a number of NFT's. What type of variable might this be?
2. Create an object inside your mintNFT function that will hold the metadata for your NFTs. 
   The metadata values will be passed to the function as parameters. When the NFT is ready, 
   you will store it in the variable you created in step 1
3. Your listNFTs() function will print all of your NFTs metadata to the console (i.e. console.log("Name: " + someNFT.name))
4. For good measure, getTotalSupply() should return the number of NFT's you have created
*/

// create a variable to hold your NFT's
let nfts = [];

// this function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT(name, creator, description) {
    const nft = {
        name: name,
        creator: creator,
        description: description
    };
    nfts.push(nft);
}

// create a "loop" that will go through an "array" of NFT's
// and print their metadata with console.log()
function listNFTs() {
    nfts.forEach(nft => {
        console.log("Name: " + nft.name);
        console.log("Creator: " + nft.creator);
        console.log("Description: " + nft.description);
        console.log("----------------------");
    });
}

// print the total number of NFTs we have minted to the console
function getTotalSupply() {
    console.log("Total NFTs: " + nfts.length);
}

// call your functions below this line
mintNFT("Fender Stratocaster", "Leo Fender", "A double-cutaway body, three single-coil pickups, and tremolo bridge result in its bright sounds and versatility.");
mintNFT("Gibson", "Lester William Polsfuss", "It's known for its unique tone and beautiful design, featuring humbucker pickups and sturdy craftsmanship.");
mintNFT("Ibañez RG Series", "Hoshino Gakki", "Sleek design, fast necks, and versitile sound, making them popular among rock and metal guitarists.");
mintNFT("Jackson Soloist", "Grover Jackson", "Sleek, fast-necked electric guitar with an aggressive tone, favored by metal and hard rock guitarists.");

listNFTs();
getTotalSupply();
