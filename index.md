![gsoc_x_kiwix](https://user-images.githubusercontent.com/17774888/91468450-aac24280-e8af-11ea-8f1a-5ec4c246bc98.png)


# Work Report for Google Summer of Code 2021 📑

## About me and the project ℹ️
My name is [Manan Jethwani](https://mananjethwani.github.io) and I worked on [New library catalogue UI for Kiwix-serve](https://summerofcode.withgoogle.com/projects/#5158540915769344) under Kiwix. My project was aimed at enhancing UI-UX experience for kiwix-serve which is used to host various zim files. My basic goals for this projects were -
- Design a new UI mockup of https://library.kiwix.org.
- Prepare the javascript to dynamically add books to kiwix-sereve.
- Allow for widgets.
- Add filter feature.
- Various other minor features like automatic language filter using browser language, custom HTML template etc.

## How it all started 🌅

I had started contributing to kiwix in august 2020 by working on kiwix-serve but then moved to working on mwoffliner under openzim org. which is a subpart of kiwix. 

MWoffliner is one of the main projects handled by the Kiwix which is a nodeJs application that enables the bundling of Wikipedia and other mediawiki websites for offline use. For example, it can scrape the whole en.wikipedia.org content in a run and provide an offline version of that in a file that can be accessed anywhere.

My main contribution for this org. was to solve bugs that cause failiure in scrapping zim files.I also worked on other UI related bugs and added webp functionality which helped us reduce offline content size by 10-15%.

Apart from kiwix-serve I also contributed to kiwix-tools and kiwix-desktop.
As my mentor was satisfied with my contributions I was recommended to take up New library catalogue UI for Kiwix-serve as a GSoC project. It will be soon released with libkiwix10.

## Contributions under GSoC 📝

<table>
<thead>
<tr>
<th align="center">before</th>
<th align="center">after</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MananJethwani/GSoC-2021-New-Library-Catalogue-UI-for-kiwix-serve/blob/gh-pages/Screenshot%20from%202021-08-22%2011-37-19.png"><img src="https://github.com/MananJethwani/GSoC-2021-New-Library-Catalogue-UI-for-kiwix-serve/raw/gh-pages/Screenshot%20from%202021-08-22%2011-37-19.png" alt="" style="max-width:100%;"></a></td>
<td align="center"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MananJethwani/GSoC-2021-New-Library-Catalogue-UI-for-kiwix-serve/blob/gh-pages/Screenshot%20from%202021-08-22%2011-37-48.png"><img src="https://github.com/MananJethwani/GSoC-2021-New-Library-Catalogue-UI-for-kiwix-serve/raw/gh-pages/Screenshot%20from%202021-08-22%2011-37-48.png" alt="" style="max-width:100%;"></a></td>
</tr>
</tbody>
</table>

### Dynamic Welcome Page for Kiwix-serve
Kiwix-served used a static template and placed all zim files at once in the HTML itself using mustache and served it directly, moving to a Dynamic welcome page helped faster loading of page and could support various other features like filter(discussed later on).
Throught this feature I also added subset loading(infinite scrolling as a feature).

##### Linked Issues - 
- [Kiwix serve welcome page should be dynamic](https://github.com/kiwix/libkiwix/issues/511)
- [Kiwix-serve welcome page doesn't account for --urlRootLocation](https://github.com/kiwix/libkiwix/issues/589)
- [Load & display only a subset of the results on the welcome page](https://github.com/kiwix/libkiwix/issues/514)

##### Linked Pull Requests -
- [Kiwix Serve welcome page dynamic and subset loading (OPDS based)](https://github.com/kiwix/libkiwix/pull/530)
- [Dynamic and subset loading of catalogue in kiwix-serve](https://github.com/kiwix/libkiwix/pull/541)
- [corrected relative links in preview and icon url](https://github.com/kiwix/libkiwix/pull/590)

### Filter functionality on Dynamic Welcome Page -
Added filter functionality for languange and categories on welcome page, I also worked on adding features like caching select box values, automatic browser language detection for language select box.
I used special language and category API endpoints created for this purpose.

##### Linked Issues -
- [Kiwix-serve welcome page filter by category](https://github.com/kiwix/libkiwix/issues/517)
- [Replace topbar and implement a few search filter on welcome page](https://github.com/kiwix/libkiwix/issues/531)
- [Use language/category API to populate Kiwix Serve filter select boxes](https://github.com/kiwix/libkiwix/issues/555)
- [Smarter default filter](https://github.com/kiwix/libkiwix/issues/594)
- [Kiwix Serve filters on welcome page should be kept](https://github.com/kiwix/libkiwix/issues/557)

##### Linked Pull Requests -
- [Add filters to kiwix-serve welcome page](https://github.com/kiwix/libkiwix/pull/534)
- [Use OPDS API to populate categories/languages select boxes on Kiwix Serve welcome page](https://github.com/kiwix/libkiwix/pull/600)
- [Improved browser lang filter working](https://github.com/kiwix/libkiwix/pull/596)
- [Keep Kiwix Serve filter values over time](https://github.com/kiwix/libkiwix/pull/561)

### UI-UX revamp
Revamped UI-UX updated navbar, cards, and added download modal.

##### Linked Issues -
- [Kiwix Serve welcome page Download overlay](https://github.com/kiwix/libkiwix/issues/579)
- [Propose a welcome page which is fancier](https://github.com/kiwix/kiwix-tools/issues/448)

##### Linkedin Pull Requests -
- [Modal download box on Kiwix Serve welcome page](https://github.com/kiwix/libkiwix/pull/583)
- [Revamped Kiwix Serve Welcome page layout](https://github.com/kiwix/libkiwix/pull/559)

### Other undergoing work -
I am working on adding support for widgets and customizable welcome page.

##### Linked Issues -
- [Kiwix Serve welcome page title should be customizable](https://github.com/kiwix/libkiwix/issues/571)
- [kiwix-serve (ZIM?) should propose widgets](https://github.com/kiwix/libkiwix/issues/585)

##### Linkedin Pull Requests -
- [added nofilter attribute and iframe conditions](https://github.com/kiwix/libkiwix/pull/587)
- [added cutomIndexTemplate option to kiwix-serve](https://github.com/kiwix/libkiwix/pull/607)

## Future Work 🔮
As far as the project goes there are few things that can be improved and changed, for more updates you can clearly have a look at the [project page](https://github.com/orgs/kiwix/projects/13), I would like to improve upon the design I created and would love to see more features coming to kiwix-serve in future few of them listed below:
- support for filters on basis of tags.
- support for filters/sorting on basis of popularity.

## Acknowledgments 🤗

I would like to thank my mentors @kelson42, @mgautier, @veloman-yunkan and @stephane.

@kelson42's guidance played a huge role in developing my project, he was present at all times to solve my stupid little doubts, Inspite of having a whole organisation to maintain. He has been an inspiration for me since I started contributing to this organisation, he and @stephane are true leaders according to me ❤️.

@mgautier and @veloman-yunkan were great at reviewing all my pull requests and they were so friendly, even after I made so many small blunders in my initial PRs.

Thanks to @stephane for his reviews on UI part and his bugs report which helped me fine-tune my project according to users needs, minute details he mentioned worked like a charm to enhance user experience.

## Conclusion ⭐
This was my first time working with such a big and professional codebase and it was fun to fit things perfectly into it. To be honest, I was intimidated by it when I saw it for the first time but as I worked through it, I understood its value. I learnt so many new things in the last 3 months : Implementing 3rd party library like Isotope to adding browser compatibality, from Unit testing to UI-UX development, it was all so good. During the course of this program my code quality has improved significantly and the major credit for this goes to the detailed code reviews that are done here at Kiwix.

I hope that both Kiwix as well as Google through their respective student developer programs will continue to inspire many more developers for years to come and hope that their journey will be as memorable as mine 😄.

There has been a lot of coding, experimentation, thousands of builds and never ending debugging put into this project and I hope when it is released the users will be satisfied and would love the new functionalities we have worked so hard on introducing to kiwix-serve.

Overall it was an incredible experience contributing to open source and working with like minded people from all over the world. My journey as a developer has just started and I hope to work on various open source projects to support and build a healthy community.
