<script setup lang="ts">
import Button from '@/components/ui/button/Button.vue';
import Input from '@/components/ui/input/Input.vue';
import Label from '@/components/ui/label/Label.vue';
import AppLayout from '@/layouts/AppLayout.vue';
import { type BreadcrumbItem } from '@/types';
import { Head } from '@inertiajs/vue3';

const breadcrumbs: BreadcrumbItem[] = [
    {
        title: 'Create a Product',
        href: '/products/create',
    },
];

defineProps<{
    name?: string;
}>();
</script>

<template>
    <Head title="Create a Product" />

    <AppLayout :breadcrumbs="breadcrumbs">
        <div class="p-4">
            <form  class="w-8/12 space-y-2">
                <div class="space-y-2">
                    <Label for="Product Name">Name</Label>
                    <Input type="text" placeholder="Name" />
                </div>
                 <div class="space-y-2">
                    <Label for="Product Price">Price</Label>
                    <Input type="number" placeholder="Price" />
                </div>
                 <div class="space-y-2">
                    <Label for="Product Description">Description</Label>
                    <Input type="text" placeholder="Description" />
                </div>
                <Button type="submit">Add a Product</Button>
            </form>
        </div>
    </AppLayout>
</template>