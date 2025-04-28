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