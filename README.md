# How to Commit
Editing is history of changes, and a change is expressed as a commit.  

## 1. Think subject line first
First of all, think subject line of commit message.  
Properly formed subject line can complete the following:  
    If applied, this commit will `SUBJECT-LINE`.
- limit to 50 chars
- use the imperative mood
- capitalize
- do not end with a period

If you're having difficulty in summarizing into 50 chars,
you might be committing too many changes at once.  
Separate them into atomic commits (= the unit of changes).  

See also Examples of subject line in commit below.

## 2. Write docstring before implementing code
**What** elements are required to accomplish subject line considered above?  
**What** problems does this code you are implementing solve?

## 3. Implement
Express your idea in code.  
Code written and tools such as diff show **How** to solve problems.

## 4. Write body of commit message following a blank line
- separate subject from body with a blank line
- wrap the body at 72 chars

Write supplemental context to understand the full diff.  
In addition to headline of docstring written above,
- **Why** is this change necessary?
- the reasons **why** you mede the change?
- Are there any alternatives?
- What side effects does this change have?


## Examples of subject line in commit
### Overview
- Add (anything such as method, test, document)
- Fix (typo, crash, NOT document)
- make sure that (concrete behavior)
- Update (document, comment, test, NOT code)
- Remove (just deletion, not change)
- Use B instead of A
- Change A to B
- Rename A to B (just change name)
- Move A to B (just change place)
- Don't use
- NOT use too abstract verb such as refactor
### オプションやフラグ、メニューを追加した
- Add -enable-experimental-nested-generic-types frontend flag
- Add --main-process flag to run specs in the main process
- Add Throws flag and ThrowsLoc to AbstractFunctionDecl
- Add "event" parameter for "click" handler of MenuItem
- Add File &gt; Exit menu on Windows
### ファイルを追加した
- Add npm start script
- Add build script
- Add SkUserConfig.h with blank SkDebugf macro
### メソッドや機能を追加した
- Add TypeLowering::hasFixedSize()
- Add overflow scrolling
- Add convenience API for demangling
- Add a typealias to avoid a build ordering dependency between projects
- Add a helper method mayHaveOpenedArchetypeOperands to SILInstruction
### 実装を別のものへ切り替えた
- Use args.resourcePath instead of args.devResourcePath
- Use arrays instead of while loops
- Use auto instead of repeating explicit class names
- Use weak pointer instead of manual bookkeeping
- Change all uses of 'CInt' to 'Int32' in the SDK overlay
- Change Integer#year to return a Fixnum instead of a Float to improve consistency
### 新しく何かに対応した/機能上の制約を取り払った
- Add support for closure contexts to readMetadataFromInstance()
- Add support for activating and deactivating package-specific keymaps
- Add support for launching HTML files directly
- Add support for allocators that require tensors with zero
- Make it possible to call `reflect` multiple times
- Make it possible to set a data type for variables that come out of constants
- Allow atom-pane to be shrunk independently of its contents' width
- Allow null TextEditorComponent::domNode during visibility check
### 何かを使うようにした
- Use const for util require
- Use FoldingSetNode for ProtocolType
- Use unique text editor title in window and tab titles
- Use an empty object if metadata is ~null
- Use target_link_libraries for fat executable dependencies
- Use existing flatMapToOptionalTests dataset
### より好ましい実装に改良した
- Make the clone function more generic
- Make IO faster for v8 compile cache
- Make model constructor argument to addViewProvider optional
- Make Browser::Quit more robust
- Make Menu.getApplicationMenu() public
- Improve incompatible native module error message
- Improve readability of multi-line command
- Improve folds behavior when duplicating lines
- Improve deprecated message on webPreferences options
### 何かを出来ない/しないようにした
- Don't bail reading a metadata instance if swift_isaMask isn't available
- Don't exit until the parent asks for an instance
- Don't include Parent pointer in Nominal/BoundGeneric TypeRef uniquing
- Don't use MatchesExtension for matching filters
- Don't use ES6 class for AutoUpdater windows class
- Don't use MatchesExtension for matching filters
- Avoid `distinct` if a subquery has already materialized
- Avoid infinite recursion when bad values are passed to tz aware fields
### オブジェクトの内容や挙動を確認しやすくした
- Emit capture descriptors in their own section
- Emit field metadata for @objc classes
- Emit reflection info for protocols
- Assertを追加した
- Add assert for role with app name in label
- Add assertions for no available bookmark
- Add asserts for properties
### 不要なコードを除去した
- Remove some dead code
- Remove some unused enum declaration
- Remove unused variable
- Remove unnecessary line feeds
- Remove trailing whitespace
- Remove debug statement
- Remove redundant mapType{Into,OutOf}Context() calls
### コードを移動した
- Move function signature analysis to a Util
- Move markInvalidGenericSignature() to a method on TypeChecker
- Move diagnostic for stored properties in protocols from type checking to validation
- Move Doxygen converter into a proper MarkupASTNode visitor
- Move Module require to top
### 名前を修正した
- Rename environment -&gt; environmentHelpers
- Rename watchProjectPath to watchProjectPaths
- Rename generic arguments
- s/grammarName/grammar
- fullVersion -&gt; writeFullVersion
### 小さなバグやタイポを修正した, 警告を潰した
- Fix typos
- Fix a typo
- Fix a test
- Fix typo in DevTools Extensions tutorial
- Fix DownloadingState typo
- Fix includes order
- Fix mistake in tvOS availability
- Fix cpplint warnings
- Fix wrong markdown
- Add missing return
- Add missing period in comment
### バグや好ましくない挙動を修正した
- Fix a memory leak in FSO
- Fix lifetime issues in ManagedBuffer.value
- Fix mangling for nested generic types
- Fix memory corruption in another circularity check
- Fix thread-unsafety in Process.Argument initialization
- Fix "Object has been destroyed" error in "page-title-updated" event
- Make Error.prepareStackTrace read-only (again)
- Make string slicing tests standalone
- Make sure showing success dialogs works correctly
- Make sure to emit closure bodies only once
- Make sure all native resources get freed on exit
- Make sure temp file will be cleaned up when base::Move fails
### テスト、コメント、ドキュメントを追加した
- Add tests for pending pane items
- Add validation test for projecting existentials
- Add a basic test for opening an editor in largeFileMode if &gt;= 2MB
- Add specs for moveSelectionLeft()
- Add failing spec for Menu.buildFromTemplate
- Add comment about map key/values
- Add TODO about blinkFeatures -&gt; enableBlinkFeatures
- Add a design-decisions section to the CONTRIBUTING guide
- Add style.less examples
- Add docs for app.getLocale()
- Add documentation for --proxy-bypass-list
### テストを削除した
- Remove a redundant test
- Remove an empty test
### テスト、コメントを修正した
- Fix comment
- Fix outdated comment
- Fix failing specs on Windows
- Fix PersistentVector test for powerpc64{le}
- Update specs for deferred activation hooks
- Update successor/predecessor in validation tests
- Update some tests to use LifetimeTracked instead of hand-rolled canaries
### ドキュメントを修正した
- Update README.md
- Update docs for marker callback
- Update documentation for markPosition
- Update link to solarized-dark-syntax
- Improve documentation of `ses.cookies.set()`
- Improve readability in CSRF section of guide
- Improve spec description


## References
- [How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/)
- [gitにおけるコミットログ/メッセージ例文集100](https://anond.hatelabo.jp/20160725092419)
