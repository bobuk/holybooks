# Bible for Machines

The purpose of this project is quite simple - I was converting different versions of the `Old` and `New Testament` into machine-readable format for my own needs, and then decided to share the result with you. The directory structure is extremely simple:
Language -> Canon -> Book -> Version.

In the language folder there is also index.json, which has an obvious structure

I try to stick to standard naming for books and versions whenever possible.
To find, for example, the `Synodal translation` of `Genesis` from the `Old Testament`, look in the directory *RU / OT / GEN / SYNO.json*

The structure of the files themselves is a little less obvious:

```
{
    "version": "version or translation identifier",
    "ID": "full identifier of book, canon and translation",
    "name": "book name",
    "text": [
        {
            "ID": "chapter identifier",
            "name": "chapter name",
            "text": [
                {"ID": "paragraph identifier", "text": "paragraph text"},
                ...
            ]
        },
        ...  
    ]
}
```

If you find any flaws or problems in the files, or want to upload other variants (or translations) - send pull requests, as usual.

### TODO

  * We clearly need a file describing the version (meta information and which books are included in it)
  * Need to proofread all files by eye
  * We need more books and options, pull requests are welcome
