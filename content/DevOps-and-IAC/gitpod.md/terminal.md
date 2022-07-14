-- Performing Test IS_WEXTRA_SUPPORTED
    CC builtin/multi-pack-index.o
    CC builtin/mv.o
    CC builtin/name-rev.o
    CC builtin/notes.o
-- Performing Test IS_WEXTRA_SUPPORTED - Success
-- Performing Test IS_WDOCUMENTATION_SUPPORTED
    CC builtin/pack-objects.o
    CC builtin/pack-redundant.o
    CC builtin/pack-refs.o
-- Performing Test IS_WDOCUMENTATION_SUPPORTED - Failed
-- Performing Test IS_WNO_DOCUMENTATION_DEPRECATED_SYNC_SUPPORTED
    CC builtin/patch-id.o
    CC builtin/prune-packed.o
    CC builtin/prune.o
-- Performing Test IS_WNO_DOCUMENTATION_DEPRECATED_SYNC_SUPPORTED - Success
-- Performing Test IS_WNO_MISSING_FIELD_INITIALIZERS_SUPPORTED
    CC builtin/pull.o
    CC builtin/push.o
    CC builtin/range-diff.o
    CC builtin/read-tree.o
    CC builtin/rebase.o
    CC builtin/receive-pack.o
    CC builtin/reflog.o
-- Performing Test IS_WNO_MISSING_FIELD_INITIALIZERS_SUPPORTED - Success
    CC builtin/remote-ext.o
-- Performing Test IS_WSTRICT_ALIASING_SUPPORTED
    CC builtin/remote-fd.o
    CC builtin/remote.o
    CC builtin/repack.o
-- Performing Test IS_WSTRICT_ALIASING_SUPPORTED - Success
-- Performing Test IS_WSTRICT_PROTOTYPES_SUPPORTED
    CC builtin/replace.o
    CC builtin/rerere.o
    CC builtin/reset.o
    CC builtin/rev-list.o
    CC builtin/rev-parse.o
-- Performing Test IS_WSTRICT_PROTOTYPES_SUPPORTED - Success
-- Performing Test IS_WDECLARATION_AFTER_STATEMENT_SUPPORTED
    CC builtin/revert.o
    CC builtin/rm.o
    CC builtin/send-pack.o
    CC builtin/shortlog.o
-- Performing Test IS_WDECLARATION_AFTER_STATEMENT_SUPPORTED - Success
-- Performing Test IS_WSHIFT_COUNT_OVERFLOW_SUPPORTED
    CC builtin/show-branch.o
    CC builtin/show-index.o
    CC builtin/show-ref.o
    CC builtin/sparse-checkout.o
    CC builtin/stash.o
    CC builtin/stripspace.o
-- Performing Test IS_WSHIFT_COUNT_OVERFLOW_SUPPORTED - Success
-- Performing Test IS_WUNUSED_CONST_VARIABLE_SUPPORTED
    CC builtin/submodule--helper.o
    CC builtin/symbolic-ref.o
    CC builtin/tag.o
    CC builtin/unpack-file.o
    CC builtin/unpack-objects.o
-- Performing Test IS_WUNUSED_CONST_VARIABLE_SUPPORTED - Success
-- Performing Test IS_WUNUSED_FUNCTION_SUPPORTED
    CC builtin/update-index.o
    CC builtin/update-ref.o
    CC builtin/update-server-info.o
    CC builtin/upload-archive.o
    CC builtin/upload-pack.o
    CC builtin/var.o
    CC builtin/verify-commit.o
-- Performing Test IS_WUNUSED_FUNCTION_SUPPORTED - Success
-- Performing Test IS_WINT_CONVERSION_SUPPORTED
    CC builtin/verify-pack.o
    CC builtin/verify-tag.o
    CC builtin/worktree.o
    CC builtin/write-tree.o
    CC common-main.o
    CC abspath.o
    CC add-interactive.o
    CC add-patch.o
    CC advice.o
-- Performing Test IS_WINT_CONVERSION_SUPPORTED - Success
-- Performing Test IS_WC11_EXTENSIONS_SUPPORTED
    CC alias.o
    CC alloc.o
    CC apply.o
-- Performing Test IS_WC11_EXTENSIONS_SUPPORTED - Failed
-- Performing Test IS_WC99_C11_COMPAT_SUPPORTED
    CC archive-tar.o
    CC archive-zip.o
    CC archive.o
    CC attr.o
    CC base85.o
-- Performing Test IS_WC99_C11_COMPAT_SUPPORTED - Success
-- Performing Test IS_WFORMAT_SUPPORTED
    CC bisect.o
    CC blame.o
    CC blob.o
-- Performing Test IS_WFORMAT_SUPPORTED - Success
-- Performing Test IS_WFORMAT_SECURITY_SUPPORTED
    CC bloom.o
    CC branch.o
    CC bulk-checkin.o
    CC bundle.o
    CC cache-tree.o
    CC cbtree.o
    CC chdir-notify.o
-- Performing Test IS_WFORMAT_SECURITY_SUPPORTED - Success
-- Performing Test IS_WMISSING_DECLARATIONS_SUPPORTED
    CC checkout.o
    CC chunk-format.o
    CC color.o
    CC combine-diff.o
    CC column.o
    CC commit-graph.o
    CC commit-reach.o
    CC commit.o
-- Performing Test IS_WMISSING_DECLARATIONS_SUPPORTED - Success
    CC compat/obstack.o
    CC compat/terminal.o
    CC compat/zlib-uncompress2.o
-- Checking prototype qsort_r for HAVE_QSORT_R_BSD - False
    CC config.o
    CC connect.o
    CC connected.o
    CC convert.o
    CC copy.o
    CC credential.o
    CC csum-file.o
    CC ctype.o
-- Checking prototype qsort_r for HAVE_QSORT_R_GNU - True
-- Looking for qsort_s
    CC date.o
    CC decorate.o
    CC delta-islands.o
-- Looking for qsort_s - not found
-- Looking for clock_gettime in rt
    CC diff-delta.o
    CC diff-merges.o
    CC diff-lib.o
    CC diff-no-index.o
    CC diff.o
    CC diffcore-break.o
-- Looking for clock_gettime in rt - found
    CC diffcore-delta.o
    CC diffcore-order.o
    CC diffcore-pickaxe.o
    CC diffcore-rename.o
    CC diffcore-rotate.o
    CC dir-iterator.o
