## About You.
1. Introduce yourself.
               

               Hello! My name is Athulya A, and I am a passionate software developer specializing in building dynamic and responsive web and mobile applications using modern JavaScript frameworks. With a strong focus on React, Next.js, and React Native, I love creating user-friendly interfaces that provide seamless experiences across different platforms. I have 3.8 yr experience in Web Development.

Skills & Expertise:
React: I have extensive experience in developing complex user interfaces using React. I utilize React’s component-based architecture to create reusable UI components and manage state effectively with hooks and context.

Next.js: I leverage Next.js to build server-side rendered (SSR) and static site generated (SSG) applications. This allows me to optimize performance and improve SEO for the applications I develop. I also enjoy working with API routes in Next.js for backend functionality.

React Native: I develop cross-platform mobile applications using React Native, enabling me to create native-like experiences for both iOS and Android devices. My approach focuses on performance optimization and utilizing native modules for enhanced functionality.

Frontend Development: I am skilled in HTML, CSS, and JavaScript, and I’m familiar with various CSS frameworks such as Bootstrap and Tailwind CSS. I emphasize responsive design and accessibility to ensure that applications are user-friendly and inclusive.

Version Control & Collaboration: I use Git for version control and am comfortable collaborating with teams using platforms like GitHub and GitLab. I understand the importance of code quality and maintainability and adhere to best practices in coding.

I’m always eager to learn and keep up with the latest trends in technology, and I enjoy solving complex problems with creative solutions. Whether working on a personal project or collaborating with a team, I strive to deliver high-quality results and continuously improve my skills.

Feel free to connect with me if you’d like to discuss a project, share insights, or collaborate!

Feel free to modify this introduction better to reflect your personality, background, and specific skills!

2. Do you own a personal computer?
   Yes

3. Describe your development environment. (Your OS, IDE, Editor and Config manager if any)


    Operating System:
I primarily work on macOS, which provides a robust environment for development, especially when working with JavaScript frameworks like React and Next.js. I also have experience with Windows and Linux (Ubuntu), allowing me to adapt to different environments as needed.

Integrated Development Environment (IDE):
For most of my projects, I use Visual Studio Code (VS Code) as my primary IDE. Its lightweight nature, combined with powerful extensions, makes it an excellent choice for JavaScript development. I appreciate features like IntelliSense, integrated terminal, and Git support, which enhance my productivity.

Text Editor:
While I primarily use VS Code, I occasionally utilize Sublime Text for quick edits and prototyping due to its speed and simplicity.

## Social Profile
1. Your StackOverflow Profile url.
https://stackoverflow.com/users/16067073/athulya

               
2. Personal website, blog or something you want us to see.
https://www.linkedin.com/in/athulyaa97/

https://97athulya23.wixsite.com/athulya97


## The real stuff.
1. Which all programming languages are installed on your system.
      Node js
2. Write a function that takes a number and returns a list of its digits in an array.
function getDigits(num) {
    // Convert the number to a string, split it into individual characters,
    // and then map those characters back to numbers
    return num.toString().split('').map(Number);
}

// Example usage:
const number = 12345;
const digits = getDigits(number);
console.log(digits); // Output: [1, 2, 3, 4, 5]


3. Remove duplicates of an array and returning an array of only unique elements
function removeDuplicates(arr) {
    return [...new Set(arr)];
}

// Example usage:
const arrayWithDuplicates = [1, 2, 2, 3, 4, 4, 5];
const uniqueArray = removeDuplicates(arrayWithDuplicates);
console.log(uniqueArray); // Output: [1, 2, 3, 4, 5]

4. Write function that translates a text to Pig Latin and back. English is translated to Pig Latin by taking the first letter of every word, moving it to the end of the word and adding ‘ay’. “The quick brown fox” becomes “Hetay uickqay rownbay oxfay”.

        function toPigLatin(text) {
    return text.split(' ').map(word => {
        const firstLetter = word.charAt(0);
        const pigLatinWord = word.slice(1) + firstLetter + 'ay';
        return pigLatinWord.charAt(0).toUpperCase() + pigLatinWord.slice(1);
    }).join(' ');
}

// Example usage:
const englishText = "The quick brown fox";
const pigLatinText = toPigLatin(englishText);
console.log(pigLatinText); 


5. Write a function that rotates a list by `k` elements. For example [1,2,3,4,5,6] rotated by `2` becomes [3,4,5,6,1,2]. Try solving this without creating a copy of the list. How many swap or move operations do you need?

   function rotateList(arr, k) {
    const n = arr.length;

    // Handle cases where k is greater than the length of the array
    k = k % n;
    if (k === 0) return; // No rotation needed

    // Function to reverse a portion of the array in place
    const reverse = (start, end) => {
        while (start < end) {
            [arr[start], arr[end]] = [arr[end], arr[start]]; // Swap elements
            start++;
            end--;
        }
    };

    // Step 1: Reverse the entire array
    reverse(0, n - 1);

    // Step 2: Reverse the first n - k elements
    reverse(0, n - k - 1);

    // Step 3: Reverse the last k elements
    reverse(n - k, n - 1);
}

// Example usage:
const list = [1, 2, 3, 4, 5, 6];
rotateList(list, 2);
console.log(list); // Output: [3, 4, 5, 6, 1, 2]


Note: It is not mandatory that you answer all the questions. You may leave some behind and create a PR. However maximum questions will earn you maximum points. It is advised that you answer all the puzzles in a language that you are applying for.

### Notes

- [Pig Latin](https://en.wikipedia.org/wiki/Pig_Latin)
- [Fun](http://www.snowcrest.net/donnelly/piglatin.html)
- [Nice Read](https://medium.com/javascript-scene/10-interview-questions-every-javascript-developer-should-know-6fa6bdf5ad95)
