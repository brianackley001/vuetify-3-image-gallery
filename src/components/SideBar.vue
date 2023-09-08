<template>
  <VNavigationDrawer expand-on-hover rail>
    <VList>
      <VListItem prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg" title="Git HubStuff"
        subtitle="randomstuff@gmailcom"></VListItem>
    </VList>
    <VList density="compact" nav>
      <VListItem prepend-icon="mdi-folder" title="My Files" value="myfiles"></VListItem>
      <VListItem prepend-icon="mdi-account-multiple" title="Shared with me" value="shared"></VListItem>
      <VListItem prepend-icon="mdi-star" title="Starred" value="starred"></VListItem>
    </VList>

  </VNavigationDrawer>
</template>