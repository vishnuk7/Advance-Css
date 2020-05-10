##### How Css Works 

What Happens to CSS when we load up a webpage?
1. First it load html
2. Then second step is parse HTML line by line
3. Parseing HTML create DOM(Document Object Model)
4. When parseing happen it load the css and it parse the css
5. CSS parseing having two steps
   * Resolve conflicting CSS declarations(cascade)
   * Process final CSS values (converting %,rem,em units into px)
6. Once parsing is done it store tree like structure like DOM and it know as CSSOM(CSS Object Model)
7. DOM + CSSDOM = Render Tree
8. For rendering a page browser use something called **the visual formatting model**