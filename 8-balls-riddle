const balls = [1,1,1,1,1,2,1,1];
let sum=0;
let sum2=0;

function sortBalls (arr){
    for (i=0; i<3; i++)
        sum=sum + arr[i];

    for (i=3; i<6; i++)
        sum2=sum2 + arr[i];

        if (sum===sum2){//jeśli sumy dwóch pierwszych wazen, czyli 6 kulek jest równa, ciezsza kulka bedzie znajdowala sie posrod pozostalych 2 kulek
            if (arr[6]>arr[7])
                {console.log("najcięzsza jest kula nr 7");}
            else if(arr[7]>arr[6])
                {console.log("najcięzsza jest kula nr 8");}
                }

        else if (sum>sum2){
            if (arr[0]==arr[1])
                {console.log("najcięzsza jest kula nr 3 ")}
            else if (arr[0]>arr[1])
                {console.log("najciezsza jest kula nr 1");}
            else
                {console.log("najciezsza jest kula nr 2");}
                }

        else if (sum2>sum){
            if (arr[3]==arr[4])
                {console.log("najcięzsza jest kula nr 6 ")}
            else if (arr[3]>arr[4])
                {console.log("najciezsza jest kula nr 4");}
            else
                {console.log("najciezsza jest kula nr 5");}
            }}

sortBalls(balls);
