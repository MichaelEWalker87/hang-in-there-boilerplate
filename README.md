# Hang In There

A boilerplate repo.

## Set Up

1. One teammate: fork this repository
2. Go to settings and turn on GitHub Pages for this repository
3. All teammates: clone down this repository
4. `cd` into the repository
5. Run `open index.html` to view it in the browser

## Progression

### Iteration 0 - Main Page

![screenshot of main page showing poster](/readme-imgs/homepage.png)

#### When the page loads, we should see a poster with a randomly selected image, title, and quote.

  - Add `querySelectors` for all classes on `index.html`.
  - Create a `loadRandom` function that changes `innerText` of `title` and `quote` and `src` of `image`.
  - Create `loadRandom` function to pass `titles`, `quotes`, and `images` arrays through the `getRandomIndex` function.
  - ![On load random](//media.giphy.com/media/llrPijEOL6KzZY0vqJ/giphy.gif)

#### Every time the user clicks the Show Random Poster button, a new random poster is displayed.

  - Create an  `eventListener` on click for the `showRandom` variable that takes in a second argument of `loadRandom`
  - ![On click random](//media.giphy.com/media/QXPiCJKnGTuTVqSDl6/source.gif)


### Iteration 1 - Switching Views

Form page:
![screenshot of form](/readme-imgs/form.png)

Saved posters page (once working with extra saved posters):
![screenshot of saved posters page](/readme-imgs/saved.png)

#### When a user clicks the "Make Your Own Poster" button, we should see the form, and the main poster should be hidden

  - Create a function that shows the the form by removing the `hidden` class from `form` and adding the `hidden` class on `poster`.
  - Create an `eventListener` on click for the `showForm` variable that takes in a second argument of `loadForm`.
  - ![On click form](//media.giphy.com/media/dyXjIjgfMfh2H32XO4/giphy.gif)

#### When a user clicks the "View Saved Posters" button, we should see the saved posters area, and the main poster should be hidden

  - Create a function that shows the saved poster page by removing the `hidden` class from `savedPosters` and adding the `hidden` class on `poster`.
  - Create an `eventListener` on click for the `showSaved` variable that takes in a second argument of `loadSaved`.
  - ![On click saved](//media.giphy.com/media/hr3GBPAXmiTJLg5EzJ/source.gif)

#### When a user clicks the "Nevermind, take me back!" or "Back to Main" buttons, we should only see the main poster section

  - Create a function that returns back to the main page from the saved page by adding the `hidden` class from `savedPoster` and removing the `hidden` class on `poster`. Then Create another function that does the same thing from the form page but this time adding the `hidden` class to `showMain`.
  - Create an `eventListener` on click for the `backToMain` variable that takes in a second argument of `loadMain`
  - Create an `eventListener` on click for the `showMain` variable that takes in a second argument of `nvmTakeMeBack`.


#### In summary: Be able to switch between the three views (main poster, form, and saved posters) on the correct button clicks
  - ![On click saved](https://giphy.com/gifs/WRiLrR4odmtOfzEs1l)

_Hint: go check out the HTML and CSS files to see how the form and saved posters sections are being hidden in the first place_

## Iteration 2 - Creating a New Poster

Form being filled out:
![screenshot of form](/readme-imgs/form.png)

Once poster is saved:
![screenshot of result](/readme-imgs/form-result.png)

- On the new poster form view, users should be able to fill out the three input fields and then hit the save button
- When the save button is clicked, several things will happen:
  - Save the submitted data into the respective arrays (image URL into the images array, etc) so that future random posters can use the user-created data
  - Use the values from the inputs to create a new instance of our Poster class
  - Change back to the main poster view (hiding the form view again)
  - Display the newly created poster image, title, and quote in the main view

## Iteration 3 - Saving & Viewing Posters

Saved posters view:
![screenshot of saved posters section](/readme-imgs/saved.png)

- When a user clicks the "Save This Poster" button, the current main poster will be added to the `savedPosters` array.
- If a user clicks the "Save This Poster" more than once on a single poster, it will still only be saved once (no duplicates)
- When a user clicks the "Show Saved Posters" button, we should see the saved posters section
- All the posters in the `savedPosters` array should be displayed in the saved posters grid section

## Iteration 4 - Deleting Saved Posters

- From the saved posters view, if a user double clicks a saved poster, it will be deleted

_Hint: How will you update the data model to achieve this?_

## Optional Extensions - Gettin' fancy

Here's a list of possible extensions to implement - but **ONLY IF** your team has completed all the previous iterations **AND** have cleaned up your code to make it DRYer and more readable.

You are welcome to add your own extensions. Be sure they are thoughtful in terms of UX/UI, and that they do not break any prior functionality.

- Implement data validation and error handling into the form (disable button, provide error messages if data entered is not correct, etc)
- In the main poster view, allow users to click each piece of the poster (image, title, quote) to update just that piece with another random item from the appropriate array
- When a user single clicks a saved poster, create a modal to view it larger
- Allow users to drag and drop saved posters into whatever order they want them to appear


Project spec & rubric can be found [here](https://frontend.turing.io/projects/module-1/hang-in-there.html)
