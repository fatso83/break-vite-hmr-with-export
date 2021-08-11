# Demo: breaking HMR when adding an export

HMR did not seem to work at all when introducing Vite to our own app and it 
took a full day of debugging to find out what exactly caused it. 

This repo is the most minimal example that will demonstrate exactly
the kind of code that broke HMR in our own app, which is a quite
innocent looking `export` statement at the second-highest root node.

## Repro
1. `npx vite`
2. Try changing anything in `App.tsx` and verify that a full reload happens
3. Uncomment [the line with `export const u = 12`](https://github.com/fatso83/break-vite-hmr-with-export/blob/h%C3%B8vding/src/App.tsx#L7) (and the next line)
