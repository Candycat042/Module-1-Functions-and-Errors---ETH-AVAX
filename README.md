Smart Contract Project
For this project, write a smart contract that implements the require(), assert() and revert() statements.

There are three methods that constitute the error-handling process in Solidity:

require(): Used to validate certain conditions before further execution of a function. It takes two parameters as an input.
The first parameter is the condition that you want to validate and the second parameter is the message that will be passed back to the caller if the condition fails. If the condition is satisfied, then the execution of the function continues and the execution jumps to the next statement. 

However, if the condition fails, then the function execution is terminated and the message (the second parameter) is displayed in the logs. The second parameter, however, is optional. require() will work even if you pass only parameter, that is, the condition to be checked. The require() statement is defined as follows:

require(<condition to be validated> , <message to be displayed if the condition fails>);

assert(): The assert function, like require, is a convenience function that checks for conditions. If a condition fails, then the function execution is terminated with an error message.
assert() takes only one parameter as input. You pass a condition to assert(), and if the condition is true, then the function execution continues and the execution jumps to the next statement in the function. The assert() statement is defined as:

assert(<condition to be checked/validated>);

revert(): Can be used to flag an error and revert the current call. You can also provide a message containing details about the error, and the message will be passed back to the caller. However, the message, like in require(), is an optional parameter. revert() causes the EVM to revert all the changes made to the state, and things return to the initial state or the state before the function call was made.
The reason for reverting is that there is no safe way to continue execution because something unexpected happened. This is important as it helps in saving gas.

Since the function execution stops after the revert() statement, the remaining gas is also returned back to the user. If you don't use the revert() statement and some error occurs, then the entire gas is lost. Using revert() does not return the consumed gas, however. The gas that is consumed is consumed, and it cannot be returned.

Specifically, your project must provide the following to be successfully completed:

Functionality
Contract successfully uses require()
Contract successfully uses assert()
Contract successfully uses revert() statements
