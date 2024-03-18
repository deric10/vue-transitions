<template>
  <div
    class="flex py-5 px-5 text-amber-700 justify-center text-2xl font-bold font-mono items-center h-dvh m-4"
  >
    <h1>Hi deric@dev!!</h1>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped></style>
<!--
Directives: v-for,if,show,on,bind,memo,once,pre,if/else,html,text and v-slot
Life cycle hooks: onBeforeUnmount,onMounted amd unUnmounted,onBeforeMount,onActivate and onDeactivate,onBeforeUpdate and onUpdate,
Components:

  <Transition/> || <TransitionGroup/> : Events{ beforeEnter,beforeLeave,enter,leave,appear,afterEnter,afterLeave and leave,enter and appear cancellation }
  otherAttributes: name,mode,appear[boolean],tag and move , styles{
  enterFromClass  |  enterActiveClass  |  enterToClass
  appearFromClass | appearActiveClass  | appearToClass
  leaveFromClass  | leaveActiveClass   | leaveToClass
   }

  <Keep-Alive/>: it saves a component state and reduce un-necessary API-calls
  Other options are include & exclude ,max

  <Teleport/> : Render html contents into other-part to the dom and it allows to=>specific id-container and disabled if condition
  <Suspense/>

  <Special Elements/> :
  <component/>: A meta component to render dynamic components through use of is attribute
  <Slot/>
  <template/> : using directives as v-if,if/else,for and v-slot.

  <Special Element/> :
  key: used as hint to vue Virtual Dom and expected to be int|string|symbol
  is: binding dynamic components,

  <Reactivity/>:
  ref: takes value and return reactive object version of the value that located in the .value
  reactive: return reactive proxy of the object
  computed: it takes a value object and return readonly object, But also allows you to define getter and setter
  separated to allows it to be writable
  watch: watches one or more reactive data sources and invokes callback when reactive value changes
         watch is lazy by default and accepting three arguments that is ['source','callback','options']
         source :{getterFunction, ref, reactiveObject,array}
         callback : it accepts 'newValue','oldValue' and 'function for registering side effects clean-up callback'
  watchEffects: function run immediately while reactively tracking its dependencies and re-runs it whenever the dependencies are changed {post,sync}
  readonly: takes an object (reactive or plain) or a ref and returns a readonly proxy to the original
  watchPostEffect:
  watchSyncEffect:

  Dependency Injection: provides a value that can be injected by descendant components. [
  provide: {'key' and 'value' },
  inject: injecting in to child components using provided 'key' to get provided value

  Reactive : Utilities
  ref: Normalize value into reactive version.
  toRef: Used to normalize values,refs and getters into refs and also can create ref for a property and referencing to the original source object or value
  unRef: Returns the inner value if the argument is a ref, otherwise return the argument itself.
  toValue: Normalizes values / refs / getters to values. This is similar to unref(), except that it also normalizes getters. If the argument is a getter, it will be invoked and its return value will be returned.
  toRefs: Converts a reactive object to a plain object where each property of the resulting object is a ref pointing to the corresponding property of the original object
  isProxy: Checks if an object is a proxy created by reactive(), readonly(), shallowReactive() or shallowReadonly().
  isReactive: Checks if an object is a proxy created by reactive() or shallowReactive().
  isReadonly: Checks whether the passed value is a readonly object. The properties of a readonly object can change, but they can't be assigned directly via the passed object.

  Advanced Reactivity:
   shallowRef: Mostly useful for performance optimizing/ it achieve that by make deep inner data not reactive
   triggerRef: Used along shallowRef to trigger shallowRef value to make deep mutation to the inner value of the shallowRef


   Priority:
   1:Component name should be multi-word eg: MyComponent or my-component
   2:Order of words in components should be considered as start generic and end with specific and should be in full-words
   components:
      |- TodoList.vue
      |- TodoListItem.vue
      |- TodoListItemButton.vue
   3:Components Instance Order:
   Global awareness {name},
   Template compiler options: {compilerOptions},
   Template dependency: {component, directives},
   composition: {extends,mixins and provide-inject},
   interface: {inheritAttrs, props and emit},
   Composition API: {setup},
   Local state:{ data,computed},
   Events: {watch,lifecycle-event},
   Non-reactive properties :{method},
   Rendering: {template, render}

   Element attribute order:
   Definition: is,{is}
   List Rendering, {v-for}
   Conditional: {v-cloak,v-if,v-if/else,v-if/elseif/else,v-show}
   Render modifier:{v-pre,v-once}
   Global awareness:{id}
   Unique Attributes:{ref,key}
   Two way binding:{v-model}
   Other attributes:{all unspecified bound & unbound attributes}
   Events: {:on}
   Content: {:text,:html}

  In-styling html elements we make use of id and classes but not it actual element tag
  Avoid using v-for with v-if:
  example:
        <ul>
        <template v-for="user in users" :key="user.id">
          <li v-if="user.isActive">
            {{ user.name }}
          </li>
        </template>
      </ul>

  Base components are {Base,App and v.[name]},
  Template is used to present data in simple complexity and let all other heavy-duty-task to computed properties,
  Cleaner method and computed properties is should be readable,testable and adoptable,
  Attributes must be in double-quotes eg id="thisIsId",
  Defining props should be in camelCase and kebab-case in template
  Defining props in composition API:
  props: {
    status: {
      type: String,
      required: true,

      validator: value => {
        return [
          'syncing',
          'synced',
          'version-conflict',
          'error'
        ].includes(value)
      }
    }
  }
  Props and Emits:
  Slots:
  Async Components:
-->
