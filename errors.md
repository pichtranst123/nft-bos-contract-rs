pich@pich-VirtualBox:~/contract/nft-bos-rs$ cargo build --target wasm32-unknown-unknown --release
   Compiling getrandom v0.2.12
error: the wasm*-unknown-unknown targets are not supported by default, you may need to enable the "js" feature. For more information see: https://docs.rs/getrandom/#webassembly-support
   --> /home/pich/.cargo/registry/src/index.crates.io-6f17d22bba15001f/getrandom-0.2.12/src/lib.rs:291:9
    |
291 | /         compile_error!("the wasm*-unknown-unknown targets are not supported by \
292 | |                         default, you may need to enable the \"js\" feature. \
293 | |                         For more information see: \
294 | |                         https://docs.rs/getrandom/#webassembly-support");
    | |________________________________________________________________________^

error[E0433]: failed to resolve: use of undeclared crate or module `imp`
   --> /home/pich/.cargo/registry/src/index.crates.io-6f17d22bba15001f/getrandom-0.2.12/src/lib.rs:347:9
    |
347 |         imp::getrandom_inner(dest)?;
    |         ^^^ use of undeclared crate or module `imp`

For more information about this error, try `rustc --explain E0433`.
error: could not compile `getrandom` (lib) due to 2 previous errors