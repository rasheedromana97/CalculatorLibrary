*Note this README.md file contains information about CI that I have understood from creating this project. It is the theory behind CI*

# What is Continuous Integration?
It is the practice of frequently building and testing each change done to your code automatically and as early as possible. 

# How does this matter?
Well just imagine going to work with alot of ideas. You want to share them with your co-workers and implement them. However, you are wasting your precious time in:
  - Worrying about introducing a bug every time you make changes
  - Fixing the mess someone else made so you can integrate your code
  - Making sure the code works on every machine, operating system, and browser.
These problems can be solved in a short period of time when you use CI.

# How do we do this?
## 1. Creating a single source repository
  Every developer working on that project creates a local copy and works on it. Once they are done making changes, they         merge into the central repository. A standard procedure is to use version control systems (VCS) like Git to handle the         workflow. Developers usually use an external service to host their source code and handle the moving parts. A few examples     are GitHub, BitBucket, and GitLab.
  
## 2. Automating the Build
   **What does it mean by building a code?**
     Building a code means taking the raw source code, and everything necessary for its execution, and translating it into a        format that computers can run directly. 
   **How do we build a Python code?**
      Python is an interpreted language, so its “build” mainly revolves around test execution rather than compilation.
   
   Now think about repeating these steps after every small change. It's tedious and time consuming. If this was the case,        companies would have to hire a person just to complete this task! With large and complicated piece of code, it might take      days! If you used a library, package, or framework that doesn’t come with the Python standard library (think anything you      needed to install with pip or conda), Python needs to know about that, so the program knows where to look when it finds        commands that it doesn’t recognize. You store a list of those packages in requirements.txt or a Pipfile. These are the        dependencies of your code and are necessary for a successful build.
   
   **What is the advantage of automating the build?**  
      - Developers commit frequently reducing the risk of major errors that code break the code.
      - Error detection is easier and faster
      - There is no chance of "Breaking the build"
      
## 3. Automated Testing
      
   Every time a developer writes a code, they are responsible for writing a test or at the least you should cover every new      function with a unit test. Running tests automatically, can help catch bugs. By automating this process, you can be at        ease even if you forget to test the code locally since the server will test your code.
   What happens after you have performed every test on your code? Can you now deploy it in your production environment? No!      Companies usually have an environment that mimics the production environment known as *development environment* or            *staging environment* , or *testing environment*
      
   The development environment should replicate production conditions as closely as possible. This setup is often called         *DEV/PROD parity*
      
  Now that we understand the essential practices of CI. You can use the above code(Code credit: realPython) to practice         this whole chain of necessary steps to use CI. This chain is known as ***CI Pipeline***.
   
