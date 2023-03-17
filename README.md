# MyTailwindPreset
This is my personal utilities preset to shorten the traditional tailwind. **WARNING: This an extreme version that covers pretty much every hard-coded values**.

## Problems with Tailwind
Tailwind is basically, in my humble opinion, the perfect CSS toolkit, except for that one notoriously annoying part - **incredibly ugly HTML**. Especially not being a big fan of putting HTML tags across multiple lines, I gradually find those excessively long tags unacceptable.  
Some people argue that my version of Tailwind is just not readable. While I agree my syntax becomes less legible, we have to eventually strike a balance between legibility and level of satisfaction, and I've done my best job to match the acronyms as logical as I can. However, I would argue that it takes only about **15 mins** for traditional Tailwind to switch over to my concise version, but with at least **20%** boost in efficiency once you get a hold of it, 
### Minor unpleasant part: inconsistent gaps
Another tedious thing is the gap system of the default Tailwind utility classes. Normally, the gaps are either 4px or 2px. But it may goes up to 16px after it reaches certain values. It is actually not rare to miss out on the gaps and I've had traumatic experiences debugging with this exact problem. (I know Emmet exists but still)  
With my version, I don't need to always have that in mind and double check if the util-class value is predefined.

## Display
```jsx
<!-- Traditional Tailwind -->
<div className="h-screen w-screen flex-col md:max-lg:flex-row flex justify-center items-center snap-y snap-mandatory overflow-hidden">
    <div className="relative w-40 aspect-[9/16] max-w-[570px] flex-shrink-0 snap-start pointer-events-none z-[35]">
        <Image src="" alt="" fill priority />
    </div>
    <div className="w-[43%] h-full">
        <div className="h-[17%] min-[540px]:h-2/5 text-2xl leading-[1.74] bg-black text-white rounded-md border-dotted">
            Lorem ipsum...
        </div>
        <div className="cursor-pointer inline-block mt-[17px] mx-[17px] text-justify opacity-[0.55]">
            Lorem ipsum...
        </div>
        <div className="-rotate-[17px] scale-x-[1.35] duration-[150ms] delay-[600ms]">
            Lorem ipsum...
        </div>
    </div>
</div>
```

```jsx
<!-- My Tailwind -->
<div className="hs ws fc md:max-lg:fr fjcic snapy snapmand ofh">
    <div className="rela w160 ar9w16h maxw570 fnoshrink snaps penone z35">
        <Image src="" alt="" fill priority />
    </div>
    <div className="w43p h100p">
        <div className="h17p min-[540px]:h40p t24 lh1_74 bg-black text-white brounded6 bdotted">
            Lorem ipsum...
        </div>
        <div className="cursorp ilb mtx17 tj opac55">
            Lorem ipsum...
        </div>
        <div className="-rotate17 scalex135 transdur150 transdelay600">
            Lorem ipsum...
        </div>
    </div>
</div>
```
**The difference is noticeable!!!** But media queries with responsive modifiers are still very long......