-- Found OpenSSL: /usr/lib/x86_64-linux-gnu/libcrypto.so (found version "1.1.1f")  
-- Found PCRE: /usr/lib/x86_64-linux-gnu/libpcre.so  
-- Looking for dirent.h
    CC dir.o
    CC editor.o
    CC entry.o
    CC environment.o
    CC ewah/bitmap.o
    CC ewah/ewah_bitmap.o
    CC ewah/ewah_io.o
    CC ewah/ewah_rlw.o
-- Looking for dirent.h - found
-- Looking for stdint.h
    CC exec-cmd.o
    CC fetch-negotiator.o
    CC fetch-pack.o
    CC fmt-merge-msg.o
-- Looking for stdint.h - found
-- Looking for inttypes.h
    CC fsck.o
    CC fsmonitor.o
    CC fsmonitor-ipc.o
    CC fsmonitor-settings.o
    CC gettext.o
    CC gpg-interface.o
    CC graph.o
-- Looking for inttypes.h - found
-- Looking for sys/stat.h
    CC grep.o
    CC hash-lookup.o
    CC hashmap.o
    GEN command-list.h
    CC hex.o
    CC hook.o
    CC ident.o
    CC json-writer.o
    CC kwset.o
-- Looking for sys/stat.h - found
-- Looking for sys/types.h
    CC levenshtein.o
    CC line-log.o
    CC line-range.o
    CC linear-assignment.o
    CC list-objects-filter-options.o
    CC list-objects-filter.o
-- Looking for sys/types.h - found
-- Looking for unistd.h
    CC list-objects.o
    CC ll-merge.o
    CC lockfile.o
    CC log-tree.o
    CC ls-refs.o
    CC mailinfo.o
-- Looking for unistd.h - found
-- Looking for windows.h
    CC mailmap.o
-- Looking for windows.h - not found
-- Looking for bcopy
    CC match-trees.o
    CC mem-pool.o
    CC merge-blobs.o
    CC merge-ort.o
    CC merge-ort-wrappers.o
    CC merge-recursive.o
    CC merge.o
    CC mergesort.o
    CC midx.o
    CC name-hash.o
-- Looking for bcopy - found
-- Looking for memmove
    CC negotiator/default.o
    CC negotiator/noop.o
    CC negotiator/skipping.o
    CC notes-cache.o
    CC notes-utils.o
    CC notes-merge.o
    CC notes.o
    CC object-file.o
-- Looking for memmove - found
-- Looking for strerror
    CC object-name.o
    CC object.o
    CC oid-array.o
    CC oidmap.o
    CC oidset.o
-- Looking for strerror - found
-- Looking for strtoll
    CC oidtree.o
    CC pack-bitmap-write.o
    CC pack-bitmap.o
    CC pack-check.o
    CC pack-mtimes.o
-- Looking for strtoll - found
-- Looking for strtoq
    CC pack-objects.o
    CC pack-revindex.o
    CC pack-write.o
-- Looking for strtoq - found
-- Looking for _strtoi64
    CC packfile.o
    CC pager.o
    CC parallel-checkout.o
    CC parse-options-cb.o
    CC parse-options.o
    CC patch-delta.o
-- Looking for _strtoi64 - not found
-- Looking for stddef.h
    CC patch-ids.o
    CC path.o
    CC pathspec.o
    CC pkt-line.o
-- Looking for stddef.h - found
-- Check size of long long
    CC preload-index.o
    CC pretty.o
    CC prio-queue.o
    CC progress.o
    CC promisor-remote.o
    CC prompt.o
-- Check size of long long - done
-- Check size of unsigned long long
    CC protocol.o
    CC protocol-caps.o
    CC prune-packed.o
    CC quote.o
    CC range-diff.o
    CC reachable.o
    CC read-cache.o
    CC rebase-interactive.o
-- Check size of unsigned long long - done
-- Performing Test IS_WNO_UNUSED_FUNCTION_SUPPORTED
    CC rebase.o
    CC ref-filter.o
    CC reflog-walk.o
    CC reflog.o
    CC refs.o
    CC refs/debug.o
    CC refs/files-backend.o
    CC refs/iterator.o
    CC refs/packed-backend.o
-- Performing Test IS_WNO_UNUSED_FUNCTION_SUPPORTED - Success
-- Performing Test IS_WNO_IMPLICIT_FALLTHROUGH_SUPPORTED
    CC refs/ref-cache.o
    CC refspec.o
    CC remote.o
    CC replace-object.o
    CC repo-settings.o
    CC repository.o
-- Performing Test IS_WNO_IMPLICIT_FALLTHROUGH_SUPPORTED - Success
-- http-parser version 2 was not found or disabled; using bundled 3rd-party sources.
-- Performing Test IS_WIMPLICIT_FALLTHROUGH_1_SUPPORTED
    CC rerere.o
    CC reset.o
    CC resolve-undo.o
    CC revision.o
    CC run-command.o
    CC send-pack.o
    CC sequencer.o
-- Performing Test IS_WIMPLICIT_FALLTHROUGH_1_SUPPORTED - Success
-- LIBSSH2 not found. Set CMAKE_PREFIX_PATH if it is installed outside of the default search path.
    CC serve.o
    CC server-info.o
-- Found GSSAPI: /usr/lib/x86_64-linux-gnu/libgssapi_krb5.so;/usr/lib/x86_64-linux-gnu/libkrb5.so;/usr/lib/x86_64-linux-gnu/libk5crypto.so;/usr/lib/x86_64-linux-gnu/libcom_err.so  
-- Enabled features:
 * nanoseconds, whether to use sub-second file mtimes and ctimes
 * futimens, futimens support
 * threadsafe, threadsafe support
 * SHA, using CollisionDetection
 * regex, using bundled PCRE
 * http-parser, http-parser support (bundled)
 * zlib, using bundled zlib

-- Disabled features:
 * debugpool, debug pool allocator
 * debugalloc, debug strict allocators
 * debugopen, path validation in open
 * tracing, tracing support
 * HTTPS
 * SSH, SSH transport support
 * ntlmclient, NTLM authentication support for Unix
 * SPNEGO, SPNEGO authentication support
 * iconv, iconv encoding conversion support

-- Configuring done
    CC setup.o
-- Generating done
    CC shallow.o
-- Build files have been written to: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build
    CC sideband.o
make[3]: Entering directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
make[3]: warning: -j16 forced in submake: resetting jobserver mode.
    CC sigchain.o
