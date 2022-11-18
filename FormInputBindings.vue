
<!-- Form Input Binding -->

<!-- The v-model Directive -->

<input v-model="text">

<p>Message is: {{ message }}</p>
<input v-model="message" placeholder="edit me" />

<span>Multiline message is:</span>
<p style="white-space: pre-line;">{{ message }}</p>
<textarea v-model="message" placeholder="add multiple lines"></textarea>

<input type="checkbox" id="checkbox" v-model="checked" />
<label for="checkbox">{{ checked }}</label>

export default {
  data() {
    return {
      checkedNames: []
    }
  }
}

<div>Checked names: {{ checkedNames }}</div>

<input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
<label for="jack">Jack</label>

<input type="checkbox" id="john" value="John" v-model="checkedNames">
<label for="john">John</label>

<input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
<label for="mike">Mike</label>

<!-- synced after "change" instead of "input" -->
<input v-model.lazy="msg" />

<input v-model.number="age" />

<input v-model.trim="msg" />
