# Tech-Quiz
An online Tech quiz Website
# Welcome to Hacktoberfest #10 2023
![Hacktoberfest Banner](hf10_banner.png)

⭐ This repository is made for beginners who are looking for a beginner-friendly repository to start open source contributions! 

⭐ Feel free to use this project to make your first contribution to an open-source project on GitHub.

⭐ Star this repository for a better reach!

# What is Hacktoberfest? 🤔
A month-long celebration from October 1st to October 31st presented by Digital Ocean and DEV Community collaborated with GitHub to get people involved in Open Source.

https://hacktoberfest.com/

# Note 🔥
1. To qualify for digital rewards by Hacktoberfest, you must register for the event and make four Pull Requests (PRs) between October 1-31, 2023 (in any time zone).

2. Pull requests can be made in any GitHub or GitLab hosted project that’s participating in Hacktoberfest (look for the “hacktoberfest” topic). 

3. The first 50,000 participants to have their first PR/MR accepted will have a tree planted in their name through Tree Nation

## How to Contribute

To contribute to our Tech-Quiz:

1. **Fork the Repository:** Click the "Fork" button at the top right of this repository to create a copy in your GitHub account. 🍴

2. **Clone Your Fork:** Clone the forked repository to your local machine using Git. 🖥️

   ```bash
   
   git clone https://github.com/yourusername/Tech-Quiz.git
   
   ```

3. **Create a Branch:** Create a new branch for your contribution under the respective folder. 🌿

   ```bash
   
   git checkout -b add-new-question
   
   ```




# Contribution Rules 🤍

⭐ Follow these steps to add your question.

1. Go to index.html
2. Copy paste the question template code to modify it.
3. Before add your question please check the last updated file then add question no. accordingly. 
4. Add any question related to js or WebDev > set only four options 

'''

        <!-- Copy and paste the following template for each new quiz question -->
        <!--next Question -->
        <!-- add your question according to the given format and also options are set accordingly-->
        
        
        <div class="question">
            <p>6. ----insert your Question here -----</p>
            <div class="option">
                <input type="radio" name="q6" id="" value="A" checked>
                <label for="">your_option1</label>
            </div>
            <div class="option">
                <input type="radio" name="q6" id="" value="B">
                <label for="">your_option2</label>
            </div>
            <div class="option">
                <input type="radio" name="q6" id="" value="C">
                <label for="">your_option3</label>
            </div>
            <div class="option">
                <input type="radio" name="q6" id="" value="D">
                <label for="">your_option4</label>
            </div>
        </div>

'''

4. Save the index.html file.
5. Now goto script.js file
6. just do some change..
7. ex: if you add question 9
    then add correct-option, form.q9.value , ${score}/9! in the given respective place!

'''    

      const correctAnswer = ["D", "B", "C", "B", "D", "A","add-your-correct-option"];
      const form = document.querySelector(".quiz-form");
      const result = document.querySelector(".result");
      const questions=document.querySelectorAll(".question");

      form.addEventListener("submit", event => {
         event.preventDefault();

          let score=0;
          const userAnswers = [form.q1.value, form.q2.value, form.q3.value, form.q4.value, form.q5.value, form.q6.value, form.qno.value];   

          userAnswers.forEach((answer, index) => {
              if(answer === correctAnswer[index]){
              score += 1;
              questions[index].classList.add("correct"); 
              } else {
              questions[index].classList.add("wrong");
          }
          });
    
          scrollTo(0,0);
          result.classList.remove("hide");
          result.querySelector("p").textContent = `You scored ${score}/your_ques_no.!`;
      });

'''

8. **Commit Your Changes:** Commit your changes with a descriptive commit message. 💬

   ```bash
   
   git commit -m "Added new quiz-question"
   
   ```

9. **Push to Your Fork:** Push your changes to your GitHub fork. 🚀

   ```bash
   
   git push origin add-new-question
   
   ```
⭐️You are done go aheaed and make your pull request.

7. **Open a Pull Request:** Submit a Pull Request (PR) to the main repository under the respective category. Include a clear title and description of your changes. 🎯

8. **Review and Merge:** We will review your PR, and if it meets our guidelines, it will be merged into the main repo. 🤝

## Like the Repository! ⭐️

As a first step, please consider giving our repository a ⭐️ to show your support! 🌟

Happy contributing and all the best for hacktoberfest! 💻📚🚗

⭐️Don't make any other changes in the code! If you find any bug or have a feature suggestion, feel free to raise an issue.
