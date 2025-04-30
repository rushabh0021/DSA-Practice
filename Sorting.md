1. Selection Sort

function selectionSort(arr){
    let copyArr = arr;

    for(let i=0; i < arr.length; i++){
        
        for(let j= i; j < arr.length; j++){
            if(copyArr[j] < copyArr[i]){
                let temp = copyArr[j];
                copyArr[j] = copyArr[i];
                copyArr[i] = temp;
            }
        }
    }
    return copyArr;
}

2. Bubble Sort

function bubbleSort(arr){
    const outputArr = arr;
    
    for(let i= arr.length; i >= 0; i--){
        for(let j= 0; j <= i; j++){
            if(outputArr[j] > outputArr[j + 1]) {
                const temp = outputArr[j];
                outputArr[j] = outputArr[j+1];
                outputArr[j+1] = temp;
            }
        }
    }
    return outputArr;
}