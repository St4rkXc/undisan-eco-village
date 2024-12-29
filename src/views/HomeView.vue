<script setup>
import Button from 'primevue/button'
import Tabs from 'primevue/tabs'
import TabList from 'primevue/tablist'
import Tab from 'primevue/tab'
import TabPanels from 'primevue/tabpanels'
import TabPanel from 'primevue/tabpanel'
</script>

<template>
    <div>
        <h1 class="text-primary text-2xl font-bold">Home</h1>
        <p>Home page content</p>
        <Button
            label="Search"
            pt:root="bg-teal-500 hover:bg-teal-700 active:bg-teal-900 cursor-pointer py-2 px-4 rounded-full border-0 flex gap-2"
            pt:label="text-white font-bold text-lg"
        />
        <Tabs value="0" pt:root="bg-blue-500">
            <TabList pt:activeBar="bg-primary">
                <Tab value="0" pt:root="flex-1 text-center py-2 border-primary/20 hover:text-primary cursor-pointer bg-base-100" pt:active=" text-white"> Header I </Tab>
                <Tab value="1" pt:root="flex-1 text-center py-2 border-primary/20 hover:text-primary cursor-pointer bg-base-100" pt:active=" text-white"> Header II </Tab>
                <Tab value="2" pt:root="flex-1 text-center py-2 border-primary/20 hover:text-primary cursor-pointer bg-base-100" pt:active=" text-white"> Header III </Tab>
            </TabList>
            <TabPanels pt:root="p-4 bg-base-100">
                <TabPanel value="0">
                    <p class="text-primary">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.
                    </p>
                </TabPanel>
                <TabPanel value="1">
                    <p class="text-primary">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam.</p>
                </TabPanel>
                <TabPanel value="2">
                    <p class="text-primary">
                        At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores.
                    </p>
                </TabPanel>
            </TabPanels>
        </Tabs>
    </div>
</template>
