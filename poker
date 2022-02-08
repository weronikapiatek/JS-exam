//1. tworzymy talię kart
function card(colour, number){
    this.colour=colour;
    this.number=number;
}

const deck=[];
function createDeck(){
    for (i=2; i<15; i++)
    deck.unshift(new card("club", i));
    for (i=2; i<15; i++)
    deck.unshift(new card("diamond", i));
    for (i=2; i<15; i++)
    deck.unshift(new card("heart", i));
    for (i=2; i<15; i++)
    deck.unshift(new card("spade", i));
 
}
createDeck();

//11=J
//12=Q
//13=K
//14=A

//2. losujemy 5 kart i tworzymy z nich tabele
let drawnCard=[];
for (i=0; i<5; i++) {
    let index;
    while (true) {
        index = Math.floor(Math.random()*deck.length);
        if (drawnCard.includes(deck[index])) {
            continue;
        }
        break;
    }
    drawnCard.unshift(deck[index]);
}
console.log(drawnCard);

//3. sprawdzamy który najwyzszy układ tworzą
function allCardsHasSameColour (arr ) {
    let first = arr[0];
    for (i=0; i<arr.length; i++) { 
        if (first.colour !== arr[i].colour) {
            return false;
        }     
    }
    return true;
}

//funkcja, która sprawdza czy wszystkie elementy następują po sobie
function strit(arr){
    arr.sort((a, b) => a.number - b.number);
        for (i=0; i<arr.length-1; i++) {
            if(arr[i].number+1 !== arr[i+1].number) {
                return false;
            }  
        }
        return true
}
let coloursOfCards=[];


function isRoyalFlush(arr) {
        if (allCardsHasSameColour(arr)) {
                for (i=0; i<arr.length; i++) {
                    numbersOfCards.unshift(arr[i].number);
                }
                for (i=10; i <= 14; i++) {
                    if (!numbersOfCards.includes(i)) {
                        return false;
                    }
                }
                return true;
        }
} 

function isStraightFlush(arr){
        if (isColour(arr) && strit(arr)) {
            return true
        }
    return false;
}

function isFourOfAKind(arr) {
    let numbersOfCards=[];
    for (i=0; i<arr.length; i++) {
        numbersOfCards.unshift(arr[i].number);
    } 
    // pivot index 0
    let pivot = numbersOfCards[0];
    let count = 1;
    for (i=1; i<numbersOfCards.length; i++) {
        if (numbersOfCards[i] === pivot) {
            count++;
        }
    }
    if (count === 4) {
        return true;
    }

    pivot = numbersOfCards[1];
    count = 1;

    for (i=2; i<numbersOfCards.length; i++) {
        if (numbersOfCards[i] === pivot) {
            count++;
        }
    }
    if (count === 4) {
        return true;
    }
    // else
    return false;
}

function isThreeOfAKind(arr) {

    let numbersOfCards=[];

    for (i=0; i<arr.length; i++) {
        numbersOfCards.unshift(arr[i].number);
    } 
    // pivot index 0
    let pivot = numbersOfCards[0];
    let count = 1;
    for (i=1; i<numbersOfCards.length; i++) {
        if (numbersOfCards[i] === pivot) {
            count++;
        }
    }
    if (count === 3) {
        return true;
    }

    pivot = numbersOfCards[1];
    count = 1;
    for (i=2; i<numbersOfCards.length; i++) {
        if (numbersOfCards[i] === pivot) {
            count++;
        }
    }
    if (count === 3) {
        return true;
    }
    // else
    return false;
}

function isOnePair(arr) {

    let numbersOfCards=[];

    for (i=0; i<arr.length; i++) {
        numbersOfCards.unshift(arr[i].number);
    } 
    // pivot index 0
    let pivot = numbersOfCards[0];
    let count = 1;
    for (i=1; i<numbersOfCards.length; i++) {
        if (numbersOfCards[i] === pivot) {
            count++;
        }
    }
    if (count === 2) {
        return true;
    }

    pivot = numbersOfCards[1];
    count = 1;
    for (i=2; i<numbersOfCards.length; i++) {
        if (numbersOfCards[i] === pivot) {
            count++;
        }
    }
    if (count === 2) {
        return true;
    }
    // else
    return false;
}

function isFullHouse(arr){
    if ( isThreeOfAKind(arr) == true && isOnePair(arr) == true)
        return true;
}

function isTwoPairs(arr){
    if (isOnePair(arr)== true && isOnePair(arr) == true)
    return true;
}

function isColour(arr) {
    if (allCardsHasSameColour(arr)) {
        return true;
    }
    return false;
}


switch (true) {

        case isRoyalFlush(drawnCard):
            console.log("You have a royal flush");
            break;

        case isStraightFlush(drawnCard):
            console.log("You have a straight flush");
            break;

        case isFourOfAKind(drawnCard):
            console.log("You have a four of a kind");
            break;

        case isFullHouse(drawnCard):
            console.log("You have a full house");  
            break;  

        case isColour(drawnCard):
            console.log("You have a colour");
            break;

        case strit(drawnCard):
            console.log("You have a straight");
            break;

        case isThreeOfAKind(drawnCard):
            console.log("You have a three of a kind");
            break;

        case isTwoPairs(drawnCard):
            console.log("You have two pairs");
            break;

        case isOnePair(drawnCard):
                console.log("You have a pair");
                break;

        default:
            console.log("couldn't match any figure");
            break;
}
