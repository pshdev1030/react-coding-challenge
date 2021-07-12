# Rocket Ship Coding Challenge 🚀 &nbsp; ![easy](https://img.shields.io/badge/-Easy-brightgreen) ![time](https://img.shields.io/badge/%E2%8F%B0-10m-blue) 

&nbsp;
## Goals / Outcomes ✨
- To test basic understanding of render lifecycles in both functional and class components

&nbsp;
## Pre-requisites ✅
None

&nbsp;
## Requirements
- Stop the Class rocket from taking off
- Stop the Functional rocket from taking off

&nbsp;
## Think about 💡
- How we prevent components from re-rendering

&nbsp;
## What's Already Been Done 🏁
- Functional and class rocket components
- UI/UX and animation

&nbsp;
## Screenshots 🌄
&nbsp;
![screenshot](https://puu.sh/Fq16F/1ad6edff1b.png)


export const FunctionalRocket =memo(()=> {
  const [initialLaunchTime] = useState(Date.now());
  return <RocketCore initialLaunchTime={initialLaunchTime} />;
});

```javascript
//수정 전
export function FunctionalRocket() {
  const [initialLaunchTime] = useState(Date.now());

  return <RocketCore initialLaunchTime={initialLaunchTime} />;
}
//수정 후
export const FunctionalRocket =memo(()=> {
  const [initialLaunchTime] = useState(Date.now());
  return <RocketCore initialLaunchTime={initialLaunchTime} />;
});
```