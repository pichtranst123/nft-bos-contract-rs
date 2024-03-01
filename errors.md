c
error[E0428]: the name `NonFungibleTokenReceiver` is defined multiple times
  --> src/lib.rs:61:1
   |
49 | trait NonFungibleTokenReceiver {
   | ------------------------------ previous definition of the trait `NonFungibleTokenReceiver` here
...
61 | pub trait NonFungibleTokenReceiver {
   | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ `NonFungibleTokenReceiver` redefined here
   |
   = note: `NonFungibleTokenReceiver` must be defined only once in the type namespace of this module

error[E0255]: the name `NonFungibleTokenResolver` is defined multiple times
  --> src/lib.rs:72:1
   |
2  |     NonFungibleTokenCore, NonFungibleTokenResolver,
   |                           ------------------------ previous import of the trait `NonFungibleTokenResolver` here
...
72 | trait NonFungibleTokenResolver {
   | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ `NonFungibleTokenResolver` redefined here
   |
   = note: `NonFungibleTokenResolver` must be defined only once in the type namespace of this module
help: you can use `as` to change the binding name of the import
   |
2  |     NonFungibleTokenCore, NonFungibleTokenResolver as OtherNonFungibleTokenResolver,
   |                           ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

error: proc-macro derive panicked
  --> src/lib.rs:82:10
   |
82 | #[derive(BorshDeserialize, BorshSerialize)]
   |          ^^^^^^^^^^^^^^^^
   |
   = help: message: called `Result::unwrap()` on an `Err` value: Could not find `borsh` in `dependencies` or `dev-dependencies` in `/home/pich/contract/nft-bos-rs/Cargo.toml`!

error: proc-macro derive panicked
  --> src/lib.rs:82:28
   |
82 | #[derive(BorshDeserialize, BorshSerialize)]
   |                            ^^^^^^^^^^^^^^
   |
   = help: message: called `Result::unwrap()` on an `Err` value: Could not find `borsh` in `dependencies` or `dev-dependencies` in `/home/pich/contract/nft-bos-rs/Cargo.toml`!

error: proc-macro derive panicked
   --> src/lib.rs:101:10
    |
101 | #[derive(BorshSerialize, BorshDeserialize)]
    |          ^^^^^^^^^^^^^^
    |
    = help: message: called `Result::unwrap()` on an `Err` value: Could not find `borsh` in `dependencies` or `dev-dependencies` in `/home/pich/contract/nft-bos-rs/Cargo.toml`!

error: proc-macro derive panicked
   --> src/lib.rs:101:26
    |
101 | #[derive(BorshSerialize, BorshDeserialize)]
    |                          ^^^^^^^^^^^^^^^^
    |
    = help: message: called `Result::unwrap()` on an `Err` value: Could not find `borsh` in `dependencies` or `dev-dependencies` in `/home/pich/contract/nft-bos-rs/Cargo.toml`!

error: proc-macro derive panicked
   --> src/lib.rs:120:10
    |
120 | #[derive(BorshDeserialize, BorshSerialize, PanicOnDefault)]
    |          ^^^^^^^^^^^^^^^^
    |
    = help: message: called `Result::unwrap()` on an `Err` value: Could not find `borsh` in `dependencies` or `dev-dependencies` in `/home/pich/contract/nft-bos-rs/Cargo.toml`!

error: proc-macro derive panicked
   --> src/lib.rs:120:28
    |
120 | #[derive(BorshDeserialize, BorshSerialize, PanicOnDefault)]
    |                            ^^^^^^^^^^^^^^
    |
    = help: message: called `Result::unwrap()` on an `Err` value: Could not find `borsh` in `dependencies` or `dev-dependencies` in `/home/pich/contract/nft-bos-rs/Cargo.toml`!

error: proc-macro derive panicked
   --> src/lib.rs:130:10
    |
130 | #[derive(BorshDeserialize, BorshSerialize, PanicOnDefault)]
    |          ^^^^^^^^^^^^^^^^
    |
    = help: message: called `Result::unwrap()` on an `Err` value: Could not find `borsh` in `dependencies` or `dev-dependencies` in `/home/pich/contract/nft-bos-rs/Cargo.toml`!

error: proc-macro derive panicked
   --> src/lib.rs:130:28
    |
130 | #[derive(BorshDeserialize, BorshSerialize, PanicOnDefault)]
    |                            ^^^^^^^^^^^^^^
    |
    = help: message: called `Result::unwrap()` on an `Err` value: Could not find `borsh` in `dependencies` or `dev-dependencies` in `/home/pich/contract/nft-bos-rs/Cargo.toml`!

error: proc-macro derive panicked
   --> src/lib.rs:142:10
    |
142 | #[derive(BorshSerialize, BorshStorageKey)]
    |          ^^^^^^^^^^^^^^
    |
    = help: message: called `Result::unwrap()` on an `Err` value: Could not find `borsh` in `dependencies` or `dev-dependencies` in `/home/pich/contract/nft-bos-rs/Cargo.toml`!

error[E0432]: unresolved import `near_sdk::Metadata`
 --> src/lib.rs:9:5
  |
9 | use near_sdk::Metadata;
  |     ^^^^^^^^^^^^^^^^^^ no `Metadata` in the root
  |
help: consider importing one of these items instead
  |
9 | use crate::StorageKey::Metadata;
  |     ~~~~~~~~~~~~~~~~~~~~~~~~~~~
9 | use std::fs::Metadata;
  |     ~~~~~~~~~~~~~~~~~

error[E0432]: unresolved import `near_sdk::Balance`
  --> src/lib.rs:14:71
   |
14 | ...son::json, AccountId, Balance, BorshStorageKey,
   |                          ^^^^^^^ no `Balance` in the root
   |
   = help: consider importing this type alias instead:
           near_contract_standards::fungible_token::Balance

error[E0425]: cannot find function `nft_on_approve` in module `ext_approval_receiver`
    --> src/lib.rs:425:41
     |
425  |             Some(ext_approval_receiver::nft_on_approve(
     |                                         ^^^^^^^^^^^^^^ help: a function with a similar name exists: `nft_approve`
...
1267 | near_contract_standards::impl_non_fungible_token_approval!(Contract, tokens);
     | ---------------------------------------------------------------------------- similarly named function `nft_approve` defined here

error[E0425]: cannot find function `nft_on_transfer` in module `ext_non_fungible_token_receiver`
    --> src/lib.rs:1077:42
     |
158  | #[near_bindgen]
     | --------------- similarly named function `nft_transfer` defined here
...
1077 |         ext_non_fungible_token_receiver::nft_on_transfer(
     |                                          ^^^^^^^^^^^^^^^ help: a function with a similar name exists: `nft_transfer`

error[E0603]: function import `nft_resolve_transfer` is private
    --> src/lib.rs:1086:29
     |
1086 |             .then(ext_self::nft_resolve_transfer(
     |                             ^^^^^^^^^^^^^^^^^^^^ private function import
     |
note: the function import `nft_resolve_transfer` is defined here...
    --> src/lib.rs:71:1
     |
71   | #[ext_contract(ext_self)]
     | ^^^^^^^^^^^^^^^^^^^^^^^^^
note: ...and refers to the function `nft_resolve_transfer` which is defined here
    --> src/lib.rs:1276:1
     |
1276 | #[near_bindgen]
     | ^^^^^^^^^^^^^^^ consider importing it directly
     = note: this error originates in the attribute macro `ext_contract` which comes from the expansion of the attribute macro `near_bindgen` (in Nightly builds, run with -Z macro-backtrace for more info)

warning: use of deprecated macro `near_sdk::setup_alloc`: Allocator is already initialized with the default `wee_alloc` feature set. Please make sure you don't disable default features on the SDK or set the global allocator manually.
   --> src/lib.rs:118:1
    |
118 | near_sdk::setup_alloc!();
    | ^^^^^^^^^^^^^^^^^^^^^
    |
    = note: `#[warn(deprecated)]` on by default

warning: use of deprecated macro `near_contract_standards::impl_non_fungible_token_approval`: implement the near_contract_standards::non_fungible_token::NonFungibleTokenApproval trait manually instead.
    --> src/lib.rs:1267:1
     |
1267 | near_contract_standards::impl_non_fungible_token_approval!(Contract, tokens);
     | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

warning: unused import: `self`
  --> src/lib.rs:10:23
   |
10 | use near_sdk::borsh::{self, BorshDeserialize, BorshSerialize};
   |                       ^^^^
   |
   = note: `#[warn(unused_imports)]` on by default

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
  --> src/lib.rs:12:28
   |
12 | use near_sdk::json_types::{ValidAccountId, U128, U64};
   |                            ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:161:39
    |
161 |     pub fn new_default_meta(owner_id: ValidAccountId, treasury_id: ValidAccoun...
    |                                       ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:161:68
    |
161 | ... ValidAccountId, treasury_id: ValidAccountId) -> Self {
    |                                  ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:179:19
    |
179 |         owner_id: ValidAccountId,
    |                   ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:180:22
    |
180 |         treasury_id: ValidAccountId,
    |                      ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:222:49
    |
222 |     pub fn set_treasury(&mut self, treasury_id: ValidAccountId) {
    |                                                 ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:240:21
    |
240 |         creator_id: ValidAccountId,
    |                     ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:329:22
    |
329 |         receiver_id: ValidAccountId,
    |                      ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:364:22
    |
364 |         receiver_id: ValidAccountId,
    |                      ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:388:21
    |
388 |         account_id: ValidAccountId,
    |                     ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:699:22
    |
699 |         receiver_id: ValidAccountId,
    |                      ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:849:21
    |
849 |         account_id: ValidAccountId
    |                     ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
   --> src/lib.rs:991:22
    |
991 |         receiver_id: ValidAccountId,
    |                      ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
    --> src/lib.rs:1018:22
     |
1018 |         receiver_id: ValidAccountId,
     |                      ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
    --> src/lib.rs:1046:22
     |
1046 |         receiver_id: ValidAccountId,
     |                      ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
    --> src/lib.rs:1124:51
     |
1124 |     pub fn nft_supply_for_owner(self, account_id: ValidAccountId) -> U128 {
     |                                                   ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
    --> src/lib.rs:1136:21
     |
1136 |         account_id: ValidAccountId,
     |                     ^^^^^^^^^^^^^^

warning: use of deprecated type alias `near_sdk::json_types::ValidAccountId`: ValidAccountId is no longer maintained, and AccountId should be used instead
    --> src/lib.rs:1195:22
     |
1195 |         receiver_id: ValidAccountId,
     |                      ^^^^^^^^^^^^^^

warning: use of deprecated function `near_sdk::env::panic`: Use env::panic_str to panic with a message.
   --> src/lib.rs:262:26
    |
262 |                     env::panic("Not valid account_id for royalty".as_bytes());
    |                          ^^^^^

warning: use of deprecated function `near_sdk::env::log`: Use env::log_str for logging messages.
   --> src/lib.rs:300:14
    |
300 |         env::log(
    |              ^^^

warning: use of deprecated function `near_sdk::env::log`: Use env::log_str for logging messages.
   --> src/lib.rs:538:14
    |
538 |         env::log(
    |              ^^^

warning: use of deprecated function `near_sdk::env::log`: Use env::log_str for logging messages.
   --> src/lib.rs:583:14
    |
583 |         env::log(
    |              ^^^

warning: use of deprecated function `near_sdk::env::log`: Use env::log_str for logging messages.
   --> src/lib.rs:622:14
    |
622 |         env::log(
    |              ^^^

warning: use of deprecated function `near_sdk::env::log`: Use env::log_str for logging messages.
  --> src/event.rs:88:24
   |
88 |         near_sdk::env::log(&self.to_string().as_bytes());
   |                        ^^^

error[E0277]: the trait bound `StorageKey: BorshSerialize` is not satisfied
   --> src/lib.rs:142:26
    |
142 | #[derive(BorshSerialize, BorshStorageKey)]
    |                          ^^^^^^^^^^^^^^^ the trait `BorshSerialize` is not implemented for `StorageKey`
    |
    = help: the following other types implement trait `BorshSerialize`:
              bool
              isize
              i8
              i16
              i32
              i64
              i128
              usize
            and 112 others
    = help: see issue #48214
    = note: this error originates in the derive macro `BorshStorageKey` (in Nightly builds, run with -Z macro-backtrace for more info)

Some errors have detailed explanations: E0255, E0277, E0425, E0428, E0432, E0603.
For more information about an error, try `rustc --explain E0255`.
warning: `nft-bos-rs` (lib) generated 27 warnings
error: could not compile `nft-bos-rs` (lib) due to 17 previous errors; 27 warnings emitted