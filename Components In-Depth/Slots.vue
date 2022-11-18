
<!-- Slot Content and Outlet -->

FancyButton('Click me!')

function FancyButton(slotContent) {
  return `<button class="fancy-btn">
      ${slotContent}
    </button>`
}

<FancyButton>
    <span style="color:red">Click me!</span>
    <AwesomeIcon name="plus" />
  </FancyButton>
  
  <span>{{ message }}</span>
<FancyButton>{{ message }}</FancyButton>

<!-- Fallback Content -->

<button type="submit">
    <slot></slot>
  </button>
  
  <button type="submit">
    <slot>
      Submit 
    </slot>
  </button>
  
  <!-- Named Slots -->

  <div class="container">
    <header>
    </header>
    <main>
    </main>
    <footer>
    </footer>
  </div>
  
  <div class="container">
    <header>
      <slot name="header"></slot>
    </header>
    <main>
      <slot></slot>
    </main>
    <footer>
      <slot name="footer"></slot>
    </footer>
  </div>

<BaseLayout>
    <template #header>
      <h1>Here might be a page title</h1>
    </template>
  
    <p>A paragraph for the main content.</p>
    <p>And another one.</p>
  
    <template #footer>
      <p>Here's some contact info</p>
    </template>
  </BaseLayout>
  
<!-- Dynamic Slot Names -->

<base-layout>
  <template v-slot:[dynamicSlotName]>
    ...
  </template>

  <template #[dynamicSlotName]>
    ...
  </template>
</base-layout>

<MyComponent v-slot="{ text, count }">
    {{ text }} {{ count }}
  </MyComponent>
  
  <slot name="header" message="hello"></slot>
