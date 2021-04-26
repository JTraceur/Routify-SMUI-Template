<script>
    // SMUI
    import Drawer, { Content } from '@smui/drawer';
    import List, { Item, Text, Graphic } from '@smui/list';

    // Navigation service:
    import { goto } from '@roxi/routify'
</script>

<Drawer style="width: 100%">
    <Content>
        <List>
            <!-- Classes -->
            <Item on:click={() => $goto('./classrooms')}>
                <Graphic class="material-icons">school</Graphic>
                <Text>
                    Classes
                </Text>
            </Item>

            <!-- Students -->
            <Item on:click={() => $goto('./students')}>
                <Graphic class="material-icons">people</Graphic>
                <Text>
                    Students
                </Text>
            </Item>

            <!-- Staff -->
            <Item on:click={() => $goto('./staff')}>
                <Graphic class="material-icons">work</Graphic>
                <Text>
                    Staff
                </Text>
            </Item>
        </List>
    </Content>
</Drawer>
