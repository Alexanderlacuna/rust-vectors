 ### Vectors
 - it is an array-like data type that stores related items
 - one major difference between a vector and an array is that vectors are growable that means their you do append and deletion of items 

 - another difference is that vectors are stored in heap rather than stack cause they grow and shrink


 ``` Rust
//   define vectors
let y=Vec::new();

// the above creates an empty vetor
 

 ```


- compiling the above code would results into an error cause the the compiler doesn't know th e
item to be stored in the vector(You have to explictly define the data type)

``` Rust
let y:Vec<i32>=Vec::new();
// the above store items of type i32

```



- Doing insertion and deletion

``` Rust
y.push(12);
// if you tried to push a non  i32 type item it fails
// for example

y.push(23.3)

// to get the length

//getting the length
y.len()

//pop removes the the last element from the vector and returns an Option of Some(val) or None if no item exists
let removed_item=y.pop()

if let Some(val)=removed_item {
   println!("the value is  {:?}",val)
}
else {
    println!("the vector is empty")
}


// removing an a given index
y.remove(12)

// this code will panic if the index is out of bound
```


