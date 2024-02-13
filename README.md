# practice
this is javascript and ds exercises



Given an array a of size N which contains elements from 0 to N-1, you need to find all the elements occurring more than once in the given array. Return the answer in ascending order. If no such element is found, return list containing [-1]. 



  let a = [5, 4, 2, 1, 4, 6, 1, 2, 2];
  let n = a.length;
  let duplicates = (arr, n) => {
    let countobj = {};
    let dupArr = [];
    for (const ele of arr) {
      if (countobj[ele]) {
        countobj[ele] += 1;
      } else {
        countobj[ele] = 1;
      }
    }
    for (const key in countobj) {
      if (countobj[key] > 1) {
        dupArr.push(Number(key));
      }
    }
    let dupArray = dupArr.sort();

    return dupArray.length ? dupArray : -1;
  };
  console.log(duplicates(a, n));
