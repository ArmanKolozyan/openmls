Fork of [openmls/openmls](https://github.com/openmls/openmls) with one change:

`MlsGroup::process_unverified_message` in `openmls/src/group/mls_group/processing.rs`: visibility changed from `pub(crate)` to `pub`. This allows an external benchmark crate to call `process_unverified_message` directly, which enables measurement of the receiver-side path secret decryption separate from the commit decryption (`unprotect_message`).
