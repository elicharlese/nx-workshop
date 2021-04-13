### 🧲 Lab 20 Alternative - Mock Store

###### ⏰ Estimated time: 5 minutes

#### 🏋️‍♀️ Steps :

For now, our `store` project has no API when it is deployed. Hence, it is only displaying the header.

1. If you removed your `fake-api/index.ts` from the `store`, let's [re-add it](https://github.com/nrwl/nx-workshop/blob/master/examples/lab2/apps/store/src/fake-api/index.ts)

2. Import it in your `apps/store/src/app/app.component.ts`

   <details>
   <summary>🐳 Hint</summary>

   ```typescript
   import { getAllGames } from '../fake-api/index';
   //....
   games = getAllGames();
   ```
   
   ```html
   <bg-hoard-header [title]="title"></bg-hoard-header>
   <div class="container">
      <div class="games-layout">
        <mat-card
          class="game-card"
          *ngFor="let game of games" <---- HERE
   ```
   </details>

6. Build and deploy your `store` project. Your deployed version should now be showing some games.
  
    ⚠️ Displaying game details will still not work. We can fix that later. 

    <img src="./lab20_result.png" width="500" alt="screenshot of lab20 result">

---

[➡️ Next lab ➡️](../lab21-alt/LAB.md)