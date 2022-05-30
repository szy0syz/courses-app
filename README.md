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

### Switch component

```ts
const Wrapper = styled.label`
  & input {
    display: none;
  }
  & input:checked {
    & ~ label {
      background: ${({ theme }) => theme.components.primary};
      &::after {
        margin-left: 3.5rem;
        background: ${({ theme }) => theme.components.active};
        ${transition()};
      }
    }
  }
`;

const VisiblePart = styled.label`
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  cursor: pointer;
  height: 3rem;
  width: 6rem;
  border-radius: 1.6rem;
  background: ${({ theme }) => theme.components.background};
  ${({ theme }) =>
    boxShadow(theme.components.shadow1, theme.components.shadow2)};
  &::after {
    content: "";
    margin-left: 0.5rem;
    width: 2.1rem;
    height: 2.1rem;
    border-radius: 50%;
    background: ${({ theme }) => theme.components.nonActive};
    ${transition()};
  }
`;
```

### CI/CD

![001](https://user-images.githubusercontent.com/10555820/170835220-8c55f44c-ce1e-4948-b036-6994ea2e5fb7.png)

<img width="921" alt="002" src="https://user-images.githubusercontent.com/10555820/170926153-ee88f859-fc8a-4444-93f4-07837b120664.png">

### Workflow

> 终于有个完全的流程概念：组件评审、UI整体评审、评审通过、合并代码。

![0002](https://user-images.githubusercontent.com/10555820/170959790-2f58dded-53b5-417e-9807-7a86d117bd85.png)

![00003](https://user-images.githubusercontent.com/10555820/170959914-d6fc9b83-48e4-4b3b-aa80-6011f839f706.png)

![00004](https://user-images.githubusercontent.com/10555820/170959925-1ae0ecd4-739b-4fba-bd1a-0003d26f5598.png)

![00005](https://user-images.githubusercontent.com/10555820/170959940-5737a2a7-b9e5-42c5-ac94-1567ce1281ea.png)




