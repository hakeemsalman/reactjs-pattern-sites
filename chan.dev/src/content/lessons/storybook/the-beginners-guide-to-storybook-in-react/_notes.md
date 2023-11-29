# Challenges to Learning

## Proposed course changes

- Remove viewports instruction. Too many requisite concepts.
- Remove chromatic lesson. Feels orthogonal.
- Move integration with your application lesson to end. Better hand-off.

## Sample stories

### Button

- `Button` interface is as peculiar. is `label` used over `children` for multi-framework support?
  - Supporting children/slots/etc. seems like a critical part of an integration.
  - Could changing the example actually aid framework support (as a test case)?
- Color picker is an impractical demo for button. It demos a nice component but isn't connected to real world.
  - Is there another component where color picker may make more sense?
  - If not, I think it should be removed.
- `Button:Secondary` story is confusing because it uses no props.
  - I'd like to see the primary component state be the default state (no args).
    - This makes the demos more progressive and easier to grok.
  - There is a natural collision here with DocBlocks `Primary` story.
    - Consiquently I think that the DocBlock should become `First`

### All

- `title` is hella confusing to a newcomer (likely familiar with file-system based routing).
  - I'd like to see auto-title (with `component` meta) as the default.
- The `stories` directory poses some practical and conceptual issues
  - People don't know realize that `./stories` isn't the golden path.
    - Could be solved with `./sample-stories`.
  - People don't know that it can safely be deleted.
    - Add `README.md` with details.
    - Initializer could say something like `Sample stories have been added to the .src/sample-stories directory. Run {command} to remove those sample stories. Use the {flag} flag to initialize projets without the sample stories.`
- Actions depend on too many requisite concepts (pramaters, argTypes, and preview) and Regex.
  - Everything should be demonstrated on-story or on-component.
  - `preview` can have comments for the global options
- Comment links are too long.
  - Short links would be helpful here.
  - `sb.link` is an available domain. We should get it for short links.
    - These _could_ be codified short links, to include ui library info: `https://sb.link/actions/react`.
- Nothing is shown when there is a component with no stories. This makes progressive instruction difficult.
  - We could show a component in the sidebar.
    - Simplest solution would be to have it be disabled in the sidebar.
    - More advanced solution is to leave it enabled with an an empty-state page for creating a sample story from the `component` provided on meta.
- The concept of a "component" in Storybook is confusing.
- The Viewports interface is extremely confusing to me.
  - Problem is that literally all the information is hidden and requires touching 2-3 files to use.
  - I'd like a path where we could implement a viewport inline (at story and component)
  - I'd also like to see a `breakpoint` variant, which we've discussed before.

## Page

- The current page demo does not accurately represent a page.
  - Could be interesting to see a sample `AuthProvider` implemented as a decorator.
    - Like with `Button`, this will push sample stories more into the territory of framework-specifics.

## Misc

- The concept of a "component" is so confusing.
  - I've decided to embrace it and just teach stories from components.
    - There's a progressive map (the one i used on YouTube) but if this is a beginner's guide, i'm just going to leave out the helpful ambiguity.
- I've used the term component meta being a `default export` object. But that isn't correct. These are all fields just exported on the module.

## COLOR theme

- using `create`, you're forced to choose light or dark.
  - This impacts folks who just want to add their image and custom domain

## Advanced topics

- Parameter inheritance

## editing process

- hard to teach, hard to learn

## Reviewer notes

Hi! Thanks for making time to review these lessons for our upcoming egghead course: _A Complete Beginners Guide to Storybook 7_.

All feedback is welcome. And I'd like to make sure that you're well equipped to provide feedback that is actionable at this stage in the process.

So, here are a few thingsy you'll want to know before reviewing.

### Audience

This is a course for Storybook beginners.
We have no intention of being exhaustive.
We will leave a lot of advanced options and insights on the table to keep it tractable for beginners.

Our definition of beginner includes designers and developers.
Anyone interested should be able to take something from this course.

## Approach

To appeal to the broadest possible audience, the course is presented in two acts.

1. An overview of Storybook UI and terms
2. Implementing features in CSF

This should allow anyone to gain an understanding of Storybook, and jump off at the point that it doesn't server them.

## Structure

The goal with these lessons is to be both progressive and atomic.

Each lesson should stictch together into a cohesive course experience.
But they'll ideally be atomic enough that we can link

_This is the area where the most review would be helpful. I have been thinking about the progressive side and less the atomic side. Let me know if there are lessons that don't seem to stand on their own (well enough)._

## These are _just_ scripts

These are just scripts used to create videos.
Don't sweat the details of grammar. But if something is technically innacurate, I'd like to know.

## Feature complete

We've done quite a bit of work to limit the demonstrated features, while still showing off a lot of Storybook's capability.
Adding features at this point could be a very big lift.
This isn't impossible but if you think something should be added, know that it will be met with immediate resistance.

## Thanks

That's it!
I applaud those who make it all the way thru.

Thanks for your help.

Chan