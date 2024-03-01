error: failed to run custom build command for `secp256k1-sys v0.8.1`

Caused by:
  process didn't exit successfully: `/home/pich/contract/nft-bos-rs/target/release/build/secp256k1-sys-05e2c742e7310f1a/build-script-build` (exit status: 1)
  --- stdout
  TARGET = Some("wasm32-unknown-unknown")
  OPT_LEVEL = Some("z")
  HOST = Some("x86_64-unknown-linux-gnu")
  cargo:rerun-if-env-changed=CC_wasm32-unknown-unknown
  CC_wasm32-unknown-unknown = None
  cargo:rerun-if-env-changed=CC_wasm32_unknown_unknown
  CC_wasm32_unknown_unknown = None
  cargo:rerun-if-env-changed=TARGET_CC
  TARGET_CC = None
  cargo:rerun-if-env-changed=CC
  CC = None
  cargo:rerun-if-env-changed=CRATE_CC_NO_DEFAULTS
  CRATE_CC_NO_DEFAULTS = None
  DEBUG = Some("false")
  cargo:rerun-if-env-changed=CFLAGS_wasm32-unknown-unknown
  CFLAGS_wasm32-unknown-unknown = None
  cargo:rerun-if-env-changed=CFLAGS_wasm32_unknown_unknown
  CFLAGS_wasm32_unknown_unknown = None
  cargo:rerun-if-env-changed=TARGET_CFLAGS
  TARGET_CFLAGS = None
  cargo:rerun-if-env-changed=CFLAGS
  CFLAGS = None
  cargo:rerun-if-env-changed=CC_wasm32-unknown-unknown
  CC_wasm32-unknown-unknown = None
  cargo:rerun-if-env-changed=CC_wasm32_unknown_unknown
  CC_wasm32_unknown_unknown = None
  cargo:rerun-if-env-changed=TARGET_CC
  TARGET_CC = None
  cargo:rerun-if-env-changed=CC
  CC = None
  cargo:rerun-if-env-changed=CRATE_CC_NO_DEFAULTS
  CRATE_CC_NO_DEFAULTS = None
  cargo:rerun-if-env-changed=CFLAGS_wasm32-unknown-unknown
  CFLAGS_wasm32-unknown-unknown = None
  cargo:rerun-if-env-changed=CFLAGS_wasm32_unknown_unknown
  CFLAGS_wasm32_unknown_unknown = None
  cargo:rerun-if-env-changed=TARGET_CFLAGS
  TARGET_CFLAGS = None
  cargo:rerun-if-env-changed=CFLAGS
  CFLAGS = None
  cargo:rerun-if-env-changed=CC_ENABLE_DEBUG_OUTPUT
  cargo:rerun-if-env-changed=CC_wasm32-unknown-unknown
  CC_wasm32-unknown-unknown = None
  cargo:rerun-if-env-changed=CC_wasm32_unknown_unknown
  CC_wasm32_unknown_unknown = None
  cargo:rerun-if-env-changed=TARGET_CC
  TARGET_CC = None
  cargo:rerun-if-env-changed=CC
  CC = None
  cargo:rerun-if-env-changed=CRATE_CC_NO_DEFAULTS
  CRATE_CC_NO_DEFAULTS = None
  cargo:rerun-if-env-changed=CFLAGS_wasm32-unknown-unknown
  CFLAGS_wasm32-unknown-unknown = None
  cargo:rerun-if-env-changed=CFLAGS_wasm32_unknown_unknown
  CFLAGS_wasm32_unknown_unknown = None
  cargo:rerun-if-env-changed=TARGET_CFLAGS
  TARGET_CFLAGS = None
  cargo:rerun-if-env-changed=CFLAGS
  CFLAGS = None

  --- stderr


  error occurred: Failed to find tool. Is `clang` installed?