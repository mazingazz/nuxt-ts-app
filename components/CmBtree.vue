<template>
  <div>
    <client-only>
      <b-tree-view
        :data="treeData"
        :contextMenu="false"
        :nodesDraggable="false"
        :showIcons="false"
        :renameNodeOnDblClick="false"
        :contextMenuItems="[]"
        @nodeSelect="nodeSelect"
      >
      </b-tree-view>
    </client-only>
  </div>
</template>
<script lang="ts">
import { Vue, Component, namespace } from "nuxt-property-decorator";

@Component({
  components: {},
})
export default class User extends Vue {
  private treeData: any = [
    {
      id: 2,
      name: "Venus",
      children: [
        { id: 3, name: "Neptune" },
        { id: 4, name: "Stratus" },
      ],
    },
  ];
  mounted() {}
  private nodeSelect() {}
}
</script>