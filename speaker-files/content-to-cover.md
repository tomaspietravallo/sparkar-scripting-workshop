# List
- Scene + Promises (fast forward to await)
- Touch Gestures
- Patch bridge
- Persistence (?)

# Long form
## Scene + Promises

Quickly re-introduce how to import modules.

```ts
import Scene from 'Scene';
```

Using the findFirst function

```ts
Scene.root.findFirst();
```

But (a)wait, Promises!

```ts
async function main(){
    // Spark promises it'll do its job
    // use await to wait for the function to finish it's job
    const obj = await Scene.root.findFirst('name');
};

main(); // avoid IIFEs
```

```ts
// SceneObjectBase type & properties
// may (will) need to get into Reactive for this 🙄
obj.transform.position;
obj.hidden;
obj.name;
```

## TouchGestures
An intro to subscriptions.

```ts
import TG from 'TouchGestures';

function whatToDoOnTap(){};

// listen to events, define callbacks
TG.onTap().subscribe(whatToDoOnTap);

TG.onTap().subscribe( () => {
    // arrow function
});
```

```ts
// idea. pseudo-code:
for(obj in objs){
    TG.onTap(obj).subscribe(()=>doThing(obj.name));
};
```
### Event sources from Signals

```ts
import Time from 'Time';
Time.ms.monitor().subscribe();
```

## Patch Bridge

```ts
import Patches from 'Patches';

async function main(){
    // show the error in Spark, no catching
    Patches.inputs.setScalar('name', 1);

    // how to get a value
    await Patches.outputs.getScalar('other');
};

main(); // avoid IIFEs
```