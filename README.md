 webprogramming_lab6 - Sri Harshini Jilloju - N01649103

 # Angular Tutorial Notes (Chapters 1-9)

## Chapter 1: Components in Angular

**What are Components?**
- Components are the foundational building blocks of Angular applications
- Each component has three essential parts:
  - **TypeScript class** - Contains the logic and data
  - **HTML template** - Defines the view structure
  - **CSS styles** - Controls the appearance

**Key Concepts:**
- Components define reusable pieces of UI
- Template property contains the HTML content
- Styles property contains CSS styling
- Use `:host` selector to style the component itself
- Angular supports all standard HTML and CSS features

## Chapter 2: Composing Components

**Component Composition:**
- Components can be nested inside other components
- Parent components can contain child components
- Import child components in the parent component
- Use component selectors as HTML tags
- Components communicate through inputs and outputs

**Benefits:**
- Code reusability
- Better organization
- Easier maintenance
- Modular architecture

## Chapter 3: Control Flow - @if

**Conditional Rendering:**
- Use `@if` directive for conditional content display
- Syntax: `@if (condition) { content }`
- Can include `@else` blocks for alternative content
- Replaces the older `*ngIf` structural directive
- Conditions can be any boolean expression

**Use Cases:**
- Show/hide elements based on user state
- Display different content for different user roles
- Toggle between loading and content states

## Chapter 4: Control Flow - @for

**Iterating Over Data:**
- Use `@for` directive to loop through arrays or collections
- Syntax: `@for (item of items; track item.id) { content }`
- `track` expression is required for performance optimization
- Replaces the older `*ngFor` structural directive
- Can access index and other loop variables

**Best Practices:**
- Always provide a track expression
- Use unique identifiers when possible
- Keep track expressions simple and efficient

## Chapter 5: Event Handling

**Handling User Interactions:**
- Use parentheses syntax: `(event)="handler()"`
- Common events: click, submit, input, change
- Event handlers are methods in the component class
- Can pass event data: `(click)="handler($event)"`
- Access event properties like `target.value`

**Event Types:**
- Mouse events: click, mouseenter, mouseleave
- Keyboard events: keyup, keydown, keypress
- Form events: submit, input, change
- Custom events from child components

## Chapter 6: Property Binding

**Data Binding Basics:**
- Use square brackets for property binding: `[property]="value"`
- Binds component properties to template elements
- One-way data flow from component to template
- Can bind to HTML attributes, DOM properties, and directive inputs
- Expressions are evaluated in component context

**Common Use Cases:**
- Setting element properties dynamically
- Passing data to child components
- Controlling CSS classes and styles
- Binding to directive inputs

## Chapter 7: Pipes

**Data Transformation:**
- Pipes transform displayed data without changing the original
- Use pipe operator: `{{ value | pipeName }}`
- Chain multiple pipes: `{{ value | pipe1 | pipe2 }}`
- Pass parameters: `{{ value | pipeName:param1:param2 }}`

**Built-in Pipes:**
- `date` - Format dates
- `currency` - Format currency values
- `uppercase/lowercase` - Text case conversion
- `json` - Display objects as JSON
- `slice` - Extract portions of arrays/strings

**Custom Pipes:**
- Create custom transformation logic
- Implement PipeTransform interface
- Use @Pipe decorator
- Pure vs impure pipes for performance

## Chapter 8: Dependency Injection

**Service Architecture:**
- Services provide shared functionality across components
- Use dependency injection to access services
- Inject services through constructor parameters
- Mark services with `@Injectable()` decorator
- Provide services in component or module

**Benefits:**
- Code reusability
- Separation of concerns
- Easier testing
- Better maintainability

**Service Types:**
- Data services for API communication
- Utility services for common functions
- State management services
- Business logic services

## Chapter 9: Input and Output

**Component Communication:**

**@Input() - Parent to Child:**
- Use `@Input()` decorator for properties
- Parent passes data through property binding
- Child receives data as component properties
- Can set default values and validation

**@Output() - Child to Parent:**
- Use `@Output()` decorator with EventEmitter
- Child emits custom events to parent
- Parent listens using event binding syntax
- Can pass data with emitted events

**Communication Patterns:**
- Parent-child: Use @Input and @Output
- Sibling components: Use shared service
- Distant components: Use state management
- Two-way binding: Combine @Input and @Output




