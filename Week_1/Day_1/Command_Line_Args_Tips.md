### Tips

In order to be able to submit a function with arguments in the command line like this:

```console
node function.js 10 25
````

... we must urgs process.argvs. This will result in the following:

```console
[ 'node',
  '/vagrant/w1/d1-focal/function.js',
  '10',
  '25' ]
```
To make things easier, we remove the first two indices and store this into a variable:

```javascript
const args = process.argv;
const input = args.slice(2);
```

Now we can use the function with as many arguments as we want!

(Don't forget to call function later on!)