# TypescriptRefactorer

I think converting javascript projects to typescript projects could be made easier by creating a tool that runs the project in a browser, logging the types of the variables used, then asserting that they are of a particular type, and if so, emmiting typescript.

So javascript: `var a = 5;`
turns into `var a: number = 4;`

#Typescript input
It also has the potential for a feature that would allow for type inference to be removed from typescript code. So --
`var a = 5;` turns into `var a: number = 5;`.

And type checking of interfaces:
```
interface A {
  B: number
}

{B: 3}//#ASSERT IS A
{B: "s"}//#ASSERT IS NOT A
{}//#ASSERT IS NOT A

```

