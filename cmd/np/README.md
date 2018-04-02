# naclpipe
NaCL pipe

## ChangeLog
2018-04-01: separating command 'np' and package 'naclpipe', this way package can eventually be reused as "crypto" stream.
            as an io.Reader/Writer interface.
            Starting 'semver' and documenting.
            First version will be 0.1.0
            
2018-03-24: fixing the empty scrypt salt reported by Tom eklof 
            better handling of pipe input.
            the structure has changed as the CSPRNG'ed salt is prefixed to the series of blocks


## Command Install
    go get github.com/unix4fun/naclpipe/cmd/np

## Featuring (because there is always a star in your production..)

* [NaCL ECC 25519] (http://nacl.cr.yp.to/install.html) box/secretbox [Go implementation](https://godoc.org/golang.org/x/crypto/nacl) with AEAD
(using Salsa20 w/ Poly1305 MAC)
* [Scrypt] (http://en.wikipedia.org/wiki/Scrypt) for key stretching
* [SHA-3] (http://en.wikipedia.org/wiki/SHA-3) for NONCE generation
* [Go] (http://golang.org) because I like trying something new and promising.


## Command Usage

    $ echo "proutproutprout" | ./np -k=tagadaa  | ./np -d -k=tagadaa



## Library Usage

    import github.com/unix4fun/naclpipe