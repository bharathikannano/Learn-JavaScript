# Objects

### Object Cloneing
```javascript
var obj1 = { foo: 'bar', x: 42 };
                                          
var clonedObj = { ...obj1 };        // { foo: "bar", x: 42 }
```

### Object concatenation
```javascript
var obj1 = { foo: 'bar', x: 42 };
var obj2 = { foo: 'baz', y: 13 };

var mergedObj = { ...obj1, ...obj2 };     // { foo: "baz", x: 42, y: 13 }
```

```javascript
var obj1 = { foo: 'bar', x: 42 };
var obj2 = { foo: 'baz', y: 13 };
const merge = ( ...objects ) => ( { ...objects } );

var mergedObj = merge ( obj1, obj2);
// Object { 0: { foo: 'bar', x: 42 }, 1: { foo: 'baz', y: 13 } }

var mergedObj = merge ( {}, obj1, obj2);
// Object { 0: {}, 1: { foo: 'bar', x: 42 }, 2: { foo: 'baz', y: 13 } }
```

```javascript
const Basic = {name: 'Bharathikannan', title: 'Front End Developer'};

const GitURL = 'https://github.com/Bharathikannano';

const profile = { ...Basic, ...(GitURL && {GitURL})};

console.log(profile);

/*
  {name: 'Bharathikannan', 
  title: 'Front End Developer'
  GitURL: 'https://github.com/Bharathikannano'}
  */
```

### Object.values() and Object.keys()
```javascript
var obj = {"Name":"Bharathikannan", "Age":28, "City":"chennai", "Country":"India"};

Object.keys(obj);           //["Name", "Age", "City", "Country"]

Object.values(obj);         //["Bharathikannan", 28, "chennai", "India"]
```

### Object.entries()
```javascript
var obj = {"Name":"Bharathikannan", "Age":28, "City":"chennai", "Country":"India"};


for(let[key,value] of Object.entries(obj)){
console.log(`key:${key} <=====> value:${value}`);
}


/*
key:Name <=====> value:Bharathikannan
VM6954:2 key:Age <=====> value:28
VM6954:2 key:City <=====> value:chennai
VM6954:2 key:Country <=====> value:India
*/


const map = new Map(Object.entries(obj));

/*
Map(4) {"Name" => "Bharathikannan", "Age" => 28, "City" => "chennai", "Country" => "India"}
*/


```

### spread examples
```javascript
var obj = {"Name":"Bharathikannan", "Age":28, "City":"chennai", "Country":"India"};

let{Name:FullName, Age, Country} = obj;
console.log(FullName);                //Bharathikannan

```
