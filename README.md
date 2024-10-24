Currently when running `pnpm update --interactive --latest` in this repo you see:

```
$ pnpm update --interactive --latest    
? Choose which packages to update (Press <space> to select, <a> to toggle all, <i> to invert selection) … 
❯ ○ dependencies
    ○ Package                                                    Current   Target            URL 
    ○ @babel/plugin-transform-logical-assignment-                 7.25.8 ❯ 7.25.9                
    ○ operators                                                                                  
```

The first package is `@babel/plugin-transform-logical-assignment-operators`, and then name is so long it overflows to the second line.

Even worse - the second package is actually for another package (`@babel/preset-react`) but that is completely hidden in the UI. But if you select the row that just says `operators`, then `@babel/preset-react` will be upgraded.
