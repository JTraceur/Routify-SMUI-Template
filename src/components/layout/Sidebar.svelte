<script>
    // SMUI
    import Drawer, { Content } from '@smui/drawer';
    import List, { Item, Text, Graphic } from '@smui/list';
</script>

<Drawer style="width: 100%">
    <Content>
        <List>
            <!-- Classes -->
            <Item>
                <Graphic class="material-icons">school</Graphic>
                <Text>
                    Classes
                </Text>
            </Item>

            <!-- Students -->
            <Item>
                <Graphic class="material-icons">people</Graphic>
                <Text>
                    Students
                </Text>
            </Item>

            <!-- Staff -->
            <Item>
                <Graphic class="material-icons">work</Graphic>
                <Text>
                    Staff
                </Text>
            </Item>
        </List>
    </Content>
</Drawer>
