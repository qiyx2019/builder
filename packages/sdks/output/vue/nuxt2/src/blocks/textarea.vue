<template>
  <textarea
    v-bind="attributes"
    :placeholder="placeholder"
    :name="name"
    :value="value"
    :defaultValue="defaultValue"
  ></textarea>
</template>
<script>
import { registerComponent } from "../functions/register-component";

export default registerComponent(
  {
    name: "builder-textarea",

    props: ["attributes", "placeholder", "name", "value", "defaultValue"],
  },
  {
    name: "Form:TextArea",
    builtIn: true,
    image:
      "https://cdn.builder.io/api/v1/image/assets%2FIsxPKMo2gPRRKeakUztj1D6uqed2%2Ff74a2f3de58c4c3e939204e5b6b8f6c3",
    inputs: [
      { advanced: true, name: "value", type: "string" },
      {
        name: "name",
        type: "string",
        required: true,
        helperText:
          'Every input in a form needs a unique name describing what it gets, e.g. "email"',
      },
      { name: "defaultValue", type: "string" },
      { name: "placeholder", type: "string", defaultValue: "Hello there" },
      { name: "required", type: "boolean", defaultValue: false },
    ],
    defaultStyles: {
      paddingTop: "10px",
      paddingBottom: "10px",
      paddingLeft: "10px",
      paddingRight: "10px",
      borderRadius: "3px",
      borderWidth: "1px",
      borderStyle: "solid",
      borderColor: "#ccc",
    },
    static: true,
    noWrap: true,
  }
);
</script>
