   Compiling nft-bos-rs v0.1.0 (/home/pich/contract/nft-bos-rs)
error[E0428]: the name `NonFungibleTokenReceiver` is defined multiple times
  --> src/lib.rs:63:1
   |
51 | trait NonFungibleTokenReceiver {
   | ------------------------------ previous definition of the trait `NonFungibleTokenReceiver` here
...
63 | pub trait NonFungibleTokenReceiver {
   | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ `NonFungibleTokenReceiver` redefined here
   |
   = note: `NonFungibleTokenReceiver` must be defined only once in the type namespace of this module

error[E0255]: the name `NonFungibleTokenResolver` is defined multiple times
  --> src/lib.rs:74:1
   |
3  |     NonFungibleTokenCore, NonFungibleTokenResolver,
   |                           ------------------------ previous import of the trait `NonFungibleTokenResolver` here
...
74 | trait NonFungibleTokenResolver {
   | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ `NonFungibleTokenResolver` redefined here
   |
   = note: `NonFungibleTokenResolver` must be defined only once in the type namespace of this module
help: you can use `as` to change the binding name of the import
   |
3  |     NonFungibleTokenCore, NonFungibleTokenResolver as OtherNonFungibleTokenResolver,
   |                           ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

error[E0425]: cannot find function `nft_on_approve` in module `ext_approval_receiver`
    --> src/lib.rs:427:41
     |
427  |             Some(ext_approval_receiver::nft_on_approve(
     |                                         ^^^^^^^^^^^^^^ help: a function with a similar name exists: `nft_approve`
...
1269 | near_contract_standards::impl_non_fungible_token_approval!(Contract, tokens);
     | ---------------------------------------------------------------------------- similarly named function `nft_approve` defined here

error[E0425]: cannot find crate `from` in the list of imported crates
   --> src/lib.rs:896:38
    |
896 |             Some(p) => return Some(::from(p)),
    |                                      ^^^^ not found in the list of imported crates

error[E0425]: cannot find function `nft_on_transfer` in module `ext_non_fungible_token_receiver`
    --> src/lib.rs:1079:42
     |
160  | #[near_bindgen]
     | --------------- similarly named function `nft_transfer` defined here
...
1079 |         ext_non_fungible_token_receiver::nft_on_transfer(
     |                                          ^^^^^^^^^^^^^^^ help: a function with a similar name exists: `nft_transfer`

error[E0603]: function import `nft_resolve_transfer` is private
    --> src/lib.rs:1088:29
     |
1088 |             .then(ext_self::nft_resolve_transfer(
     |                             ^^^^^^^^^^^^^^^^^^^^ private function import
     |
note: the function import `nft_resolve_transfer` is defined here...
    --> src/lib.rs:73:1
     |
73   | #[ext_contract(ext_self)]
     | ^^^^^^^^^^^^^^^^^^^^^^^^^
note: ...and refers to the function `nft_resolve_transfer` which is defined here
    --> src/lib.rs:1278:1
     |
1278 | #[near_bindgen]
     | ^^^^^^^^^^^^^^^ consider importing it directly
     = note: this error originates in the attribute macro `ext_contract` which comes from the expansion of the attribute macro `near_bindgen` (in Nightly builds, run with -Z macro-backtrace for more info)

warning: use of deprecated macro `near_sdk::setup_alloc`: Allocator is already initialized with the default `wee_alloc` feature set. Please make sure you don't disable default features on the SDK or set the global allocator manually.
   --> src/lib.rs:120:1
    |
120 | near_sdk::setup_alloc!();
    | ^^^^^^^^^^^^^^^^^^^^^
    |
    = note: `#[warn(deprecated)]` on by default

warning: use of deprecated macro `near_contract_standards::impl_non_fungible_token_approval`: implement the near_contract_standards::non_fungible_token::NonFungibleTokenApproval trait manually instead.
    --> src/lib.rs:1269:1
     |
1269 | near_contract_standards::impl_non_fungible_token_approval!(Contract, tokens);
     | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

warning: unused import: `crate::StorageKey::Metadata`
  --> src/lib.rs:10:5
   |
10 | use crate::StorageKey::Metadata;
   |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^
   |
   = note: `#[warn(unused_imports)]` on by default

warning: unused import: `near_sdk::env::account_balance`
  --> src/lib.rs:21:5
   |
21 | use near_sdk::env::account_balance;
   |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

warning: unnecessary parentheses around function argument
   --> src/lib.rs:872:33
    |
872 |                 Some(x) => Some((x)),
    |                                 ^ ^
    |
    = note: `#[warn(unused_parens)]` on by default
help: remove these parentheses
    |
872 -                 Some(x) => Some((x)),
872 +                 Some(x) => Some(x),
    |

warning: unnecessary parentheses around method argument
    --> src/lib.rs:1133:24
     |
1133 |             .unwrap_or((0))
     |                        ^ ^
     |
help: remove these parentheses
     |
1133 -             .unwrap_or((0))
1133 +             .unwrap_or(0)
     |

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
  --> src/lib.rs:13:28
   |
13 | use near_sdk::json_types::{ValidAccountId,U128,U64};
   |                            ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:163:39
    |
163 |     pub fn new_default_meta(owner_id: ValidAccountId, treasury_id: ValidAccountId) -> Self {
    |                                       ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:163:68
    |
163 |     pub fn new_default_meta(owner_id: ValidAccountId, treasury_id: ValidAccountId) -> Self {
    |                                                                    ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:181:19
    |
181 |         owner_id: ValidAccountId,
    |                   ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:182:22
    |
182 |         treasury_id: ValidAccountId,
    |                      ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:224:49
    |
224 |     pub fn set_treasury(&mut self, treasury_id: ValidAccountId) {
    |                                                 ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:242:21
    |
242 |         creator_id: ValidAccountId,
    |                     ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:331:22
    |
331 |         receiver_id: ValidAccountId,
    |                      ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:366:22
    |
366 |         receiver_id: ValidAccountId,
    |                      ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:390:21
    |
390 |         account_id: ValidAccountId,
    |                     ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:701:22
    |
701 |         receiver_id: ValidAccountId,
    |                      ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:851:21
    |
851 |         account_id: ValidAccountId
    |                     ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:993:22
    |
993 |         receiver_id: ValidAccountId,
    |                      ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
    --> src/lib.rs:1020:22
     |
1020 |         receiver_id: ValidAccountId,
     |                      ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
    --> src/lib.rs:1048:22
     |
1048 |         receiver_id: ValidAccountId,
     |                      ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
    --> src/lib.rs:1126:51
     |
1126 |     pub fn nft_supply_for_owner(self, account_id: ValidAccountId) -> u128 {
     |                                                   ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
    --> src/lib.rs:1138:21
     |
1138 |         account_id: ValidAccountId,
     |                     ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
    --> src/lib.rs:1197:22
     |
1197 |         receiver_id: ValidAccountId,
     |                      ^^^^^^^^^^^^^^

warning: use of deprecated function `near_sdk::env::panic`: Use env::panic_str to panic with a message.
   --> src/lib.rs:264:26
    |
264 |                     env::panic("Not valid account_id for royalty".as_bytes());
    |                          ^^^^^

warning: use of deprecated function `near_sdk::env::log`: Use env::log_str for logging messages.
   --> src/lib.rs:302:14
    |
302 |         env::log(
    |              ^^^

warning: use of deprecated function `near_sdk::env::log`: Use env::log_str for logging messages.
   --> src/lib.rs:540:14
    |
540 |         env::log(
    |              ^^^

warning: use of deprecated function `near_sdk::env::log`: Use env::log_str for logging messages.
   --> src/lib.rs:585:14
    |
585 |         env::log(
    |              ^^^

warning: use of deprecated function `near_sdk::env::log`: Use env::log_str for logging messages.
   --> src/lib.rs:624:14
    |
624 |         env::log(
    |              ^^^

warning: use of deprecated function `near_sdk::env::log`: Use env::log_str for logging messages.
  --> src/event.rs:88:24
   |
88 |         near_sdk::env::log(&self.to_string().as_bytes());
   |                        ^^^

error[E0107]: enum takes 1 generic argument but 0 generic arguments were supplied
   --> src/lib.rs:601:83
    |
601 |     pub fn nft_set_series_price(&mut self, token_series_id: TokenSeriesId, price: Option<>) -> Option<> {
    |                                                                                   ^^^^^^ expected 1 generic argument
    |
note: enum defined here, with 1 generic parameter: `T`
   --> /home/pich/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/src/rust/library/core/src/option.rs:563:10
    |
563 | pub enum Option<T> {
    |          ^^^^^^ -
help: add missing generic argument
    |
601 |     pub fn nft_set_series_price(&mut self, token_series_id: TokenSeriesId, price: Option<T>) -> Option<> {
    |                                                                                          +

error[E0107]: enum takes 1 generic argument but 0 generic arguments were supplied
   --> src/lib.rs:601:96
    |
601 |     pub fn nft_set_series_price(&mut self, token_series_id: TokenSeriesId, price: Option<>) -> Option<> {
    |                                                                                                ^^^^^^ expected 1 generic argument
    |
note: enum defined here, with 1 generic parameter: `T`
   --> /home/pich/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/src/rust/library/core/src/option.rs:563:10
    |
563 | pub enum Option<T> {
    |          ^^^^^^ -
help: add missing generic argument
    |
601 |     pub fn nft_set_series_price(&mut self, token_series_id: TokenSeriesId, price: Option<>) -> Option<T> {
    |                                                                                                       +

Some errors have detailed explanations: E0107, E0255, E0425, E0428, E0603.
For more information about an error, try `rustc --explain E0107`.
warning: `nft-bos-rs` (lib) generated 30 warnings
error: could not compile `nft-bos-rs` (lib) due to 8 previous errors; 30 warnings emitted
