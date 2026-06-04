<script lang="ts">
  import { cleanClass } from '$lib';
  import noThumbnailUrl from '$lib/assets/no-thumbnail.png';

  interface Props {
    alt?: string;
    preload?: boolean;
    class?: string;
  }

  let { alt = '', preload = false, class: className }: Props = $props();
</script>

<img
  {alt}
  class={cleanClass('size-full rounded-xl object-cover aspect-square', className)}
  data-testid="album-image"
  draggable="false"
  loading={preload ? 'eager' : 'lazy'}
  src={noThumbnailUrl}
/>