make[4]: Entering directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
make[5]: Entering directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
make[5]: Entering directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
make[5]: Entering directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
make[5]: Entering directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
Scanning dependencies of target http-parser
make[5]: Leaving directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
make[5]: Entering directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
    CC sparse-index.o
Scanning dependencies of target zlib
make[5]: Leaving directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
[  1%] Building C object deps/http-parser/CMakeFiles/http-parser.dir/http_parser.c.o
make[5]: Entering directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
Scanning dependencies of target pcre
make[5]: Leaving directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
make[5]: Entering directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
    CC split-index.o
[  1%] Building C object deps/zlib/CMakeFiles/zlib.dir/adler32.c.o
[  2%] Building C object deps/zlib/CMakeFiles/zlib.dir/crc32.c.o
[  2%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_byte_order.c.o
[  3%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_chartables.c.o
[  3%] Building C object deps/zlib/CMakeFiles/zlib.dir/deflate.c.o
[  3%] Building C object deps/zlib/CMakeFiles/zlib.dir/inffast.c.o
[  4%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_config.c.o
[  5%] Building C object deps/zlib/CMakeFiles/zlib.dir/infback.c.o
[  5%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_compile.c.o
[  5%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_dfa_exec.c.o
[  6%] Building C object deps/zlib/CMakeFiles/zlib.dir/inflate.c.o
[  7%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_exec.c.o
[  7%] Building C object deps/zlib/CMakeFiles/zlib.dir/inftrees.c.o
    CC stable-qsort.o
[  7%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_fullinfo.c.o
[  8%] Building C object deps/zlib/CMakeFiles/zlib.dir/trees.c.o
    CC strbuf.o
    CC streaming.o
    CC string-list.o
[  9%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_get.c.o
    CC strmap.o
[ 10%] Building C object deps/zlib/CMakeFiles/zlib.dir/zutil.c.o
    CC strvec.o
[ 10%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_globals.c.o
    CC sub-process.o
[ 11%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_jit_compile.c.o
[ 12%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_newline.c.o
[ 12%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_maketables.c.o
    CC submodule-config.o
    CC submodule.o
    CC symlinks.o
[ 12%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_ord2utf8.c.o
[ 13%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_refcount.c.o
[ 13%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_string_utils.c.o
    CC tag.o
    CC tempfile.o
[ 13%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_tables.c.o
[ 14%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_study.c.o
make[5]: Leaving directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
Scanning dependencies of target git2internal
make[5]: Leaving directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
    CC thread-utils.o
[ 16%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_ucd.c.o
[ 16%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_version.c.o
[ 16%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_valid_utf8.c.o
[ 16%] Built target http-parser
    CC tmp-objdir.o
[ 16%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcre_xclass.c.o
[ 17%] Building C object deps/pcre/CMakeFiles/pcre.dir/pcreposix.c.o
make[5]: Entering directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
[ 18%] Building C object src/CMakeFiles/git2internal.dir/hash/sha1/collisiondetect.c.o
[ 18%] Building C object src/CMakeFiles/git2internal.dir/hash/sha1/sha1dc/sha1.c.o
    CC trace.o
[ 18%] Building C object src/CMakeFiles/git2internal.dir/unix/map.c.o
[ 19%] Building C object src/CMakeFiles/git2internal.dir/hash/sha1/sha1dc/ubc_check.c.o
[ 20%] Building C object src/CMakeFiles/git2internal.dir/unix/realpath.c.o
    CC trace2.o
[ 20%] Building C object src/CMakeFiles/git2internal.dir/alloc.c.o
[ 20%] Building C object src/CMakeFiles/git2internal.dir/allocators/stdalloc.c.o
[ 21%] Building C object src/CMakeFiles/git2internal.dir/allocators/failalloc.c.o
    CC trace2/tr2_cfg.o
[ 21%] Building C object src/CMakeFiles/git2internal.dir/annotated_commit.c.o
    CC trace2/tr2_cmd_name.o
[ 22%] Building C object src/CMakeFiles/git2internal.dir/apply.c.o
[ 22%] Building C object src/CMakeFiles/git2internal.dir/attr.c.o
[ 23%] Building C object src/CMakeFiles/git2internal.dir/allocators/win32_leakcheck.c.o
make[5]: Leaving directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
[ 23%] Built target zlib
    CC trace2/tr2_dst.o
    CC trace2/tr2_sid.o
[ 24%] Building C object src/CMakeFiles/git2internal.dir/attr_file.c.o
    CC trace2/tr2_sysenv.o
[ 24%] Building C object src/CMakeFiles/git2internal.dir/attrcache.c.o
[ 25%] Building C object src/CMakeFiles/git2internal.dir/blame.c.o
    CC trace2/tr2_tbuf.o
    CC trace2/tr2_tgt_event.o
[ 25%] Building C object src/CMakeFiles/git2internal.dir/blame_git.c.o
    CC trace2/tr2_tgt_normal.o
[ 25%] Building C object src/CMakeFiles/git2internal.dir/branch.c.o
[ 26%] Building C object src/CMakeFiles/git2internal.dir/blob.c.o
    CC trace2/tr2_tgt_perf.o
    CC trace2/tr2_tls.o
    CC trailer.o
    CC transport-helper.o
[ 27%] Building C object src/CMakeFiles/git2internal.dir/buffer.c.o
    CC transport.o
[ 27%] Building C object src/CMakeFiles/git2internal.dir/cache.c.o
[ 28%] Building C object src/CMakeFiles/git2internal.dir/checkout.c.o
    CC tree-diff.o
[ 29%] Building C object src/CMakeFiles/git2internal.dir/clone.c.o
[ 29%] Building C object src/CMakeFiles/git2internal.dir/cherrypick.c.o
    CC tree-walk.o
    CC tree.o
[ 29%] Building C object src/CMakeFiles/git2internal.dir/commit.c.o
    CC unpack-trees.o
[ 30%] Building C object src/CMakeFiles/git2internal.dir/commit_graph.c.o
[ 30%] Building C object src/CMakeFiles/git2internal.dir/commit_list.c.o
    CC upload-pack.o
[ 31%] Building C object src/CMakeFiles/git2internal.dir/config.c.o
[ 31%] Building C object src/CMakeFiles/git2internal.dir/config_cache.c.o
[ 32%] Building C object src/CMakeFiles/git2internal.dir/config_entries.c.o
[ 32%] Building C object src/CMakeFiles/git2internal.dir/config_file.c.o
    CC url.o
    CC urlmatch.o
    CC usage.o
[ 33%] Building C object src/CMakeFiles/git2internal.dir/config_mem.c.o
[ 33%] Building C object src/CMakeFiles/git2internal.dir/config_parse.c.o
    CC userdiff.o
[ 33%] Building C object src/CMakeFiles/git2internal.dir/crlf.c.o
[ 34%] Building C object src/CMakeFiles/git2internal.dir/config_snapshot.c.o
[ 35%] Building C object src/CMakeFiles/git2internal.dir/date.c.o
[ 35%] Building C object src/CMakeFiles/git2internal.dir/delta.c.o
    CC utf8.o
[ 36%] Building C object src/CMakeFiles/git2internal.dir/describe.c.o
    CC varint.o
[ 36%] Building C object src/CMakeFiles/git2internal.dir/diff.c.o
[ 37%] Building C object src/CMakeFiles/git2internal.dir/diff_driver.c.o
[ 37%] Building C object src/CMakeFiles/git2internal.dir/diff_file.c.o
[ 38%] Building C object src/CMakeFiles/git2internal.dir/diff_generate.c.o
[ 38%] Building C object src/CMakeFiles/git2internal.dir/diff_parse.c.o
    CC versioncmp.o
[ 38%] Building C object src/CMakeFiles/git2internal.dir/diff_stats.c.o
[ 39%] Building C object src/CMakeFiles/git2internal.dir/diff_print.c.o
    CC walker.o
    CC wildmatch.o
    CC worktree.o
[ 40%] Building C object src/CMakeFiles/git2internal.dir/diff_tform.c.o
[ 40%] Building C object src/CMakeFiles/git2internal.dir/diff_xdiff.c.o
    CC wrapper.o
    CC write-or-die.o
[ 41%] Building C object src/CMakeFiles/git2internal.dir/email.c.o
    CC ws.o
[ 41%] Building C object src/CMakeFiles/git2internal.dir/errors.c.o
[ 42%] Building C object src/CMakeFiles/git2internal.dir/fetch.c.o
[ 43%] Building C object src/CMakeFiles/git2internal.dir/filebuf.c.o
    CC wt-status.o
[ 43%] Building C object src/CMakeFiles/git2internal.dir/filter.c.o
[ 43%] Building C object src/CMakeFiles/git2internal.dir/fetchhead.c.o
    CC xdiff-interface.o
    CC zlib.o
    CC unix-socket.o
[ 44%] Building C object src/CMakeFiles/git2internal.dir/futils.c.o
[ 44%] Building C object src/CMakeFiles/git2internal.dir/graph.c.o
[ 45%] Building C object src/CMakeFiles/git2internal.dir/hash.c.o
    CC unix-stream-server.o
    CC compat/simple-ipc/ipc-shared.o
[ 45%] Building C object src/CMakeFiles/git2internal.dir/hashsig.c.o
[ 46%] Building C object src/CMakeFiles/git2internal.dir/ident.c.o
[ 46%] Building C object src/CMakeFiles/git2internal.dir/idxmap.c.o
    CC compat/simple-ipc/ipc-unix-socket.o
[ 47%] Building C object src/CMakeFiles/git2internal.dir/ignore.c.o
    CC sha1dc_git.o
    CC sha1dc/sha1.o
    CC sha1dc/ubc_check.o
[ 47%] Building C object src/CMakeFiles/git2internal.dir/index.c.o
[ 48%] Building C object src/CMakeFiles/git2internal.dir/indexer.c.o
    CC sha256/block/sha256.o
[ 49%] Building C object src/CMakeFiles/git2internal.dir/libgit2.c.o
[ 49%] Building C object src/CMakeFiles/git2internal.dir/iterator.c.o
    CC compat/linux/procinfo.o
[ 49%] Building C object src/CMakeFiles/git2internal.dir/mailmap.c.o
    CC compat/fopen.o
[ 50%] Building C object src/CMakeFiles/git2internal.dir/merge.c.o
[ 50%] Building C object src/CMakeFiles/git2internal.dir/merge_driver.c.o
    CC compat/strlcpy.o
    CC compat/qsort_s.o
[ 51%] Building C object src/CMakeFiles/git2internal.dir/merge_file.c.o
[ 51%] Building C object src/CMakeFiles/git2internal.dir/message.c.o
    CC xdiff/xdiffi.o
[ 52%] Building C object src/CMakeFiles/git2internal.dir/midx.c.o
[ 52%] Building C object src/CMakeFiles/git2internal.dir/mwindow.c.o
[ 53%] Building C object src/CMakeFiles/git2internal.dir/net.c.o
    CC xdiff/xemit.o
    CC xdiff/xhistogram.o
[ 53%] Building C object src/CMakeFiles/git2internal.dir/netops.c.o
    CC xdiff/xmerge.o
[ 54%] Building C object src/CMakeFiles/git2internal.dir/notes.c.o
[ 54%] Building C object src/CMakeFiles/git2internal.dir/object.c.o
    CC xdiff/xpatience.o
[ 55%] Building C object src/CMakeFiles/git2internal.dir/object_api.c.o
    CC xdiff/xprepare.o
[ 55%] Building C object src/CMakeFiles/git2internal.dir/odb.c.o
[ 55%] Building C object src/CMakeFiles/git2internal.dir/odb_mempack.c.o
[ 56%] Building C object src/CMakeFiles/git2internal.dir/odb_pack.c.o
[ 56%] Building C object src/CMakeFiles/git2internal.dir/offmap.c.o
[ 57%] Building C object src/CMakeFiles/git2internal.dir/odb_loose.c.o
    CC xdiff/xutils.o
    CC reftable/basics.o
    CC reftable/error.o
    CC reftable/block.o
    CC reftable/blocksource.o
    CC reftable/iter.o
    CC reftable/publicbasics.o
[ 58%] Building C object src/CMakeFiles/git2internal.dir/oid.c.o
    CC reftable/merged.o
    CC reftable/pq.o
    CC reftable/reader.o
[ 58%] Building C object src/CMakeFiles/git2internal.dir/oidarray.c.o
    CC reftable/record.o
[ 59%] Building C object src/CMakeFiles/git2internal.dir/oidmap.c.o
[ 59%] Building C object src/CMakeFiles/git2internal.dir/pack-objects.c.o
[ 60%] Building C object src/CMakeFiles/git2internal.dir/pack.c.o
    CC reftable/refname.o
    CC reftable/generic.o
    CC reftable/stack.o
[ 60%] Building C object src/CMakeFiles/git2internal.dir/parse.c.o
    CC reftable/tree.o
[ 61%] Building C object src/CMakeFiles/git2internal.dir/patch.c.o
    CC reftable/writer.o
    CC remote-curl.o
[ 61%] Building C object src/CMakeFiles/git2internal.dir/patch_generate.c.o
[ 62%] Building C object src/CMakeFiles/git2internal.dir/patch_parse.c.o
[ 62%] Building C object src/CMakeFiles/git2internal.dir/path.c.o
[ 62%] Building C object src/CMakeFiles/git2internal.dir/pool.c.o
[ 63%] Building C object src/CMakeFiles/git2internal.dir/pathspec.c.o
    CC http.o
    CC http-walker.o
[ 64%] Building C object src/CMakeFiles/git2internal.dir/posix.c.o
    CC http-backend.o
    CC git.o
[ 64%] Building C object src/CMakeFiles/git2internal.dir/pqueue.c.o
    CC builtin/bugreport.o
    CC builtin/help.o
[ 65%] Building C object src/CMakeFiles/git2internal.dir/proxy.c.o
[ 65%] Building C object src/CMakeFiles/git2internal.dir/push.c.o
[ 66%] Building C object src/CMakeFiles/git2internal.dir/rebase.c.o
[ 67%] Building C object src/CMakeFiles/git2internal.dir/reader.c.o
    CC help.o
[ 67%] Building C object src/CMakeFiles/git2internal.dir/refdb.c.o
[ 67%] Building C object src/CMakeFiles/git2internal.dir/reflog.c.o
[ 68%] Building C object src/CMakeFiles/git2internal.dir/refdb_fs.c.o
    CC version.o
[ 69%] Building C object src/CMakeFiles/git2internal.dir/refs.c.o
[ 69%] Building C object src/CMakeFiles/git2internal.dir/refspec.c.o
[ 70%] Building C object src/CMakeFiles/git2internal.dir/regexp.c.o
    AR xdiff/lib.a
[ 70%] Building C object src/CMakeFiles/git2internal.dir/remote.c.o
[ 71%] Building C object src/CMakeFiles/git2internal.dir/repository.c.o
[ 71%] Building C object src/CMakeFiles/git2internal.dir/reset.c.o
[ 72%] Building C object src/CMakeFiles/git2internal.dir/revert.c.o
[ 72%] Building C object src/CMakeFiles/git2internal.dir/revparse.c.o
    AR libgit.a
/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/source/src/path.c: In function ‘git_path_owner_is’:
/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/source/src/path.c:2229:38: warning: ‘sudo_uid’ may be used uninitialized in this function [-Wmaybe-uninitialized]
 2227 |  if ((owner_type & GIT_PATH_OWNER_RUNNING_SUDO) != 0 &&
      |      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 2228 |      euid == 0 &&
      |      ~~~~~~~~~~~~                     
 2229 |      sudo_uid_lookup(&sudo_uid) == 0 &&
      |      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^~
 2230 |      st.st_uid == sudo_uid) {
      |      ~~~~~~~~~~~~~~~~~~~~~            
[ 72%] Building C object src/CMakeFiles/git2internal.dir/runtime.c.o
/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/source/src/path.c: At top level:
cc1: warning: unrecognized command line option ‘-Wno-documentation-deprecated-sync’
[ 73%] Building C object src/CMakeFiles/git2internal.dir/revwalk.c.o
[ 74%] Building C object src/CMakeFiles/git2internal.dir/signature.c.o
[ 75%] Building C object src/CMakeFiles/git2internal.dir/stash.c.o
[ 75%] Building C object src/CMakeFiles/git2internal.dir/sortedcache.c.o
[ 75%] Building C object src/CMakeFiles/git2internal.dir/status.c.o
make[5]: Leaving directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
[ 76%] Building C object src/CMakeFiles/git2internal.dir/strarray.c.o
    AR reftable/libreftable.a
[ 77%] Building C object src/CMakeFiles/git2internal.dir/streams/openssl.c.o
[ 77%] Building C object src/CMakeFiles/git2internal.dir/streams/mbedtls.c.o
[ 77%] Built target pcre
    LINK git
    LINK git-http-backend
[ 77%] Building C object src/CMakeFiles/git2internal.dir/streams/openssl_dynamic.c.o
[ 78%] Building C object src/CMakeFiles/git2internal.dir/streams/openssl_legacy.c.o
[ 78%] Building C object src/CMakeFiles/git2internal.dir/streams/registry.c.o
[ 79%] Building C object src/CMakeFiles/git2internal.dir/streams/socket.c.o
[ 79%] Building C object src/CMakeFiles/git2internal.dir/streams/stransport.c.o
[ 80%] Building C object src/CMakeFiles/git2internal.dir/streams/tls.c.o
[ 80%] Building C object src/CMakeFiles/git2internal.dir/strmap.c.o
[ 81%] Building C object src/CMakeFiles/git2internal.dir/submodule.c.o
[ 81%] Building C object src/CMakeFiles/git2internal.dir/sysdir.c.o
[ 82%] Building C object src/CMakeFiles/git2internal.dir/tag.c.o
[ 82%] Building C object src/CMakeFiles/git2internal.dir/thread.c.o
[ 83%] Building C object src/CMakeFiles/git2internal.dir/threadstate.c.o
[ 83%] Building C object src/CMakeFiles/git2internal.dir/trace.c.o
[ 83%] Building C object src/CMakeFiles/git2internal.dir/transports/auth.c.o
[ 84%] Building C object src/CMakeFiles/git2internal.dir/transport.c.o
[ 84%] Building C object src/CMakeFiles/git2internal.dir/transaction.c.o
[ 85%] Building C object src/CMakeFiles/git2internal.dir/trailer.c.o
[ 86%] Building C object src/CMakeFiles/git2internal.dir/transports/auth_negotiate.c.o
[ 86%] Building C object src/CMakeFiles/git2internal.dir/transports/auth_ntlm.c.o
[ 87%] Building C object src/CMakeFiles/git2internal.dir/transports/credential.c.o
[ 87%] Building C object src/CMakeFiles/git2internal.dir/transports/http.c.o
[ 87%] Building C object src/CMakeFiles/git2internal.dir/transports/credential_helpers.c.o
[ 88%] Building C object src/CMakeFiles/git2internal.dir/transports/git.c.o
    LINK git-remote-http
[ 89%] Building C object src/CMakeFiles/git2internal.dir/transports/httpclient.c.o
[ 89%] Building C object src/CMakeFiles/git2internal.dir/transports/local.c.o
[ 90%] Building C object src/CMakeFiles/git2internal.dir/transports/smart.c.o
[ 91%] Building C object src/CMakeFiles/git2internal.dir/transports/smart_protocol.c.o
[ 91%] Building C object src/CMakeFiles/git2internal.dir/transports/smart_pkt.c.o
[ 91%] Building C object src/CMakeFiles/git2internal.dir/transports/ssh.c.o
[ 91%] Building C object src/CMakeFiles/git2internal.dir/tree-cache.c.o
[ 92%] Building C object src/CMakeFiles/git2internal.dir/transports/winhttp.c.o
[ 93%] Building C object src/CMakeFiles/git2internal.dir/tree.c.o
[ 93%] Building C object src/CMakeFiles/git2internal.dir/tsort.c.o
[ 93%] Building C object src/CMakeFiles/git2internal.dir/util.c.o
[ 94%] Building C object src/CMakeFiles/git2internal.dir/utf8.c.o
[ 95%] Building C object src/CMakeFiles/git2internal.dir/varint.c.o
[ 95%] Building C object src/CMakeFiles/git2internal.dir/vector.c.o
[ 96%] Building C object src/CMakeFiles/git2internal.dir/wildmatch.c.o
[ 96%] Building C object src/CMakeFiles/git2internal.dir/worktree.c.o
[ 97%] Building C object src/CMakeFiles/git2internal.dir/xdiff/xdiffi.c.o
[ 97%] Building C object src/CMakeFiles/git2internal.dir/xdiff/xemit.c.o
[ 98%] Building C object src/CMakeFiles/git2internal.dir/xdiff/xhistogram.c.o
[ 98%] Building C object src/CMakeFiles/git2internal.dir/xdiff/xmerge.c.o
[ 98%] Building C object src/CMakeFiles/git2internal.dir/xdiff/xprepare.c.o
[ 99%] Building C object src/CMakeFiles/git2internal.dir/xdiff/xpatience.c.o
[100%] Building C object src/CMakeFiles/git2internal.dir/xdiff/xutils.c.o
make[3]: Leaving directory '/workspace/gitlab-development-kit/gitaly/_build/deps/git-v2.37.1.gl1'
[100%] Building C object src/CMakeFiles/git2internal.dir/zstream.c.o
make[5]: Leaving directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
[100%] Built target git2internal
make[5]: Entering directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
Scanning dependencies of target git2
make[5]: Leaving directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
make[5]: Entering directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
[100%] Linking C static library ../libgit2.a
make[5]: Leaving directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
[100%] Built target git2
make[4]: Leaving directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
Install the project...
-- Install configuration: "Release"
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/lib/pkgconfig/libgit2.pc
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/lib/libgit2.a
-- Up-to-date: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/annotated_commit.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/apply.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/attr.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/blame.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/blob.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/branch.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/buffer.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/cert.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/checkout.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/cherrypick.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/clone.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/commit.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/common.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/config.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/cred_helpers.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/credential.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/credential_helpers.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/deprecated.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/describe.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/diff.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/email.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/errors.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/filter.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/global.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/graph.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/ignore.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/index.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/indexer.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/mailmap.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/merge.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/message.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/net.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/notes.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/object.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/odb.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/odb_backend.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/oid.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/oidarray.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/pack.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/patch.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/pathspec.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/proxy.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/rebase.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/refdb.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/reflog.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/refs.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/refspec.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/remote.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/repository.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/reset.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/revert.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/revparse.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/revwalk.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/signature.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/stash.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/status.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/stdint.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/strarray.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/submodule.h
-- Up-to-date: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/alloc.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/commit.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/commit_graph.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/config.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/cred.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/credential.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/diff.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/email.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/filter.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/hashsig.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/index.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/mempack.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/merge.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/midx.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/odb_backend.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/openssl.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/path.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/refdb_backend.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/reflog.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/refs.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/repository.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/stream.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/sys/transport.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/tag.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/trace.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/transaction.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/transport.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/tree.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/types.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/version.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2/worktree.h
-- Installing: /workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/install/include/git2.h
make[3]: Leaving directory '/workspace/gitlab-development-kit/gitaly/_build/deps/libgit2/build'
go install -a github.com/libgit2/git2go/v33
make[2]: Leaving directory '/workspace/gitlab-development-kit/gitaly'

--------------------------------------------------------------------------------
Installing gitlab-org/gitaly Ruby gems
--------------------------------------------------------------------------------
ok: run: /workspace/gitlab-development-kit/services/postgresql: (pid 55284) 0s, normally down
ok: run: /workspace/gitlab-development-kit/services/redis: (pid 55285) 0s, normally down
praefect sql-migrate: all migrations are up
make[1]: Leaving directory '/workspace/gitlab-development-kit'

--------------------------------------------------------------------------------
Ensuring necessary data services are running
--------------------------------------------------------------------------------
ok: run: /workspace/gitlab-development-kit/services/postgresql: (pid 55284) 2s, normally down
ok: run: /workspace/gitlab-development-kit/services/redis: (pid 55285) 2s, normally down
ok: run: /workspace/gitlab-development-kit/services/praefect: (pid 55744) 0s, normally down
ok: run: /workspace/gitlab-development-kit/services/praefect-gitaly-0: (pid 55745) 0s, normally down
ok: run: /workspace/gitlab-development-kit/services/postgresql: (pid 55284) 3s, normally down
ok: run: /workspace/gitlab-development-kit/services/redis: (pid 55285) 3s, normally down
gitlabhq_development exists, nothing to do here.
gitlabhq_development_ci exists, nothing to do here.

--------------------------------------------------------------------------------
Updating gitlab-org/gitlab-metrics-exporter
--------------------------------------------------------------------------------
Successfully fetched and checked out 'main' for 'gitlab-metrics-exporter/'
Successfully pulled (--ff-only) for 'gitlab-metrics-exporter/'

--------------------------------------------------------------------------------
Building gitlab-org/gitlab-metrics-exporter version main
--------------------------------------------------------------------------------

> Reconfigured as of 2022-07-14 21:07:34. Took 397 second(s).
Thu 14 Jul 2022 09:07:34 PM UTC – Running DB migrations
make[1]: Entering directory '/workspace/gitlab-development-kit'
make[2]: Entering directory '/workspace/gitlab-development-kit'

--------------------------------------------------------------------------------
Updating gitlab-org/gitaly to 76dabc8174f7978025f48adcfab0a19c85416531
--------------------------------------------------------------------------------
✅️ Successfully fetched and checked out '76dabc8174f7978025f48adcfab0a19c85416531' for 'gitaly/'
make[2]: Leaving directory '/workspace/gitlab-development-kit'

--------------------------------------------------------------------------------
Building gitlab-org/gitaly 76dabc8174f7978025f48adcfab0a19c85416531
--------------------------------------------------------------------------------
make[2]: Entering directory '/workspace/gitlab-development-kit/gitaly'
make[2]: Leaving directory '/workspace/gitlab-development-kit/gitaly'

--------------------------------------------------------------------------------
Installing gitlab-org/gitaly Ruby gems
--------------------------------------------------------------------------------
ok: run: /workspace/gitlab-development-kit/services/postgresql: (pid 55284) 28s, normally down
ok: run: /workspace/gitlab-development-kit/services/redis: (pid 55285) 28s, normally down
praefect sql-migrate: all migrations are up
make[1]: Leaving directory '/workspace/gitlab-development-kit'

--------------------------------------------------------------------------------
Ensuring necessary data services are running
--------------------------------------------------------------------------------
ok: run: /workspace/gitlab-development-kit/services/postgresql: (pid 55284) 30s, normally down
ok: run: /workspace/gitlab-development-kit/services/praefect: (pid 55744) 28s, normally down
ok: run: /workspace/gitlab-development-kit/services/praefect-gitaly-0: (pid 65278) 2s, normally down
ok: run: /workspace/gitlab-development-kit/services/redis: (pid 55285) 30s, normally down

--------------------------------------------------------------------------------
Processing gitlab rails DB migrations
--------------------------------------------------------------------------------
main: == 20220706191627 AddEncryptedErrorTrackingAccessToken: migrating =============
main: -- add_column(:application_settings, :error_tracking_access_token_encrypted, :text, {:if_not_exists=>true})
main:    -> 0.1989s
main: -- transaction_open?()
main:    -> 0.0000s
main: -- current_schema()
main:    -> 0.0005s
main: -- transaction_open?()
main:    -> 0.0000s
main: -- execute("ALTER TABLE application_settings\nADD CONSTRAINT check_5688c70478\nCHECK ( char_length(error_tracking_access_token_encrypted) <= 255 )\nNOT VALID;\n")
main:    -> 0.0045s
main: -- current_schema()
main:    -> 0.0005s
main: -- execute("SET statement_timeout TO 0")
main:    -> 0.0005s
main: -- execute("ALTER TABLE application_settings VALIDATE CONSTRAINT check_5688c70478;")
main:    -> 0.0012s
main: -- execute("RESET statement_timeout")
main:    -> 0.0005s
main: == 20220706191627 AddEncryptedErrorTrackingAccessToken: migrated (0.2343s) ====

ci: == 20220706191627 AddEncryptedErrorTrackingAccessToken: migrating =============
ci: -- add_column(:application_settings, :error_tracking_access_token_encrypted, :text, {:if_not_exists=>true})
ci:    -> 0.1890s
ci: -- transaction_open?()
ci:    -> 0.0000s
ci: -- current_schema()
ci:    -> 0.0020s
ci: -- transaction_open?()
ci:    -> 0.0000s
ci: -- execute("ALTER TABLE application_settings\nADD CONSTRAINT check_5688c70478\nCHECK ( char_length(error_tracking_access_token_encrypted) <= 255 )\nNOT VALID;\n")
ci:    -> 0.0063s
ci: -- current_schema()
ci:    -> 0.0006s
ci: -- execute("SET statement_timeout TO 0")
ci:    -> 0.0010s
ci: -- execute("ALTER TABLE application_settings VALIDATE CONSTRAINT check_5688c70478;")
ci:    -> 0.0024s
ci: -- execute("RESET statement_timeout")
ci:    -> 0.0008s
ci: == 20220706191627 AddEncryptedErrorTrackingAccessToken: migrated (0.2198s) ====

Thu 14 Jul 2022 09:08:44 PM UTC – Stopping GDK
ok: down: /workspace/gitlab-development-kit/services/gitlab-workhorse: 80s
ok: down: /workspace/gitlab-development-kit/services/rails-background-jobs: 80s
ok: down: /workspace/gitlab-development-kit/services/rails-web: 80s
ok: down: /workspace/gitlab-development-kit/services/sshd: 80s
ok: down: /workspace/gitlab-development-kit/services/webpack: 80s
ok: down: /workspace/gitlab-development-kit/services/praefect: 1s
ok: down: /workspace/gitlab-development-kit/services/praefect-gitaly-0: 0s
ok: down: /workspace/gitlab-development-kit/services/redis: 0s
ok: down: /workspace/gitlab-development-kit/services/postgresql: 1s
Thu 14 Jul 2022 09:08:46 PM UTC – GDK stopped
gitpod-start done
ℹ️  A backup of 'gdk.yml' has been made at '.backups/gdk.yml.20220714210846'.
✅️ 'gitlab.rails.hostname' is now set to '3000-shaolabgroup-gitlab-v7i309tykzc.ws-us54.gitpod.io' (previously '127.0.0.1').
ℹ️  Don't forget to run 'gdk reconfigure'
⚠️  WARNING: 'gitlab.rails.port' is already set to '443'
⚠️  WARNING: 'gitlab.rails.https.enabled' is already set to 'true'
ℹ️  A backup of 'gdk.yml' has been made at '.backups/gdk.yml.20220714210848'.
✅️ 'webpack.host' is now set to '127.0.0.1' (previously '3000-shaolabgroup-gitlab-v7i309tykzc.ws-us54.gitpod.io').
ℹ️  Don't forget to run 'gdk reconfigure'
⚠️  WARNING: 'webpack.static' is already set to 'false'
⚠️  WARNING: 'webpack.live_reload' is already set to 'false'
Thu 14 Jul 2022 09:08:49 PM UTC – Reconfiguring GDK
make[1]: Entering directory '/workspace/gitlab-development-kit'
make[1]: Leaving directory '/workspace/gitlab-development-kit'

-------------------------------------------------------------------------------------------------------------
@@ -29,7 +29,7 @@ production: &base
   ## GitLab settings
   gitlab:
     ## Web server settings (note: host is the FQDN, do not include http://)
-    host: 127.0.0.1
+    host: 3000-shaolabgroup-gitlab-v7i309tykzc.ws-us54.gitpod.io
     port: 443
     https: true
 

-------------------------------------------------------------------------------------------------------------
'gitlab/config/gitlab.yml' has incoming changes:
WARNING: 'gitlab/config/gitlab.yml' has been overwritten. To recover the previous version, run:

cp -f '/workspace/gitlab-development-kit/.backups/gitlab__config__gitlab.yml.20220714210851' \
'/workspace/gitlab-development-kit/gitlab/config/gitlab.yml'

If you want to protect this file from being overwritten, see:
https://gitlab.com/gitlab-org/gitlab-development-kit/-/blob/main/doc/configuration.md#overwriting-configuration-files
-------------------------------------------------------------------------------------------------------------

--------------------------------------------------------------------------------
Installing gitlab-org/gitlab Ruby gems
--------------------------------------------------------------------------------

--------------------------------------------------------------------------------
Installing gitlab-org/gitlab Node.js packages
--------------------------------------------------------------------------------

--------------------------------------------------------------------------------
Ensuring GDK managed configuration files are up-to-date
--------------------------------------------------------------------------------

--------------------------------------------------------------------------------
Installing gitlab-org/gitlab-shell Ruby gems
--------------------------------------------------------------------------------

--------------------------------------------------------------------------------
Compiling gitlab/workhorse/gitlab-workhorse
--------------------------------------------------------------------------------

--------------------------------------------------------------------------------
Building gitlab-org/gitaly 76dabc8174f7978025f48adcfab0a19c85416531
--------------------------------------------------------------------------------
make[1]: Entering directory '/workspace/gitlab-development-kit/gitaly'
make[1]: Leaving directory '/workspace/gitlab-development-kit/gitaly'

--------------------------------------------------------------------------------
Installing gitlab-org/gitaly Ruby gems
--------------------------------------------------------------------------------
make[1]: Entering directory '/workspace/gitlab-development-kit'
make[2]: Entering directory '/workspace/gitlab-development-kit'

--------------------------------------------------------------------------------
Updating gitlab-org/gitaly to 76dabc8174f7978025f48adcfab0a19c85416531
--------------------------------------------------------------------------------
Successfully fetched and checked out '76dabc8174f7978025f48adcfab0a19c85416531' for 'gitaly/'
make[2]: Leaving directory '/workspace/gitlab-development-kit'

--------------------------------------------------------------------------------
Building gitlab-org/gitaly 76dabc8174f7978025f48adcfab0a19c85416531
--------------------------------------------------------------------------------
make[2]: Entering directory '/workspace/gitlab-development-kit/gitaly'
make[2]: Leaving directory '/workspace/gitlab-development-kit/gitaly'

--------------------------------------------------------------------------------
Installing gitlab-org/gitaly Ruby gems
--------------------------------------------------------------------------------
ok: run: /workspace/gitlab-development-kit/services/postgresql: (pid 85410) 0s, normally down
ok: run: /workspace/gitlab-development-kit/services/redis: (pid 85409) 0s, normally down
praefect sql-migrate: all migrations are up
make[1]: Leaving directory '/workspace/gitlab-development-kit'

--------------------------------------------------------------------------------
Ensuring necessary data services are running
--------------------------------------------------------------------------------
ok: run: /workspace/gitlab-development-kit/services/postgresql: (pid 85410) 2s, normally down
ok: run: /workspace/gitlab-development-kit/services/redis: (pid 85409) 2s, normally down
ok: run: /workspace/gitlab-development-kit/services/praefect: (pid 85864) 1s, normally down
ok: run: /workspace/gitlab-development-kit/services/praefect-gitaly-0: (pid 85863) 1s, normally down
ok: run: /workspace/gitlab-development-kit/services/postgresql: (pid 85410) 3s, normally down
ok: run: /workspace/gitlab-development-kit/services/redis: (pid 85409) 3s, normally down
gitlabhq_development exists, nothing to do here.
gitlabhq_development_ci exists, nothing to do here.

--------------------------------------------------------------------------------
Updating gitlab-org/gitlab-metrics-exporter
--------------------------------------------------------------------------------
Successfully fetched and checked out 'main' for 'gitlab-metrics-exporter/'
Successfully pulled (--ff-only) for 'gitlab-metrics-exporter/'

--------------------------------------------------------------------------------
Building gitlab-org/gitlab-metrics-exporter version main
--------------------------------------------------------------------------------

> Reconfigured as of 2022-07-14 21:09:54. Took 65 second(s).
Thu 14 Jul 2022 09:09:54 PM UTC – Starting GDK
ok: run: /workspace/gitlab-development-kit/services/postgresql: (pid 85410) 10s, normally down
ok: run: /workspace/gitlab-development-kit/services/redis: (pid 85409) 10s, normally down
ok: run: /workspace/gitlab-development-kit/services/praefect: (pid 85864) 8s, normally down
ok: run: /workspace/gitlab-development-kit/services/praefect-gitaly-0: (pid 85863) 8s, normally down
ok: run: /workspace/gitlab-development-kit/services/gitlab-workhorse: (pid 87029) 0s, normally down
ok: run: /workspace/gitlab-development-kit/services/rails-background-jobs: (pid 87031) 0s, normally down
ok: run: /workspace/gitlab-development-kit/services/rails-web: (pid 87030) 0s, normally down
ok: run: /workspace/gitlab-development-kit/services/sshd: (pid 87032) 1s, normally down
ok: run: /workspace/gitlab-development-kit/services/webpack: (pid 87033) 1s, normally down

=> GitLab available at http://127.0.0.1:3000.
master
SYNCING
Renamed /workspace/gitlab/.git/hooks/pre-push to /workspace/gitlab/.git/hooks/pre-push.old
SERVED HOOKS: pre-push, prepare-commit-msg
Updated 1 path from the index
Awaiting port 3000... ok
Waiting for GitLab at https://3000-shaolabgroup-gitlab-v7i309tykzc.ws-us54.gitpod.io .............
Thu 14 Jul 2022 09:10:54 PM UTC – GitLab is up (took ~2.1 minutes)
Took 12.0 minutes from https://gitlab.com/gitlab-org/gitlab/-/blob/master/.gitpod.yml being executed through to completion 
gitpod /workspace/gitlab (master) $ 
