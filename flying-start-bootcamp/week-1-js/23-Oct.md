
# 23 Oct 2019
## Morning
## Object Oriented Programming

**Object Oriented Programming is often used to represent entities that can be represented in real life**

#### Initialising an object

The class defining an object in js always starts with a constructor (called constructor()) and it uses the dot notation with 'this' to define a new property


``` js
//defining a new class to decribe octocat
class octoCat{
    constructor(){
        this.ears = 2
        this.eyes = "2 cute ones"
        this.tentacles = 8
    }
}
```

:octocat:


#### Reasons for choosing OOP over other functional prgramming
OOP is well suited for creating code that is easier to read by the programmer and other developers and when sections of code are need to be repeated within the program

**Keyboard Shorcuts (VSCode)**

* **cmd + D** Highlight the last character
* **cmd + L** Highlight line-by-line
* **alt + up / down** Move highlighted code up and down the file
* **cmd + shift + F** searches for key term in all files
* **cmd + /** Comment highlighted text

## Afternoon

### MVP

MVP (Minimum Viable Product) is the mindset that involves creating a product that meets the requirements of the client needs with the least amount of effort, where the product is still fully functional

#### TDD for MVP

Use event keywords to help create nested tests for the product:
* --> **GIVEN**
    * --> **WHEN**
       * --> **THEN**
       * --> **AND**


#### Example ####
``` js
        describe('basic game setup', () => {
          describe("GIVEN a word selected with five letters, e.g. 'lunch'", () => {
            let wordSelected
            before(() => {
              wordSelected = 'lunch'
            })
            describe('WHEN a hangman game is initialised using that word', () => {
              let newGame
              before(() => {
                newGame = new Hangman(wordSelected)
              })
              it('THEN the newGame knows that its solution is the selected word', () => {
                expect(newGame.solution).to.equal(wordSelected)
              })
​
              it('AND the current remaining lives is equal to 8', () => {
                expect(newGame.livesRemaining).to.equal(8)
              })
            })
          })
        })

```

### Arrays vs Objects


Arrays make it easier to reference array elements in relation to other elements,
and so it is more relevant when the order/positioning of the things inside matters

Objects are better from when there are many items, because it reduces the computation needed when searching for an item since it can use a since key reference instead of itereating through each element until target is found


## Hangman Testing in OOP

``` html
<!DOCTYPE html>
<html lang="en">
​
<head>
  <meta charset="utf-8" />
  <title>Mocha Tests</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link rel="stylesheet" href="https://unpkg.com/mocha/mocha.css" />
</head>
​
​
<body>
  <!-- Mocha setup -->
  <div id="mocha"></div>
  <script src="https://unpkg.com/chai/chai.js"></script>
  <script src="https://unpkg.com/mocha/mocha.js"></script>
  ​
  <script class="mocha-init">
    mocha.setup('bdd');
    mocha.checkLeaks();
  </script>
  ​
  <!-- Main code -->
  <script>
    // write your code here
    class Hangman {
      constructor(wordChosen) {
        this.solution = wordChosen
        this.livesRemaining = 8
        this.wordInProgress = Array(wordChosen.length).fill('_')
        this.guessedLetters = []
      }
​
      guess(letterGuessed) {
        if (this.isLetterCorrect(letterGuessed)) {
          const indexOfLetterInSolution = this.arrayOfLettersForSolution().findIndex(letter => letter === letterGuessed)
          this.wordInProgress[indexOfLetterInSolution] = letterGuessed
        } else {
          this.livesRemaining = this.livesRemaining - 1
          this.guessedLetters.push('r')
        }
      }
​
      isLetterCorrect(letter) {
        return this.arrayOfLettersForSolution().includes(letter)
      }
​
      isOver() {
        return this.livesRemaining === 0 || this.wordInProgress.join('') === this.solution
      }
​
      arrayOfLettersForSolution() {
        return this.solution.split('')
      }

    }
​
​
​
  </script>
  ​
  <!-- tests -->
  <script>
    const expect = chai.expect
  </script>
  <script>
    // write your tests here
    describe('Hangman game', () => {
      describe('MVP', () => {
        describe('basic game setup', () => {
          describe("GIVEN a word selected with five letters, e.g. 'lunch'", () => {
            let wordSelected
            beforeEach(() => {
              wordSelected = 'lunch'
            })
            describe('WHEN a hangman game is initialised using that word', () => {
              let newGame
              beforeEach(() => {
                newGame = new Hangman(wordSelected)
              })
              it('THEN the newGame knows that its solution is the selected word', () => {
                expect(newGame.solution).to.equal(wordSelected)
              })
​
              it('AND the current remaining lives is equal to 8', () => {
                expect(newGame.livesRemaining).to.equal(8)
              })
​
              it('AND the word in progress is represented by an array with five empty strings', () => {
                expect(newGame.wordInProgress).to.deep.equal(['_', '_', '_', '_', '_'])
              })
​
              it('AND the guessed letters is empty', () => {
                expect(newGame.guessedLetters).to.deep.equal([])
              })
​
              describe("AND a player guesses the letter 'r'", () => {
                beforeEach(() => {
                  newGame.guess('r')
                })
​
                it('THEN the current lives remaining should be equal to 7', () => {
                  expect(newGame.livesRemaining).to.equal(7)
                })
​
                it('AND the word in progress is represented by an array with five empty strings', () => {
                  expect(newGame.wordInProgress).to.deep.equal(['_', '_', '_', '_', '_'])
                })
​
                it('AND the guessed letters has one element, r', () => {
                  expect(newGame.guessedLetters).to.deep.equal(['r'])
                })
​
                describe('AND a player guesses the letter u', () => {
                  beforeEach(() => {
                    newGame.guess('u')
                  })

                  it('THEN the current lives remaining should be equal to 7', () => {
                    expect(newGame.livesRemaining).to.equal(7)
                  })
​
                  describe('AND a player guesses the letters l, n, c, and h', () => {
                    beforeEach(() => {
                      // newGame.guess('l')
                      // newGame.guess('c')
                      // // etc
                      ['l', 'n', 'c', 'h'].forEach(letter => newGame.guess(letter))
                    })
​
                    it('THEN the game is over', () => {
                      console.log(newGame)
                      expect(newGame.isOver()).to.be.true
                    })
                  })
                })
              })
​
              describe('AND a player guesses the letter u', () => {
                it('THEN the current lives remaining should be equal to 8', () => {
                  expect(newGame.livesRemaining).to.equal(8)
                })
              })
            })
          })
        })
      })
​
    })
​
​
  </script>
  <script class="mocha-exec">
    mocha.run();
  </script>
</body>
​
​
</html>
```
