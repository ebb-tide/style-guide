# React/JSX Style Guide

*Inspired by the [AirBnB](https://github.com/airbnb/javascript) style guide*

## Table of Contents

  1. [Promises vs Async](#promises-vs-async)

## Promises vs Async

  - Prefer async/await pattern over promises with try/catch

  ```javascript
  // DO:
  func = async () => {
    try{
      const data = await functionThatReturnsPromise()
      doTheNextThing(data)
    } catch(error){}
      console.error(error)
  }

  // NOT:
  func = () => {
    functionThatReturnsPromise()
      .then(data) => {
        doTheNextThing(data)
      })
      .catch((error) => {
        console.error(error)
      })
  }
  ```

  > Why?
