# OTPSent---Automated-tests
The final part of the series that automates tests based on time and validates the OTP in MongoDB.

Terminologies - fake, unit tests, mocks, non-fatal expectations, fatal assertions

The sheer joy of doing Agile is not just in testing more but be able to refine design through tests, see methods and method parameters take shape and discover newer forms of improvement to code, to make the final product of quality. 

To illustrate these advantages of Agile, let me enumerate the different techniques used in this series. First, the requirement, based on the web and using the Node.js framework, uses Express. But, to run tests on a live server is not something that is recommended hence, a 'fake' server is created through 'supertest'. 

A fake helps by decoupling the dev environment from the test. 

A fake is different from a mock in that a fake completely replicates the functionality of an entity whereas, a mock simply provides a temporary mirror of the entity.

Once the fake server is made aware of the initialization server script, 'supertest' runs the script (server) and shuts it down once the tests are complete. But there is a catch because Node.js is an asynchronous environment and therefore, if any callback or promise remains pending, the calling process would be responsible to handle the shutdown event. But again, there is another catch, although the calling environment knows its responsibilities, it becomes difficult to determine whether it is a Node.js, a mocha test or a mongodb callback/promise that is pending. So, by default, because of this sequence of testing, bugs in code get identified and rectified, one of the major advantages of doing testing the Agile way.

Unit tests are created in 'mocha' with some expectations handled by 'chai', two popular and prevalent test frameworks for Node.js.

To be updated...

The scenario that this series has followed has been one of using a 
