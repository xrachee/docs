# Tooling Research, and the Struggles it's Created

So before I could start finding a tool that did what the company wanted, I needed to know the requirements. Alongside the feedback I'd gathered, I'd also asked for some requirements:


1. The wiki needs to support multi-repository documentation locations. Basically, the tool needs to be able to pull code from any defined repository, and using metadata, place it in the correct place in the wiki. 
2. The search functionality needs to support partial search results. So, I need to find a tool that is going to meet the security policy, and (as a preference) be open-source and actively supported.
3. Needs to support Markdown and MDX. This shouldn't be a problem, most tools support Markdown as it's a lightweight markup language.
4. Needs to support images in png, jpeg and svg formats. Apart from svg format, quite simple to do.
5. Needs to support the display of UML-type diagrams, including Mermaid diagrams. Thankfully UML languages are becoming quite common, so there's a lot of support for displaying these types of diagrams.
6. Preference for an in-built editor, but only if bi-directional syncing exists. Simply put, someone can modify a page in the wiki, and the source code (in the repository) will be updated. However, you cannot create new pages in the wiki, they have to be done in a repository.
7. Deployment needs to be similar to what already exists. So needs to go to AWS, and has automatic refresh when there is a change to the wiki in any way.
8. Optional. Comments and feedback available to give in the wiki. From an analytics point of view, this would be good. It would allow us to see how the wiki is being used, and by being able to give feedback on any given page, people can see and learn how useful the information is.


- [Docusaurus](https://docusaurus.io/)

So Docusaurus was one of the first tools I considered as an alternative to wiki.js. Created by Meta (formally known as Facebook), it's an open source, static site generator. Docusaurus builds a single-page application, using React to make the site interactive. In order to use it, you need to install [Node.js](Nodejs.org). Many big companies use Docusaurus to build their website. It's a very user-friendly interface, 

- MKDocs
- Gitbook
- Astro
- Gatsby
- Hugo

Utilise Git submodules?

headless cms separates content from presentation (website). why? content tangled with code. 

*Sources*
- [Docusaurus Documentation](https://docusaurus.io/docs)