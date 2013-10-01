# hb-epub3

A Harp boilerplate for generating EPUB3 ebooks.

## Get started

1. Install Harp

  This boilerplate is for Harp, the static web server with built-in preprocessing. [Harp](http://harpjs.com) can flatten the preprocessed code—in this case, Jade, Stylus and Markdown—to HTML & CSS. Then, it can easily be turned into a `.epub` file.

  Install Harp globally:

  ```ssh
  sudo npm install harp -g
  ```

2. Clone this boilerplate

  Next, clone this boilerplate.

  ```ssh
  git clone https://github.com/kennethormandy/hb-epub3 ebook
  cd ebook
  ```

3. Compile your `.epub` using Harp

  Then, using the OS’ `zip` command, the generated folder can be compressed into a valid `.epub` file.

  ```ssh
  harp compile . ebook; cd ebook; zip -X0 \../ebook.epub mimetype; zip -rDX9 \../ebook.epub * -x "*.DS_Store" -x mimetype; cd \../
  ```

  Now, if you want to make some quick changes and just view them in the browser, you can serve a locally:

  ```ssh
  harp server
  # The content is now visible at http://harp.nu:9000/OPS/book/content
  ```

## Todo

- [ ] Properly support everything listed in `harp.json`
- [ ] Further improve typographic defaults
- [ ] Automatically use any Markdown in `_content/`
- [ ] Restore text sizing in iBooks
- [ ] Run against accessibility checklist

## Works Cited

* [Candide by Voltaire, via Project Gutenberg](http://www.gutenberg.org/ebooks/19942)
* [reitermarkus/epub3-boilerplate](https://github.com/reitermarkus/epub3-boilerplate)
* [javierarce/epub-boilerplate](https://github.com/javierarce/epub-boilerplate)
* [Saolee/epub-boilerplate](https://github.com/Saolee/epub-boilerplate)
* [mattharrison/epub-css-starter-kit](https://github.com/mattharrison/epub-css-starter-kit)