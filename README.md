# Courses-App

> next.js + storybook + strapi

## Notes

### Custom hook useId

```ts
export const useId = (): string => {
  const { current } = useRef(Math.random().toString(16).slice(2));
  return current;
};
```
