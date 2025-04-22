Problem 1:  Given an array of size N. Find the highest and lowest frequency element.

Example 1:
Input: array[] = {10,5,10,15,10,5};
Output: 10 15
Explanation: The frequency of 10 is 3, i.e. the highest and the frequency of 15 is 1 i.e. the lowest.

Solution: function findHighestOccurance(arr){
    debugger;
    let copyArr = arr;
    let hashObj = {};
    let highest = 0;
    let highestOccurance = 0;
    copyArr.forEach((elm) => {
        if(hashObj[elm]){
            hashObj[elm] = hashObj[elm] + 1;
        } else {
            hashObj[elm] = 1;
        }    
    });

    Object.keys(hashObj).forEach((elm) => {
        if(hashObj[elm] > highestOccurance){
            highestOccurance = hashObj[elm];
            highest = elm;
        }
    })
    return `${highest} ${highestOccurance}`;
}