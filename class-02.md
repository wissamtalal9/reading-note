## HTML & CSS Design and build Websites
### Summary 
- HTML pages are text documents.
- X HTML uses tags (characters that sit inside angled 
- brackets) to give the information they surround special 
meaning.
- X Tags are often referred to as elements.
- X Tags usually come in pairs. The opening tag denotes 
- the start of a piece of content; the closing tag denotes 
the end.
- X Opening tags can carry attributes, which tell us more 
about the content of that element.
- X Attributes require a name and a value.
- X To learn HTML you need to know what tags are 
available for you to use, what they do, and where they 
can go

## HTML5: Adding HTML5 Audio to Your Pages
  - <audio>
  - <source>
  - FLASH, VIDEO & AUDIO
  - Understanding CSS: Thinking Inside the Box
  - CSS Associates Style rules with HTML elements
  - CSS Properties Affect How Elements Are Displayed
  - Using External CSS
  - Using Internal CSS
  

  







## How to Write a Git Commit Message
### Introduction: Why good commit messages matter
If you browse the log of any random Git repository, you will probably find its commit messages are more or less a mess. For example, take a look at these gems from my early days committing to Spring:
......................................................................
$ git log --oneline -5 --author cbeams --before "Fri Mar 26 2009"

e5f4b49 Re-adding ConfigurationPostProcessorTests after its brief removal in r814. @Ignore-ing the testCglibClassesAreLoadedJustInTimeForEnhancement() method as it turns out this was one of the culprits in the recent build breakage. The classloader hacking causes subtle downstream effects, breaking unrelated tests. The test method is still useful, but should only be run on a manual basis to ensure CGLIB is not prematurely classloaded, and should not be run as part of the automated build.
2db0f12 fixed two build-breaking issues: + reverted ClassMetadataReadingVisitor to revision 794 + eliminated ConfigurationPostProcessorTests until further investigation determines why it causes downstream tests to fail (such as the seemingly unrelated ClassPathXmlApplicationContextTests)
147709f Tweaks to package-info.java files
22b25e0 Consolidated Util and MutableAnnotationUtils classes into existing AsmUtils
7f96f57 polishing
......................................................................
### Yikes. Compare that with these more recent commits from the same repository:
......................................................................
$ git log --oneline -5 --author pwebb --before "Sat Aug 30 2014"

5ba3db6 Fix failing CompositePropertySourceTests
84564a0 Rework @PropertySource early parsing logic
e142fd1 Add tests for ImportSelector meta-data
887815f Update docbook dependency and generate epub
ac8326d Polish mockito usage
......................................................................

Which would you rather read?

The former varies in length and form; the latter is concise and consistent.
The former is what happens by default; the latter never happens by accident.

While many repositories’ logs look like the former, there are exceptions. The Linux kernel and Git itself are great examples. Look at Spring Boot, or any repository managed by Tim Pope.

The contributors to these repositories know that a well-crafted Git commit message is the best way to communicate context about a change to fellow developers (and indeed to their future selves). A diff will tell you what changed, but only the commit message can properly tell you why. Peter Hutterer makes this point well:

Re-establishing the context of a piece of code is wasteful. We can’t avoid it completely, so our efforts should go to reducing it [as much] as possible. Commit messages can do exactly that and as a result, a commit message shows whether a developer is a good collaborator.
If you haven’t given much thought to what makes a great Git commit message, it may be the case that you haven’t spent much time using git log and related tools. There is a vicious cycle here: because the commit history is unstructured and inconsistent, one doesn’t spend much time using or taking care of it. And because it doesn’t get used or taken care of, it remains unstructured and inconsistent.

But a well-cared for log is a beautiful and useful thing. git blame, revert, rebase, log, shortlog and other subcommands come to life. Reviewing others’ commits and pull requests becomes something worth doing, and suddenly can be done independently. Understanding why something happened months or years ago becomes not only possible but efficient.

A project’s long-term success rests (among other things) on its maintainability, and a maintainer has few tools more powerful than his project’s log. It’s worth taking the time to learn how to care for one properly. What may be a hassle at first soon becomes habit, and eventually a source of pride and productivity for all involved.

In this post, I am addressing just the most basic element of keeping a healthy commit history: how to write an individual commit message. There are other important practices like commit squashing that I am not addressing here. Perhaps I’ll do that in a subsequent post.

Most programming languages have well-established conventions as to what constitutes idiomatic style, i.e. naming, formatting and so on. There are variations on these conventions, of course, but most developers agree that picking one and sticking to it is far better than the chaos that ensues when everybody does their own thing.

A team’s approach to its commit log should be no different. In order to create a useful revision history, teams should first agree on a commit message convention that defines at least the following three things:

Style. Markup syntax, wrap margins, grammar, capitalization, punctuation. Spell these things out, remove the guesswork, and make it all as simple as possible. The end result will be a remarkably consistent log that’s not only a pleasure to read but that actually does get read on a regular basis.

Content. What kind of information should the body of the commit message (if any) contain? What should it not contain?

Metadata. How should issue tracking IDs, pull request numbers, etc. be referenced?

Fortunately, there are well-established conventions as to what makes an idiomatic Git commit message. Indeed, many of them are assumed in the way certain Git commands function. There’s nothing you need to re-invent. Just follow the seven rules below and you’re on your way to committing like a pro.
