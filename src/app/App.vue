<script lang="ts">
import { AppFolder, AppFile, FuncRecycleBin } from '@/shared/ui'
import { EntityContextMenu } from '@/features/entity-context-menu'
import { AppHeader } from '@/widgets/header'
import { MainPageTitle } from '@/widgets/main-page-title'

export default {
  components: { AppFolder, AppFile, EntityContextMenu, AppHeader, FuncRecycleBin, MainPageTitle },
  data() {
    return {
      activeFile: null as null | number,
      isCtxMenuActive: false as boolean,
      pageX: 0 as number,
      pageY: 0 as number,
      files: [
        {
          id: 0,
          type: 'file',
          title: 'Nr.XLS'
        },
        {
          id: 1,
          type: 'folder',
          title: 'New folder'
        },
        {
          id: 2,
          type: 'folder',
          title: 'open'
        },
        {
          id: 3,
          type: 'folder',
          title: '777'
        },
        {
          id: 4,
          type: 'folder',
          title: '666'
        },
        {
          id: 5,
          type: 'file',
          title: 'Nr.XLS'
        },
        {
          id: 6,
          type: 'folder',
          title: '777'
        },
        {
          id: 7,
          type: 'file',
          title: '666'
        },
        {
          id: 8,
          type: 'folder',
          title: 'Nr.XLS'
        },
        {
          id: 9,
          type: 'folder',
          title: 'New folder'
        },
        {
          id: 10,
          type: 'folder',
          title: 'open'
        },
        {
          id: 11,
          type: 'folder',
          title: '777'
        },
        {
          id: 12,
          type: 'folder',
          title: '666'
        },
        {
          id: 13,
          type: 'file',
          title: 'Nr.XLS'
        }
      ]
    }
  },
  methods: {
    activateFileCtxMenu(e: MouseEvent, fileId: number): void {
      if (this.isCtxMenuActive && this.activeFile === fileId) {
        this.activeFile = null
        this.isCtxMenuActive = false
        return
      }
      this.isCtxMenuActive = true
      this.activeFile = fileId
      this.pageX = e.pageX
      this.pageY = e.pageY
    }
  }
}
</script>

<template>
  <app-header />
  <main-page-title />
  <div class="containerApp">
    <div v-for="file in files" :key="file.id">
      <app-file
        v-if="file.type === 'file'"
        :title="file.title"
        :is-active="file.id === activeFile"
        @click="(e) => activateFileCtxMenu(e, file.id)"
      />
      <app-folder
        v-else
        :title="file.title"
        :is-active="file.id === activeFile"
        @click="(e) => activateFileCtxMenu(e, file.id)"
      />
    </div>
  </div>

  <func-recycle-bin class="recycle-bin" />
  <entity-context-menu :page-x="pageX" :page-y="pageY" :is-active="isCtxMenuActive" />
</template>

<style lang="scss">
@import './index.scss';

.containerApp {
  margin: 0px 50px;
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  gap: 17px;
}

.recycle-bin {
  position: absolute;
  bottom: 32px;
  right: 140px;
}
</style>
