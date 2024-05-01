## Setup
1. Run both applications
2. Explain that your a developer working on stafftools application. You need to make a change to the to a shared component

## Steps (with typical setup)
1. show applications running
1. make a non-breaking change to lib on feature branch. All good :) (change Name to Tree Name in Flashcard component)
1. make breaking change and see that you have to update other team's application :( (change onClick to onTap)
1. stash the breaking change

## Steps (with lazy release)
1. show github action
1. make changes
    1. make package.json changes to main for
        - ./src/index.ts --> ./dist/game.js
        - ./src/index.ts --> ./dist/elements.js
    1. remove tsconfig paths
1. commit and push "fix:" change to lib on feature branch
1. open pull request into main and merge in -> watch action create pull request release
1. look at pr release, especially changelog
1. commit, push, and merge again a breaking change into the same feature branch with "feat!:" change -> see action update pull request release
1. notice the other app isn't broken
1. look at pr release again
1. merge in pr release
1. (talk about how this could also send a slack message)
1. look over the npm package and release notes there
1. run npm install on flashcards application (semver should get the fix but not the breaking change) <-- point out here code visibility con (still 99% though...)
1. intentionally get the updated major version release
1. see your app break and fix it

## If you get stuck
* Make sure your commits are into one of the libraries
* Have to change paths in tsconfig
* It's `npm run dev`
* Did you change your tsconfig paths?

## Other notes
npm install @better-world-dev/game @better-world-dev/elements