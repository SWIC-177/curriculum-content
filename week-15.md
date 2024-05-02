# Week 1️⃣5️⃣

**Note:** This week's content starts for Thursday as we extended last week's content to Tuesday.

## Homework Due Thursday

The homework will just be code-alongs. You will watch the video and follow along. You will then commit and push your code and **write proper commit messages.**

You will also write a reflection Gist to convey your thoughts on the videos. This is a chance to mention any particular nuggets from the videos to show your attention to details, and that you did take the time to watch the videos. You should show what you actually learned as opposed to just blindly following along.

I'm particularly interested in your thoughts on `reduce`. Is it too much? Is it easy? Is it just right? What questions remain?

### Testing ✅ `getLastName`

**Note:** The assumption is that you did already do `npm i -D vitest`, otherwise none of your tests ✅ will work.

We introduce `describe` as we write multiple tests for the `getLastName` function.

1. [Video](https://somup.com/cZhVnY56EN)
1. [Video](https://somup.com/cZhVnO56GI)

The videos show the long way of writing tests and you should do that until this becomes second nature. However, you can also write the tests in a more concise way like this:

```js
describe("getLastName", () => {
  it("should return the last name of a full name", () => {
    expect(getLastName("John Cena")).toBe("Cena");
  });

  it("should return the last name of a full name", () => {
    expect(getLastName("Randy Orton")).toBe("Orton");
  });

  it("should return the last name of a full name", () => {
    expect(getLastName("The Rock")).toBe("Rock");
  });
});
```

### Test Driven Development (TDD)

We've mentioned this before, and now we'll actually do it. We'll write the tests first and then write the code to make the tests pass.

Before proceeding with the videos, you may wish to consider the following pseudo code:

```text
function merge2ArraysIntoAnArrayOfObjects(parameters):
    - The function takes an object as a parameter with the following properties:
        - a1: An array
        - a2: Another array of the same length as a1
        - key1: A string representing the key for elements from a1 in the resulting objects
        - key2: A string representing the key for elements from a2 in the resulting objects

    - Initialize an empty array to store the accumulated results

    - Iterate over each element in a1 using the reduce function:
        - For each element in a1 at index i:
            - Create a copy of the accumulated results array
            - Create a new object:
                - Set the property named key1 to the current element from a1
                - Set the property named key2 to the element at the same index i from a2
            - Append the new object to the copy of the accumulated results array
            - Return the updated accumulated results array

    - Return the final accumulated results array containing objects with properties key1 and key2
```

1. [Failing Test](https://somup.com/cZhVnz56GB)
1. [Passing Test](https://somup.com/cZhVnN56mO)
1. [Break Down of `reduce`](https://go.screenpal.com/watch/cZhVeeVMadi)
