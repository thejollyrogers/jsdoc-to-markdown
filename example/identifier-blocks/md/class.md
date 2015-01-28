#Class cherry-picking

Just the docs for the Animal class. The command to generate this markdown output would be (from the root directory): 
```
$ jsdoc2md example/src/*.js --template example/identifier-blocks/template/class.hbs > example/identifier-blocks/md/class.md
```
The template looks like this: 
```handlebars
{{#class name="Animal"}}{{>docs}}{{/class}}
```
this is equivalent to: 
```handlebars
{{#class name="Animal"~}}
{{>header~}}
{{>body~}}
{{>member-index~}}
{{>members~}}
{{/class}}
```

<a name="Animal"></a>
##class: Animal
Animals are multicellular, eukaryotic organisms of the kingdom Animalia (also called Metazoa). Their body plan eventually becomes fixed as they develop, although some undergo a process of metamorphosis later on in their lives. Most animals are motile, meaning they can move spontaneously and independently. All animals must ingest other organisms or their products for sustenance (see Heterotroph).


* [class: Animal](#Animal)
  * [new Animal(species, parents)](#new_Animal_new)
  * _instance_
    * [.age](#Animal#age) → <code>number</code>
    * [.species](#Animal#species) → <code>[Species](#Species)</code>
  * _static_
    * [enum: .eMood](#Animal.eMood)

<a name="new_Animal_new"></a>
###new Animal(species, parents)
| Param | Type | Description |
| --- | --- | --- |
| species | <code>array</code> | an array of two parent [Animal](#Animal) objects |
| parents | <code>[Species](#Species)</code> | the species |

<a name="Animal#age"></a>
###animal.age → <code>number</code>
the current age

**Default**: `0`  
<a name="Animal#species"></a>
###animal.species → <code>[Species](#Species)</code>
<a name="Animal.eMood"></a>
###enum: Animal.eMood
Animal moods

**Properties**

| Name | Default | Description |
| --- | --- | --- |
| satisfied | `0` | chilling |
| angry | `1` | pissed off |
| hungry | `2` | need to eat |



##Show only part of the Class docs
E.g. just show the `header` and `body` if you like (skipping the `member-index` and `members`)

The template looks like this: 
```handlebars
{{#class name="Animal"~}}
{{>header~}}
{{>body~}}
{{/class}}
```

<a name="Animal"></a>
##class: Animal
Animals are multicellular, eukaryotic organisms of the kingdom Animalia (also called Metazoa). Their body plan eventually becomes fixed as they develop, although some undergo a process of metamorphosis later on in their lives. Most animals are motile, meaning they can move spontaneously and independently. All animals must ingest other organisms or their products for sustenance (see Heterotroph).

