<template>
        <div>
            <a :href="`mailto:${field.value}`"
                v-if="clickable && field.value"
                class="cursor-pointer dim no-underline text-primary inline-flex items-center"
                target="_blank"
            >
                <svg xmlns="http://www.w3.org/2000/svg"
                    class="fill-current mr-2"
                    width="16"
                    height="16"
                    viewBox="0 0 24 24"
                    role="presentation"
                >
                    <path d="M4 4h16a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V6c0-1.1.9-2 2-2zm16 3.38V6H4v1.38l8 4 8-4zm0 2.24l-7.55 3.77a1 1 0 0 1-.9 0L4 9.62V18h16V9.62z"/>
                </svg>

                <span>
                    {{ field.value }}
                </span>
            </a>
            <span v-else-if="field.value">{{ field.value }}</span>
            <span v-else>&mdash;</span>
        </div>
</template>

<script>
export default {
    props: ['resource', 'resourceName', 'resourceId', 'field', 'clickable'],
}
</script>
