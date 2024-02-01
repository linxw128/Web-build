```js
// Create a function that takes a file URL and a file name as parameters
function downloadFile(fileURL, fileName) {
  // Create a hidden anchor element
  var a = document.createElement("a");
  // Set the href attribute to the file URL
  a.href = fileURL;
  // Set the download attribute to the file name
  a.download = fileName;
  // Append the anchor element to the document body
  document.body.appendChild(a);
  // Trigger a click event on the anchor element
  a.click();
  // Remove the anchor element from the document body
  document.body.removeChild(a);
}

// Call the function with an example file URL and name
downloadFile("https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh", "install.sh");
```
https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh