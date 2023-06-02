# useNavigate()

- return : a function that let me navigate

- page 1 (from)

```javascript
import { useNavigate } from "react-router-dom";
export default page1 = () => {
  useEffect(() => {
    if (userLoginStatus) {
      navigate("/url", { state: { key: value } });
    }
  }, [userLoginStatus]);
};
```

- page 2 (to)

```javascript
import { useLocation } from "react-router-dom";
export default page2 = () => {
  const { state } = useLocation();
  const { key } = state; // value
};
```
