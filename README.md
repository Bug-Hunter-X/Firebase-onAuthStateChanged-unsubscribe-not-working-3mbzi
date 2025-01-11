# Firebase onAuthStateChanged unsubscribe issue
This repo demonstrates a common issue with the Firebase `onAuthStateChanged` listener: not unsubscribing properly when the component unmounts.  Failure to unsubscribe can lead to memory leaks and unexpected behavior.
The `bug.js` file shows the problematic code. The `bugSolution.js` file provides the correct implementation.
## Problem
The original code fails to unsubscribe from the `onAuthStateChanged` listener, resulting in the listener continuing to run even after the component is unmounted. This can lead to memory leaks and performance issues.
## Solution
The solution involves returning an unsubscribe function from the component to ensure that the listener is properly unsubscribed when the component is unmounted.