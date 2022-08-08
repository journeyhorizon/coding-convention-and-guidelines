## React-Coding-Convention
This is the React coding convention for Journey Horizon developers. Please read it kindly and carefully.


## Here is our convention to have a consistent source code and quanlity.

This style guide is mostly based on the standards that are currently prevalent in JavaScript.

## Table of Contents

  1. [Basic Rules](#basic-rules)
  1. [Naming](#naming)
  1. [Class and Function components](#class-and-function-components)
  1. [Hooks](#hooks)
  1. [Alignment](#alignment)
  1. [Quotes](#quotes)
  1. [Spacing](#spacing)
  1. [Props](#props)
  1. [Refs](#refs)
  1. [Parentheses](#parentheses)
  1. [Tags](#tags)
  1. [Methods](#methods)
  1. [Ordering](#ordering)
  1. [Third party library/packages](#third-party-library-packages)


## Basic Rules

  - Only include one React component per file.
    - However, multiple Stateless components are allowed per file.
    > Why? By doing this, we can read code quickly then fixing bugs or maintaining processes will be more efficiency.

  - Always use JSX syntax.
  - Do not use `React.createElement` unless you’re initializing the app from a file that is not JSX.

  - Defined types for every functions and components
    - With **Javascript Project**, always defined proptypes and default props.
    - With **Typescription Project**, try to avoid ***any*** or ***unknown*** type.
    > Why? By doing it, we will help other developers and ourself can manage types in good way and avoid unexpected bugs because of types. It is also a good document for us.

## Naming

  - **Extensions**: Use `.tsx` extension for Typescript React components.
  - **Filename**: Use camelCase for folder and non-component file names and PascalCase for component file names

    ```jsx
      E.g., `components/ListingCard.tsx` or `components/ListingCard.js`
      E.g., `utils/validateFormData.ts` or `utils/validateFormData.js`
    ```

  - **Reference Naming**: Use PascalCase for React components and camelCase for their instances.

    ```jsx
    // ❌
    import listingCard from 'components/ListingCard/ListingCard';

    // ✅
    import ListingCard from 'components/ListingCard/ListingCard';

    // ❌
    const ListingItem = <ListingCard />;

    // ✅
    const listingItem = <ListingCard />;
    ```

  - **Component Naming**: Use the filename as the component name. For example, `ListingCard.js` should have a reference name of `ListingCard`: It will help you easy to search the file. Try to avoid naming component file name is `index.js`.

    ```jsx
    // ❌
    import Footer from 'components/Footer/index';

    // ❌
    import Footer from 'components/Footer';

    // ✅
    import Footer from 'components/Footer/Footer';
    ```

  - **Higher-order Component Naming**: Use a composite of the higher-order component’s name and the passed-in component’s name as the `displayName` on the generated component. For example, the higher-order component `withFoo()`, when passed a component `Bar` should produce a component with a `displayName` of `withFoo(Bar)`.

    > Why? A component’s `displayName` may be used by developer tools or in error messages, and having a value that clearly expresses this relationship helps people understand what is happening.

    ```jsx
    // ❌
    export default function withFoo(WrappedComponent) {
      return function WithFoo(props) {
        return <WrappedComponent {...props} foo />;
      }
    }

    // ✅
    export default function withFoo(WrappedComponent) {
      function WithFoo(props) {
        return <WrappedComponent {...props} foo />;
      }

      const wrappedComponentName = WrappedComponent.displayName
        || WrappedComponent.name
        || 'Component';

      WithFoo.displayName = `withFoo(${wrappedComponentName})`;
      return WithFoo;
    }
    ```

  - **Props Naming**: Avoid using DOM component prop names for different purposes.

    > Why? People expect props like `style` and `className` to mean one specific thing. Varying this API for a subset of your app makes the code less readable and less maintainable, and may cause bugs.

    ```jsx
    // ❌
    <MyComponent style="fancy" />

    // ❌
    <MyComponent className="fancy" />

    // ✅
    <MyComponent variant="fancy" />
    ```
  
  - **Interface**, **Type**: in TS use Pascal case for Interface and Type.

  ```jsx
    interface UserType {
      //...
    }

    type userType {
      //...
    }
  ```

  - Use descriptive variable names

    ```jsx
    // ❌ Avoid single letter names
    const n = 'Max';
    // ✅
    const name = 'Max';

    // ❌ Avoid abbreviations
    const sof = 'Sunday';
    // ✅
    const startOfWeek = 'Sunday';

    // ❌ Avoid meaningless names
    const foo = false;
    // ✅
    const appInit = false;
    ```

## Class and Function components

  - Should use Function components with hooks.
    > It can help us easy to split logic, reuse logic, and easy to read code.
  - Don't need to convert old components writing in Class to Function components. However, if you have time and need to convert to reuse hooks, just do it, and please ensure it does not break any previous flow. :). If you have time, do some regression tests after converting.

  - Avoid Huge component: Whenever it is possible, split your component into smaller chunks. Often applicable when you are using conditional rendering or defining the columns for a data grid, etc. Also applicable when a lot of custom hooks are used — check the section above.

    ```jsx
    // ❌
    const SomeSection = ({ isEditable, value }) => {
      if (isEditable) {
        return (
          <Section>
            <Title>Edit this content</Title>
            <Content>{value}</Content>
            <Button>Clear content</Button>
          </Section>
        );
      }

      return (
        <Section>
          <Title>Read this content</Title>
          <Content>{value}</Content>
        </Section>
      );
    };

    // ✅
    const EditableSection = ({ value }) => {
      return (
        <Section>
          <Title>Edit this content</Title>
          <Content>{value}</Content>
          <Button>Clear content</Button>
        </Section>
      );
    };

    const DetailSection = ({ value }) => {
      return (
        <Section>
          <Title>Read this content</Title>
          <Content>{value}</Content>
        </Section>
      );
    };

    const SomeSection = ({ isEditable, value }) => {
      return isEditable ? (
        <EditableSection value={value} />
      ) : (
        <DetailSection value={value} />
      );
    };
    ```

  - Prefer conditional rendering with ternary operator

    ```jsx
    const { role } = user;

    // ❌
    if (role === ADMIN) {
      return <AdminUser />;
    } else {
      return <NormalUser />;
    }

    // ✅
    return role === ADMIN ? <AdminUser /> : <NormalUser />;
    ```

  - **Component structure**: To keep all the component files consistent, please follow the following pattern:

    ```jsx
      // 1. Imports - Prefer destructuring imports to minimize writen code. However in some case, I do not prefer destructuring imports because of performance (Lodash)
      import React, { PropsWithChildren, useState, useEffect } from "react";

      // 2. Types in Typescript
      type ComponentProps = {
        someProperty: string;
      };

      // 4. Additional variables
      const SOME_CONSTANT = "something";

      // 5. Component
      function Component({ someProperty }: PropsWithChildren<ComponentProps>) {
        // 5.1 Definitions
        const [state, setState] = useState(true);
        const { something } = useSomething();

        // 5.2 Functions
        function handleToggleState() {
          setState(!state);
        }

        // 5.3 Effects
        // ❌
        React.useEffect(() => {
          // ...
        }, []);

        // ✅
        useEffect(() => {
          // ...
        }, []);

        // 5.5 Additional destructures
        const { property } = something;

        return (
          <div>
            {/* Separate elements if not closed on the same line to make the code clearer */}
            {/* ❌ */}
            <div>
              <div>
                <p>Lorem ipsum</p>
                <p>Pellentesque arcu</p>
              </div>
              <p>Lorem ipsum</p>
              <p>Pellentesque arcu</p>
            </div>
            <div>
              <p>
                Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Pellentesque
                arcu. Et harum quidem rerum facilis est et expedita distinctio.
              </p>
              <p>Pellentesque arcu</p>
              <p>
                Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Pellentesque
                arcu. Et harum quidem rerum facilis est et expedita distinctio.
              </p>
            </div>

            {/* ✅ */}
            <HeaderInfo>
              <div>
                <p>Lorem ipsum</p>
                <p>Pellentesque arcu</p>
              </div>

              <p>Lorem ipsum</p>
              <p>Pellentesque arcu</p>
            </HeaderInfo>

            <ContentInfo>
              <div>
                <p>
                  Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
                  Pellentesque arcu. Et harum quidem rerum facilis est et expedita
                  distinctio.
                </p>

                <p>Pellentesque arcu</p>

                <p>
                  Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
                  Pellentesque arcu. Et harum quidem rerum facilis est et expedita
                  distinctio.
                </p>
              </div>
            </ContentInfo>
          </div>
        );
      }
    ```

  - Should use Fragment to wrap peer components in a conditional block.

    > Why? 
    > - Because it reduce nested elements => good performance
    > - Prevent break in layout => Save time.

    ```jsx
    // ❌
    const ActionButtons = ({ text1, text2 }) => {
      return (
        <div>
          <button>{text1}</button>
          <button>{text2}</button>
        </div>
      );
    };

    // ✅
    const Button = ({ text1, text2 }) => {
      return (
        <>
          <button>{text1}</button>
          <button>{text2}</button>
        </>
      );
    };
    ```

## Hooks
  - Should use custom hook when needed to make logic clear and easy to reuse.
    
    > How? To separate the responsibilities, first of all you should create custom hooks instead of just putting a useEffect or multiple useStates directly to your component.

    ```jsx
    function HomePage() {
      const [windowSize, setWindowSize] = useState({
        width: undefined,
        height: undefined,
        isMobileLayout: false,
        isDesktopHDLayout: false,
        isTabletLayout: false,
      });

      useEffect(() => {
        // only execute all the code below in client side
        if (typeof window !== 'undefined') {
          const handleResize = () => {
            let isMobileLayout = false;
            let isDesktopHDLayout = false;
            let isTabletLayout = false;
            if (window.innerWidth < MAX_MOBILE_SCREEN_WIDTH) {
              isMobileLayout = true;
            } else {
              isTabletLayout = true;
            }
            if (window.innerWidth >= DESKTOP_HD_SCREEN_WIDTH) {
              isDesktopHDLayout = true;
            }

            setWindowSize({
              width: window.innerWidth,
              height: window.innerHeight,
              isMobileLayout,
              isDesktopHDLayout,
              isTabletLayout,
            });
          };

          window.addEventListener('resize', handleResize);

          handleResize();

          return () => window.removeEventListener('resize', handleResize);
        }
      }, []);

      return (
        <div>Window size: ${windowSize.width}</div>
      )
    }

    // Hook
    export const useWindowSize = () => {
      const [windowSize, setWindowSize] = useState({
        width: undefined,
        height: undefined,
        isMobileLayout: false,
        isDesktopHDLayout: false,
        isTabletLayout: false,
      });

      useEffect(() => {
        // only execute all the code below in client side
        if (typeof window !== 'undefined') {
          const handleResize = () => {
            let isMobileLayout = false;
            let isDesktopHDLayout = false;
            let isTabletLayout = false;
            if (window.innerWidth < MAX_MOBILE_SCREEN_WIDTH) {
              isMobileLayout = true;
            } else {
              isTabletLayout = true;
            }
            if (window.innerWidth >= DESKTOP_HD_SCREEN_WIDTH) {
              isDesktopHDLayout = true;
            }

            setWindowSize({
              width: window.innerWidth,
              height: window.innerHeight,
              isMobileLayout,
              isDesktopHDLayout,
              isTabletLayout,
            });
          };

          window.addEventListener('resize', handleResize);

          handleResize();

          return () => window.removeEventListener('resize', handleResize);
        }
      }, []);
      return windowSize;
    };

    function HomePage() {
      const { width } = useWindowSize();

      return (
        <div>Window size: ${width}</div>
      )
    }
    ```

## Alignment

  - Follow these alignment styles for JSX syntax.

    ```jsx
    // ❌
    <Foo superLongParam="bar"
         anotherSuperLongParam="baz" />

    // ✅
    <Foo
      superLongParam="bar"
      anotherSuperLongParam="baz"
    />

    // if props fit in one line then keep it on the same line
    <Foo bar="bar" />

    // children get indented normally
    <Foo
      superLongParam="bar"
      anotherSuperLongParam="baz"
    >
      <Quux />
    </Foo>

    // ❌
    {showButton &&
      <Button />
    }

    // ❌
    {
      showButton &&
        <Button />
    }

    // ✅
    {showButton && (
      <Button />
    )}

    // ✅
    {showButton && <Button />}

    // ✅
    {someReallyLongConditional
      && anotherLongConditional
      && (
        <Foo
          superLongParam="bar"
          anotherSuperLongParam="baz"
        />
      )
    }

    // ✅
    {someConditional ? (
      <Foo />
    ) : (
      <Foo
        superLongParam="bar"
        anotherSuperLongParam="baz"
      />
    )}
    ```

## Quotes

  - Always use double quotes (`"`) for JSX attributes, but single quotes (`'`) for all other JS.

    > Why? Regular HTML attributes also typically use double quotes instead of single, so JSX attributes mirror this convention.

    ```jsx
    // ❌
    <Foo bar='bar' />

    // ✅
    <Foo bar="bar" />

    // ❌
    <Foo style={{ left: "20px" }} />

    // ✅
    <Foo style={{ left: '20px' }} />
    ```

  - Prefer using template literals

    ```jsx
    // ❌
    const userName = user.firstName + " " + user.lastName;

    // ✅
    const userDetails = `${user.firstName} ${user.lastName}`;
    ```

## Spacing

  - Always include a single space in your self-closing tag.

    ```jsx
    // ❌
    <Foo/>

    // very bad
    <Foo                 />

    // ❌
    <Foo
     />

    // ✅
    <Foo />
    ```

  - Do not pad JSX curly braces with spaces.

    ```jsx
    // ❌
    <Foo bar={ baz } />

    // ✅
    <Foo bar={baz} />
    ```

## Props

  - Avoid curly braces for string props:

    ```jsx
    // ❌
    <Title variant={"h1"} value={"Home page"} />

    // ✅
    <Title variant="h1" value="Home page" />
    ```

  - Should destructuring properties

    > Why? Because it is clear what properties are used in the component.

    ```jsx
    // ❌
    const Button = (props) => {
      return <button>{props.text}</button>;
    };

    // ✅
    const Button = (props) => {
      const { text } = props;

      return <button>{text}</button>;
    };

    // ✅
    const Button = ({ text }) => {
      return <button>{text}</button>;
    };
    ```

  - Always use camelCase for prop names, or PascalCase if the prop value is a React component.

    ```jsx
    // ❌
    <Foo
      UserName="hello"
      phone_number={12345678}
    />

    // ✅
    <Foo
      userName="hello"
      phoneNumber={12345678}
      Component={SomeComponent}
    />
    ```

  - Omit the value of the prop when it is explicitly `true`.

    ```jsx
    // ❌
    <Foo
      hidden={true}
    />

    // ✅
    <Foo
      hidden
    />

    // ✅
    <Foo hidden />
    ```

  - Always include an `alt` prop on `<img>` tags. If the image is presentational, `alt` can be an empty string or the `<img>` must have `role="presentation"`. The presentation role and its synonym none remove an element's implicit ARIA semantics from being exposed to the accessibility tree.

    ```jsx
    // ❌
    <img src="hello.jpg" />

    // ✅
    <img src="hello.jpg" alt="Me waving hello" />

    // ✅
    <img src="hello.jpg" alt="" />

    // ✅
    <img src="hello.jpg" role="presentation" />
    ```

  - Do not use words like "image", "photo", or "picture" in `<img>` `alt` props.

    > Why? Screenreaders already announce `img` elements as images, so there is no need to include this information in the alt text.

    ```jsx
    // ❌
    <img src="hello.jpg" alt="Picture of me waving hello" />

    // ✅
    <img src="hello.jpg" alt="Me waving hello" />
    ```

  - Use only valid, non-abstract [ARIA roles](https://www.w3.org/TR/wai-aria/#usage_intro).

    ```jsx
    // ❌ - not an ARIA role
    <div role="datepicker" />

    // ❌ - abstract ARIA role
    <div role="range" />

    // ✅
    <div role="button" />
    ```

  - Do not use `accessKey` on elements.

    > Why? Inconsistencies between keyboard shortcuts and keyboard commands used by people using screenreaders and keyboards complicate accessibility.

    ```jsx
    // ❌
    <div accessKey="h" />

    // ✅
    <div />
    ```

  - Avoid using an array index as `key` prop, prefer a stable ID.

    > Why? Not using a stable ID [is an anti-pattern](https://medium.com/@robinpokorny/index-as-a-key-is-an-anti-pattern-e0349aece318) because it can negatively impact performance and cause issues with component state.

  - We don’t recommend using indexes for keys if the order of items may change.

    ```jsx
    // ❌
    {todos.map((todo, index) =>
      <Todo
        {...todo}
        key={index}
      />
    )}

    // ✅
    {todos.map(todo => (
      <Todo
        {...todo}
        key={todo.id}
      />
    ))}
    ```

  - Always define explicit defaultProps for all non-required props.

    > Why? propTypes are a form of documentation, and providing defaultProps means the reader of your code doesn’t have to assume as much. In addition, it can mean that your code can omit certain type checks.

    ```jsx
    // ❌
    function Comp({ foo, bar, children }) {
      return <div>{foo}{bar}{children}</div>;
    }
    Comp.propTypes = {
      foo: PropTypes.number.isRequired,
      bar: PropTypes.string,
      children: PropTypes.node,
    };

    // ✅
    function Comp({ foo, bar, children }) {
      return <div>{foo}{bar}{children}</div>;
    }
    Comp.propTypes = {
      foo: PropTypes.number.isRequired,
      bar: PropTypes.string,
      children: PropTypes.node,
    };
    Comp.defaultProps = {
      bar: '',
      children: null,
    };
    ```

  - Use spread props sparingly.
  > Why? Otherwise you’re more likely to pass unnecessary props down to components. And for React v15.6.1 and older, you could [pass invalid HTML attributes to the DOM](https://reactjs.org/blog/2017/09/08/dom-attributes-in-react-16.html).

  Exceptions:

  - HOCs that proxy down props and hoist propTypes

    ```jsx
    function HOC(WrappedComponent) {
      return class Proxy extends React.Component {
        Proxy.propTypes = {
          text: PropTypes.string,
          isLoading: PropTypes.bool
        };

        render() {
          return <WrappedComponent {...this.props} />
        }
      }
    }
    ```

  - Spreading objects with known, explicit props. This can be particularly useful when testing React components with Mocha’s beforeEach construct.

    ```jsx
    export default function Foo {
      const props = {
        text: '',
        isPublished: false
      }

      return (<div {...props} />);
    }
    ```

  Notes for use:
  Filter out unnecessary props when possible.

    ```jsx
    // ❌
    render() {
      const { irrelevantProp, ...relevantProps } = this.props;
      return <WrappedComponent {...this.props} />
    } 

    // ✅
    render() {
      const { irrelevantProp, ...relevantProps } = this.props;
      return <WrappedComponent {...relevantProps} />
    }
    ```

  - Avoid using inline styles

    ```jsx
    // ❌
    const Title = (props) => {
      return (
        <h1 style={{ fontWeight: 600, fontSize: '24px' }} {...props}>
          {children}
        </h1>
      );
    };

    // ✅
    const useStyles = (props) => {
      return useMemo(
        () => ({
          header: { fontWeight: props.isBold ? 700 : 400, fontSize: "24px" }
        }),
        [props]
      );
    };

    const Title = (props) => {
      const styles = useStyles(props);

      return (
        <h1 style={styles.header} {...props}>
          {children}
        </h1>
      );
    };
    ```

## Refs

  - Always use ref callbacks or useRef.

    ```jsx
    // ❌
    <Foo
      ref="myRef"
    />

    // ✅
    <Foo
      ref={(ref) => { this.myRef = ref; }}
    />

    // ✅
    const fooRef = useRef();
    return <Foo ref={fooRef} />
    ```

## Parentheses

  - Wrap JSX tags in parentheses when they span more than one line.

    ```jsx
    // ❌
    render() {
      return <MyComponent variant="long body" foo="bar">
               <MyChild />
             </MyComponent>;
    }

    // ✅
    render() {
      return (
        <MyComponent variant="long body" foo="bar">
          <MyChild />
        </MyComponent>
      );
    }

    // ✅, when single line
    render() {
      const body = <div>hello</div>;
      return <MyComponent>{body}</MyComponent>;
    }
    ```

## Tags

  - Always self-close tags that have no children.

    ```jsx
    // ❌
    <Foo variant="stuff"></Foo>

    // ✅
    <Foo variant="stuff" />
    ```

  - If your component has multiline properties, close its tag on a new line.

    ```jsx
    // ❌
    <Foo
      bar="bar"
      baz="baz" />

    // ✅
    <Foo
      bar="bar"
      baz="baz"
    />
    ```

## Methods

  - Separate function from the JSX if it takes more than 1 line:

    ```jsx
    // ❌
    <button
      onClick={() => {
        setState(!state);
        resetForm();
        reloadData();
      }}
    />

    // ✅
    <button onClick={() => setState(!state)} />

    // ✅
    const handleButtonClick = () => {
      setState(!state);
      resetForm();
      reloadData();
    }

    <button onClick={handleButtonClick} />

    ```

  - Use arrow functions to close over local variables. It is handy when you need to pass additional data to an event handler. Although, make sure they [do not massively hurt performance](https://www.bignerdranch.com/blog/choosing-the-best-approach-for-react-event-handlers/), in particular when passed to custom components that might be PureComponents, because they will trigger a possibly needless rerender every time.

    ```jsx
    function ItemList(props) {
      return (
        <ul>
          {props.items.map((item, index) => (
            <Item
              key={item.key}
              onClick={(event) => { doSomethingWith(event, item.name, index); }}
            />
          ))}
        </ul>
      );
    }
    ```

  - Bind event handlers for the render method in the constructor.

    > Why? A bind call in the render path creates a brand new function on every single render. Do not use arrow functions in class fields, because it makes them [challenging to test and debug, and can negatively impact performance](https://medium.com/@charpeni/arrow-functions-in-class-properties-might-not-be-as-great-as-we-think-3b3551c440b1), and because conceptually, class fields are for data, not logic.

    ```jsx
    // ❌
    class extends React.Component {
      onClickDiv() {
        // do stuff
      }

      render() {
        return <div onClick={this.onClickDiv.bind(this)} />;
      }
    }

    // very bad
    class extends React.Component {
      onClickDiv = () => {
        // do stuff
      }

      render() {
        return <div onClick={this.onClickDiv} />
      }
    }

    // ✅
    class extends React.Component {
      constructor(props) {
        super(props);

        this.onClickDiv = this.onClickDiv.bind(this);
      }

      onClickDiv() {
        // do stuff
      }

      render() {
        return <div onClick={this.onClickDiv} />;
      }
    }
    ```

  - Do not use underscore prefix for internal methods of a React component.
    > Why? Underscore prefixes are sometimes used as a convention in other languages to denote privacy. But, unlike those languages, there is no native support for privacy in JavaScript, everything is public. Regardless of your intentions, adding underscore prefixes to your properties does not actually make them private, and any property (underscore-prefixed or not) should be treated as being public. See issues [#1024](https://github.com/airbnb/javascript/issues/1024), and [#490](https://github.com/airbnb/javascript/issues/490) for a more in-depth discussion.

    ```jsx
    // ❌
    React.createClass({
      _onClickSubmit() {
        // do stuff
      },

      // other stuff
    });

    // ✅
    class extends React.Component {
      onClickSubmit() {
        // do stuff
      }

      // other stuff
    }
    ```

  - Be sure to return a value in your `render` methods.

    ```jsx
    // ❌
    render() {
      (<div />);
    }

    // ✅
    render() {
      return (<div />);
    }
    ```

## Ordering

  - Ordering for `import`: Ordering import line by packages name. You can select all import lines then use CMD + Shift + P and select `Organize Import` to re-order import lines.
  

  - Ordering for `class extends React.Component`:

  1. optional `static` methods
  1. `constructor`
  1. `getChildContext`
  1. `componentWillMount`
  1. `componentDidMount`
  1. `componentWillReceiveProps`
  1. `shouldComponentUpdate`
  1. `componentWillUpdate`
  1. `componentDidUpdate`
  1. `componentWillUnmount`
  1. *event handlers starting with 'handle'* like `handleSubmit()` or `handleChangeDescription()`
  1. *event handlers starting with 'on'* like `onClickSubmit()` or `onChangeDescription()`
  1. *getter methods for `render`* like `getSelectReason()` or `getFooterContent()`
  1. *optional render methods* like `renderNavigation()` or `renderProfilePicture()`
  1. `render`

  - How to define `propTypes`, `defaultProps`, `contextTypes`, etc...

    ```jsx
    import React from 'react';
    import PropTypes from 'prop-types';

    const propTypes = {
      id: PropTypes.number.isRequired,
      url: PropTypes.string.isRequired,
      text: PropTypes.string,
    };

    const defaultProps = {
      text: 'Hello World',
    };

    class Link extends React.Component {
      static methodsAreOk() {
        return true;
      }

      render() {
        return <a href={this.props.url} data-id={this.props.id}>{this.props.text}</a>;
      }
    }

    Link.propTypes = propTypes;
    Link.defaultProps = defaultProps;

    export default Link;
    ```

## Third party library/packages

  - Don’t use third-party libraries directly: Instead of importing the third-party libraries directly, re-export them in one centralised place.

    > Why? Because it help us easy to plug and unplug library

    *src/lib/store.ts*

    ```export { useDispatch, useSelector } from 'react-redux';```

    *src/lib/query.ts*

    ```export { useQuery, useMutation, useQueryClient } from 'react-query';```



## Refs:

https://github.com/airbnb/javascript
https://levelup.gitconnected.com/react-code-conventions-and-best-practices-433e23ed69aa