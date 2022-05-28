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

