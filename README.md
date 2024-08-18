# Next js

Next.js is a React framework for building full-stack web applications. You use React Components to build user interfaces, and Next.js for additional features and optimizations.

Under the hood, Next.js also abstracts and automatically configures tooling needed for React, like bundling, compiling, and more. This allows you to focus on building your application instead of spending time with configuration.

Whether you're an individual developer or part of a larger team, Next.js can help you build interactive, dynamic, and fast React applications.

## Installation

`npx create-next-app@latest myapp `

- What is your project named? my-app
- Would you like to use TypeScript? No / Yes
- Would you like to use ESLint? No / Yes
- Would you like to use Tailwind CSS? No / Yes
- Would you like your code inside a `src/` directory? No / Yes
- Would you like to use App Router? (recommended) No / Yes
- Would you like to use Turbopack for `next dev`?  No / Yes
- Would you like to customize the import alias (`@/*` by default)? No / Yes
- What import alias would you like configured? @/*

> how to run

```json
"dev": "next dev", // use this for run
"build": "next build",
"start": "next start",
"lint": "next lint"
```

> Example

``` javascript
export default function Home() {
  return (
    <main>
    <h1 className="">UDIT KUMAR</h1>
    <button onClick={()=>alert("udit")}>Click me</button>
    </main>
  );
}
```

```json
Error: Event handlers cannot be passed to Client Component props.
  <button onClick={function onClick} children=...>
                  ^^^^^^^^^^^^^^^^^^
If you need interactivity, consider converting part of this to a Client Component.
```

Use the `"use client";` at the top

> correct code

``` javascript
"use client";

export default function Home() {
  return (
    <main>
    <h1 className="">UDIT KUMAR</h1>
    <button onClick={()=>alert("udit")}>Click me</button>
    </main>
  );
}
```

## Using inner components

``` javascript
"use client";

const  InnerComponet = ()=>{
  return(
    <>
    hello inner component
    </>
  )
}

export default function Home() {
  return (
    <main>
    <h1 className="">UDIT KUMAR</h1>
    <button onClick={()=>apple()}>Click me</button>
    {/* <InnerComponet/> */} // render as componet
    {InnerComponet()} // call as function
    </main>
  );
}
```