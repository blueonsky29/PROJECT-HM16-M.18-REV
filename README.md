# PROJECT-HM16-M.18-REV
Creating a custom Gradle task and adding libraries in Visual Studio Code (VSCode) involves a similar process as doing it in a terminal. 
Here are the steps:

**1. Install VSCode and Required Extensions:**
  
  If you haven't already, install Visual Studio Code and make sure you have the necessary extensions installed for Gradle development:

**-   Gradle Language Support:**
      
      This extension provides syntax highlighting and other features specific to Gradle. You can install it from the VSCode Extensions Marketplace.


**2. Create a New Gradle Project:**
  
  Create a new directory for your Gradle project and open it in VSCode.


**3. Initialize Gradle Project:**
  
  In the terminal within VSCode, navigate to your project directory and run the following command to initialize a Gradle project:
    
    gradle init --type java-library
  
  This will create the project structure with the necessary Gradle files.

**4. Define a Custom Task:**
  
  Open the `build.gradle` file in VSCode and add the following code to define a custom task:
    
    task greetingTask(type: DefaultTask) {
      doLast {
          String name = project.hasProperty('name') ? project.property('name') : 'Gradle User'
          println "Hello, $name! Welcome to Gradle World!"
      }
    }

**5. Run the Custom Task:**

  In VSCode's integrated terminal, navigate to your project directory and run the custom task using the following command:
  
    ./gradlew greetingTask -Pname=YourName

  Replace YourName with your desired name. This will execute the custom task and display the greeting message with the provided name.

**6. Add Libraries:**

  In the build.gradle file in VSCode, add the libraries you want to include in your project's dependencies, just like in the previous steps:

	dependencies {
      implementation 'com.google.guava:guava:29.0-jre'
      testImplementation 'junit:junit:4.13'
	}

**7. Push to GitHub:**

  - Create a new repository on GitHub.

  - In VSCode, initialize a Git repository:
    
    	 git init

	
  - Add all files to the repository:

     	 git add .

  - Commit the changes:

   		 git commit -m "Initial commit"

  - Add the remote repository URL:
    
   		 git remote add origin https://github.com/<your_username>/<repository_name>.git

    Replace **<your_username>** with your GitHub username and **<repository_name>** with the name of your GitHub repository.

  - Push the code to GitHub:

   		 git push -u origin master

**8. Verify on GitHub:**
	
Go to your GitHub repository and verify that the code, including the custom Gradle task and the library dependencies, has been pushed successfully.

### [
![GRADLE RUNNING](https://github.com/blueonsky29/PROJECT-HM16-M.18-REV/assets/101382822/f1921db2-0934-483b-b840-8b7ddce308a8)
](url)
