- [Just a Note Before We Start](#markdown-header-just-a-note-before-we-start)
- [Mindset](#markdown-header-mindset)
- [Mobile/Web Target Screen Size](#markdown-header-mobileweb-target-screen-size)
- [Image Placement, Masking, Clipping & Cropping](#markdown-header-image-placement-masking-clipping-cropping)
- [Videos](#markdown-header-videos)
- [Forms](#markdown-header-forms)
- [Cookie Notices](#markdown-header-cookie-notices)
- [Assets & Layer naming](#markdown-header-assets-layer-naming)

The purpose of this guide is to help cover the fundamentals regarding web design, with the hope it will result in smoother workflow, builds and fewer unwanted surprises.

We’ve provided clear headings so this can be used as a key guide.

# Just a note before we start

Currently at Bright we work back to front on web projects, spec’ing and designing without the content creates more work. We are effectively just designing and building templates, we can buy those from Themeforest for $30 and end up in the exact same place, with copywriters needing lots of amends to help them because dreaming up engaging content to fill features is infinitely harder than dreaming up features to display the content.

The features we design, and code should be solving the problem of how best and engaging we can display the content, something you can only do to the highest possible standards with the actual content to work with. We need to stop dreaming up features, then figuring out how to fill it later, it doesn’t work! We will always end up with a final product that failed to reach its full potential.

Also, content for content’s sake, the kind used to fill a website feature just for the sake of having that feature, it almost always lacks energy and passion and often brings zero user and SEO value to the page.

# Mindset
When approaching a website design, think of it like Lego bricks. What we want is the picture on the box, but also to be able to take it all apart and build it back in all different shapes and sizes. So, what the developer needs from design, are the individual bricks. BUT! Lego are made from plastic and that’s bad for the environment, so we want to use as few bricks as possible.

You want each Lego brick to be as versatile and reusable as possible, the best Lego is the Lego with the fewest special niche bricks, the ones you can remake into the most different things.

# Mobile/Web Target Screen Size

Small Sized Mobile
* Width: 280px - Height: 600px (ish)

**Medium Sized Mobile**
* **Width: 375px - Height: 700px (ish)**

Large Sized Mobile
* Width: 420px - Height: 900px (ish)

Tablet Portrait View
* Width: 800px - Height: 1200px (ish) 

Tablet Landscape View
* Width: 1200px - Height: 800px (ish)

Desktop Small Screen
* Width: 1200px - Height: 760px (ish)

**Desktop Medium Screen**
* **Width: 1800px - Height: 950px (ish)**

Desktop Large Screen
* Width: 2400px - Height: 1200px (ish)

The sizes in bold are the best 2 to sizes to target. If your design canvas is set to these sizes this will give you the most common expected view. It will allow you to predict image and video placement with the most accuracy and result in the fewest amends at the end.

Regarding tablets, they only account for < 3% of the traffic and are often overlooked. In landscape view they usually get the desktop version of the website, and in portrait view, they tend to get a big version of the mobile view. So usually, the tablet view sorts it’s self out with very few if any tablet-specific amends. But 3% is still enough to take seriously, so be considerate of tablets and remember the desktop view maybe on a touch screen, meaning both desktop and mobile MUST be fully touch screen friendly.

## Max & Min Widths

Min: 280px - Max: 2200px (ish)

The max size depends on the design, but 1440p is pretty much standard on all new budget monitors, and 4k is a lot more prevalent, so working to a 2200px max width is a good future proof starting point. The traditional 1600px (ish) max width is very narrow on modern monitors.

With mobile, there is still a huge part of the user base with view port as small as 280px, so all mobile versions need to display optimally at that size.

## Above The Fold

**The content that is first displayed on page load without the need to scroll into view, is the most valuable SEO real estate.**

The above the fold content on the home page is usually given priority to visual impact, rather than SEO. But for all other pages, try and get as much of the written content above the fold as possible. As far as SEO matters, the above the fold content is everything, whatever is above the fold on page load carries the entire page’s SEO authority.

## Responsive Elements

**Consider how the desktop version can break down into the mobile friendly view and avoid making the alternative version of the other something completely different.**

The desktop and mobile view of every section needs to expand out and contract in depending on screen size, and we want to avoid having to use JS or Backend user agent arguments to decide which view to present. User agent based mobile detection is not accurate at all, and many users will be shown the wrong display.

It needs to adjust based on screen size and be always a version of itself, going against the view port size is the most accurate method to make sure mobile users get the mobile view, and desktop get desktop. And having the component expand and contract is the optimal bloat-free approach.

If the desktop view is a list of links, the mobile view is a list of links formatted for mobile. If the desktop is a carousel, or an accordion, the mobile view would also be a carousel, or an accordion.

Mobile menu’s function differently, as do auto playing videos, both of which have different behaviour based on mobile.

## Fonts

**Be mindful of how many different fonts you include, as the need to load too many font files can damage SEO.**

To be clear, don’t let yourself be restricted. If the design wants and needs a collection of fonts, use them. But please be reluctant to use fonts to solve problems.

Web has an anti-bloat ambition, it doesn’t want to make you download an entire font family just to access one version of it, such as bold, so we include each one individually. Each time you introduce a new font and then a variant of that font such as bold or italic, we need to then include a new file. Regular + Bold + Italic = 3 file includes. 

A font using weights 300, 500, 700 and italic styles would be 6 includes. That’s the files for each weight, and then a file for each weight in italic. Please try and keep total font includes to 6 or under if possible. If you need to use 10 or more, you’re going to give that website a huge life-long SEO handicap.

The damage to our SEO is exponential with each new file include, they are render blocking assets even when set to defer and swap, and it’s not possible to compensate elsewhere for better page speed scores.

## Font Sizing Units

**Use any font size unit in design files, but understand the dev needs to translate that into EM or REM relational size units, and this is done by eye.**

We use REM’s and EM’s for web, and these are relational sizes that don’t necessarily translate well from the PT and Pixel font sizing used in designs.

Using PT sizing on web doesn’t provide the same consistency across devices. The size we use is in relation to a predictable metric, the user’s current viewport size. Whereas PT sizing is in the control of the OS/Browser, something that varies hugely from user to user thus making it unpredictable.

The reason we avoid using pixel font-sizing on web is because it requires more arguments to account for the large array of potential screen sizes. When using relational sizing, that varying screen size between users stops being a problem to solve and instead becomes a useful metric to calculate font size.

Design should use whatever font sizing unit they wish to use with the understanding the developer will try and match that like-for-like with EM or REM units, and if the result is off, design needs to feed back to that dev with instructions to make it larger or smaller.

## Font Leading & Kerning

**Translation of kerning from print sizes to web sizes is another unit translated by eye, give feedback requesting more or less.**

Font leading in web is called line-height, and kerning is called letter-spacing. These are another example of units where the dev needs to translate with their eye. If the result is off, please feedback whether to increase or decrease.

## Text & Font Size Use

**Don’t use font sizing to solve problems! Set them to use the standard web DOM elements H1 to H6 and P and only divert from this when the design lacks other options.**

If a section is special and unique, for example you’re delivering the page header over a hero image, and the text input for that feature **ONLY ACCEPTS TEXT!** Text with no italic, bold, or hyperlinking at all. Then use any size and style of font you want.

If, however the user input will require more substantial input of a full sentence or more, the design needs to factor in the list below.

If we continue designing without content, we must always assume that every tool will be required not only for the copywriters to populate a section, but for the SEO and link building strategists to do their thing too. Even if that section’s design only logically accepts a single paragraph of text. Experience has unfortunately taught us the hard way, that without content first, we must account for every eventuality instead.

So, unless there is an explicit reason to believe anything on the list below won’t be needed, such as having copy first and knowing it won’t be needed, every text section needs to assume the following will always be needed and accounted for in the design and therefore design need to include this in their timeframe for quoting projects.

* **Header 1 </*h1*/> Highest authority** - The H1 tag carries the most SEO authority and should only be used once per page.
* **Header 2 </*h2*/>** - Often set to be an exact match as Header 1, and then used to present the same visual but with less SEO authority.
* **Header 3 </*h3*/>** - This would be used for in-body subheadings if H2 is being employed as a less authoritative page header option.
* **Header 4 </*h4*/>** - spare if needed and useful for minor headings, be mindful of its reduced SEO authority and avoid using these with important SEO relevant content.
* **Header 5 </*h5*/>** - Good for footer and sidebar/aside headings, they carry very little authority but still signify some importance to the section they head.
* **Header 6 </*h6*/>** Lowest authority – Used for footer and aside subheadings, and other headers with little to zero SEO relevance. 
* **Paragraph </*p*/>** - Paragraph text.
  * **</*b*/>/</*strong*/>** - Bold Paragraph text
  * **</*i*/>** - Italic text
  * **</*u*/>** - underline text
  * **</*a*/>** - hyper-link
   * **</*a*/>:hover** - hyper-link hover state
   * **</*a*/>:active** - hyper-link active state 9if an active style is required)
  * **</*ul*/>** - Bullet point list
  * **</*ol*/>** - Numbered list

## Image Sizes and file format

**Use images with pixel dimensions 2x larger than the area they are intended to fill, but don’t go over 2.5x times larger and If your original image is over 2200px wide do not use 2x**.

We use images twice in size because we need to account for retina and mobile displays. The reason for this is due to how these device’s viewports relate to their physical screen resolution.

For example, an iMac retina desktop is 5k physically, but it’s viewport is only 1440p (2k). A modern iPhone has a physical screen resolution in portrait view that is 1,170 pixels wide, but its web browser reports and uses a viewport size that is only 390 pixels wide.

The browsers on these devices are pretending to be smaller in pixels to provide a numerical value that better represents the physical size of the device, but the result that is rendered at that smaller size still needs to fill the physical pixels, of which there are many more.

Vectors and fonts obviously scale up perfectly, but when it comes to images, if you use a file that is 380px wide for example, that file will be stretched over the physical screen’s 1,170px, which would mean the image is enlarged by around 300% resulting in poor and blurred image quality.

BUT! We can’t just use an image of 1,170px wide to fill every pixel achieving perfect visual fidelity, because Google Page Speed will see that image, then see the 390px wide container, and think “that’s way to big for that” and mark us down on our performance, which negatively impacts our SEO.

2x larger is the sweet spot for page speed scores, SEO and visual clarity.

**Image file format PNG vs JPG**
How to make the decision when exporting your images. That’s quite simple, if the image needs a transparent background because it’s going to overlay a coloured CSS background then PNG is the correct choice.

For any other images use JPG, they are flattened into smaller file sizes resulting in improved website speed and performance SEO scores.

**NOTE: please avoid using PNG files over 1000 pixels in height or width unless absolutely necessary, as they generate huge file sizes that damage SEO**

**Vector graphics**
SVGs are now well supported across most web browsers, if you have vector icons/illustrations please supply as SVG.

**Vectors do not apply to emails**, SVGs are not supported across most email clients.

# Image Placement, Masking, Clipping & Cropping

**Place images anchored by one of its corners, or fully centred to better predict cropping behaviour.**

When placing images in design files, we’ve noticed images are within masks, which is great as we often code it just like that, but the placement of that image is often done by mouse and eye, impossible to replicate with code.

When placing images inside masks or clipping paths, please place them so the image is either centred, or anchored by one of its corners. This fixed point will determine cropping behaviour as it scales to fit its parent element corner to corner.

# Videos

**Don’t forget to add the controls and remember that on mobile we never play a video the user doesn’t explicitly request to play.**

When using videos as a background feature, muted with no intended interaction, remember that this will only be for desktop and tablet view only. We must always assume the worst-case scenario with mobile, in that their connection will not only be slow, but that user may have limited access to data. So, the mobile view should stick to imagery and vectors for background visuals.

For in-body videos, we need the following:

* Play
* Pause
* Mute
* Volume Slider
* Progress track bar
* Numerical progress indicators (optional)
* Thumbnail/pre-load state
* Loading/buffering feedback
* Error/failed to load video state

# Forms

**Designs need to cover all states, including feedback messages and completed submissions.**

We don’t think this guide needs to detail all the different fields, we are all Interneters here, but forms need the following.

* Initial state, as already done in usual designs.
* Each individual field needs:
  * Focus state – What happens when clicked on and entering a value
  * Error state – Visual indicator on the field that there is a problem with the user’s current input
  * Individual feedback message/tool-tips – For errors such as invalid email, required field etc.
* Submit button:
  * Enabled/Disabled states – We want to always use front end validation as a first line of anti-spam defence, and not allow invalid form submissions if we can prevent them, so a visual indication that the submit button is disabled is needed.
  * Also, a tool-tip on hover or feedback of some kind to let the user know why the button is disabled, and it should detail briefly what the user needs to do so the disabled state doesn’t confuse.
* GDPR/PRIVACY – Always put at least 2 check boxes on your forms if there is no copy to work with, forms almost always carry legal issues with them, which are solved by check boxes 99.9% of the time.
* Click Walls - Forms can be quite damaging to SEO, especially if you want to place one in the footer for example, so for footer forms a “click wall” is preferable, something for the user to click on that would then present the form. This lets us hide those types of forms and the bloat they come with from crawlers that influence our SEO.
* We need a successful submission message - This short period of time immediately after a form submission is a powerful and potent time while our user is invested and engaged, it’s one of the best times to pull in a call to action offering a more direct and immediate form of communication, such as phone numbers, which convert much better than email/web form generated leads.
* For React/Cloud native we need an error state if an API is unreachable. In a cloud native environment an entire website wouldn’t go offline in the event of a technical fault, but rather just a specific section or function, so we need a state that indicates there is an issue connecting, and that the form can’t take any submission attempts.
* Drop downs:
  * Default state
  * Open state
  * An option selected while open state
  * An option selected but closed state
* Image Drag and Drop uploaders
  * Default state
  * Hovering over with images selected state - a visual indicator to let the user know that the drag and drop area sees the files being held by the user’s click, and that it’s ready for them to let go.
  * Image uploading progress.
  * Image upload successful (thumbnail optional)
  * Add more images button if 1 or more images have already been added.
  * Invalid image format feedback
  * Image too large feedback
  * Delete uploaded image trigger
  * File limitations and other labels:
    * File types accepted
    * Max file size
    * Short sentence letting the user know they can click or drag and drop.

# Cookie Notices

**It’s an annoyance no one cares about, but it doesn’t have to be boring. We can be more creative to offer something different.**

There’s nothing in the GDPR guidelines that says the notice must be the same generic bottom bar that everyone does, and it doesn’t state that it needs to consume half the page. Obvious and clear is the requirement, and we can tone these down to simple corner popups that are far less intrusive, more visually engaging, and far less damaging to the website’s overall aesthetics.

# Assets & Layer naming

**Give your files and layers descriptive names.**

These designs are a permanent visual reference throughout the life of the project and giving your assets and layers relevant and descriptive names will help in the future and during development, especially if the developer or designer is unfamiliar with the project, it will help them enormously to pair development assets with its design counterpart.

All website projects will need the following assets supplied:
* Favicon (browser tab icon) – 512px x 512px
* OG image (displayed when a website is shared) – Can be set per page/post but a default one should be supplied – 1024px x 1024px
* Loading animation – Displayed if there is a delay in loading content
