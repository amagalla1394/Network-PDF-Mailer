# Network-PDF-Mailer
Use of both Puppeteer.js and NodeMailer.js to create and send a PDF over the network.

in my code variation, you may notice the missing use of 'require' as noted below:

   my code:

        const puppeteer = ("puppeteer");

         (async () => {
            const browser = await puppeteer.launch();
            const page = await browser.newPage();
            ......
        }


   Puppeteer documentation:
   
         const puppeteer = require("puppeteer");

         (async () => {
            ......
        }
        
        
        
 The documentation given for all modules and items that i came across never helped me understand the reason for this error.
 after some attempts, i simply removed the selected error by deleting the word completely.
 
          const puppeteer = require("puppeteer");
                            ^

        ReferenceError: require is not defined
            at file:///C:....
            at ModuleJob.run (internal/modules/esm/module_job.js:152:23)
            at async Loader.import (internal/modules/esm/loader.js:166:24)
            at async Object.loadESM (internal/process/esm_loader.js:68:5)
  
  
  
  Once i had applied the change, the code ran without a problem and gave me the wanted result.
  
  
  
