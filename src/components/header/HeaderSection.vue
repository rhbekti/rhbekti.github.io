<script setup lang="ts">
import {
  NavigationMenu,
  NavigationMenuItem,
  NavigationMenuLink,
  NavigationMenuList,
} from '@/components/ui/navigation-menu'
import ModeToggle from '../ModeToggle.vue';
</script>

<template>
  <header class="fixed top-0 z-40 w-full">
    <div class="border-b backdrop-blur-xl">
      <nav class="mx-auto flex h-14 max-w-5xl items-center justify-between px-6">
        <a class="font-mono text-sm font-semibold tracking-tight uppercase text-foreground transition-colors hover:text-primary"
          href="/">RHBEKTI</a>
        <div>
          <NavigationMenu>
            <NavigationMenuList>
              <NavigationMenuItem>
                <NavigationMenuLink href="/">Home</NavigationMenuLink>
              </NavigationMenuItem>
              <NavigationMenuItem>
                <NavigationMenuLink href="/">Works</NavigationMenuLink>
              </NavigationMenuItem>
              <NavigationMenuItem>
                <NavigationMenuLink href="/">Blogs</NavigationMenuLink>
              </NavigationMenuItem>
              <NavigationMenuItem>
                <NavigationMenuLink href="/">About</NavigationMenuLink>
              </NavigationMenuItem>
            </NavigationMenuList>
          </NavigationMenu>
        </div>
        <div>
          <ModeToggle />
        </div>
      </nav>
    </div>
  </header>
</template>
