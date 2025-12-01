## $${\color{red}YAML}$$


#### object
```YAML
person:
```

  #### string value. single/double quotes anchoring
  ```YAML
  name: &name "keny" # anchor name doesn't have to be the same as key name
  occupation: 'boss'
```

  #### integer value type casting
  ```YAML
  age: !!float 69 # 69.0
  gpa: !!str 66.6 # "66.6"
```
  #### exponential form
  ```YAML
  fav_num: 1e+20
```

  #### boolean
  ```YAML
  boss: true
```

  #### dates (ISO 8601)
  ```YAML
  birthday: 1993-06-06 16:06:06
```

  #### null value
  ```YAML
  flaws: null
```

  #### list of items
  ```YAML
  hobbies: 
    - music
    - running
    - painting
    - tattooing
```

  #### another way to create lists
  ```YAML
  movies: ['The Office', "Harry Potter"]
```

  #### store list of objects
  ```YAML
  friends:
  - name: "keny"
    age: 69
  - {name: 'Billy', age: 16}
  -
    name: "Alexis"
    age: 21
```

  #### long text. newline will be removed
  ```YAML
  description: >
If you like — I can try to dig past records
(via web archives / WHOIS)
to check whether “keny.studio” once existed.
That might show if it was a website that went offline,
or if the domain was ever registered.
Do you want me to attempt that for you now?
```

  #### verbatim. format will be preserved

  ```YAML
  signature: |
    KENY.STUDIO
    Luxury Company
    email - keny@keny.studio
```

  #### anchoring. value will refer to anchor &ANCHOR
  ```YAML
  id: *name # "keny"
```


  #### anchoring key-value object
  ```YAML
  base: &base
    var1: 'value1'
  foo:
    <<: *base # expands to    var1: 'value1'
    val2: 'value2'
```
