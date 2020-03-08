<!--<template>-->
<!--  <div class="home">-->
<!--    <img alt="Vue logo" src="../assets/logo.png">-->
<!--    <HelloWorld msg="Welcome to Your Vue.js App"/>-->
<!--       <Button>Default</Button>-->
<!--    <Button type="primary">Primary</Button>-->
<!--    <Button type="dashed">Dashed</Button>-->
<!--    <Button type="text">Text</Button>-->
<!--  </div>-->
  <style scoped>
.layout{
    border: 1px solid #d7dde4;
    background: #f5f7f9;
    position: relative;
    border-radius: 4px;
    overflow: hidden;
}
.layout-logo{
    width: 100px;
    height: 30px;
    background: #5b6270;
    border-radius: 3px;
    float: left;
    position: relative;
    top: 15px;
    left: 20px;
}
.layout-nav{
    width: 420px;
    margin: 0 auto;
    margin-right: 20px;
}
      .layout{
          height: 100%;
      }
</style>
<template>
    <div class="layout">
        <Layout>
            <Header>
                <Menu mode="horizontal" theme="dark" active-name="1">
                    <div class="layout-logo"></div>
                    <div class="layout-nav">
                        <MenuItem name="1">
                            <Icon type="ios-navigate"></Icon>
                            项目 1
                        </MenuItem>
                        <MenuItem name="2">
                            <Icon type="ios-keypad"></Icon>
                            项目 2
                        </MenuItem>
                        <MenuItem name="3">
                            <Icon type="ios-analytics"></Icon>
                            项目 3
                        </MenuItem>
                        <MenuItem name="4">
                            <Icon type="ios-paper"></Icon>
                            项目 4
                        </MenuItem>
                    </div>
                </Menu>
            </Header>
            <Layout>
                <Sider hide-trigger :style="{background: '#fff'}">
                    <Menu active-name="1-2" theme="light" width="auto" :open-names="['1']">
                        <Submenu name="1">
                            <template slot="title">
                                <Icon type="ios-navigate"></Icon>
                                首页
                            </template>
                        </Submenu>
                        <Submenu name="2">
                            <template slot="title">
                                <Icon type="ios-keypad"></Icon>
                                接口测试
                            </template>
                            <MenuItem name="2-1">接口管理</MenuItem>
                            <MenuItem name="2-2">测试用例</MenuItem>
                            <MenuItem name="2-3">测试集</MenuItem>
                            <MenuItem name="2-4">执行测试</MenuItem>
                            <MenuItem name="2-5">测试报告</MenuItem>
                        </Submenu>
                        <Submenu name="3">
                            <template slot="title">
                                <Icon type="ios-analytics"></Icon>
                                性能测试
                            </template>
                            <MenuItem name="3-1">测试用例</MenuItem>
                            <MenuItem name="3-2">测试集</MenuItem>
                            <MenuItem name="3-3">执行测试</MenuItem>
                            <MenuItem name="3-4">测试报告</MenuItem>
                        </Submenu>
                        <Submenu name="4">
                            <template slot="title">
                                <Icon type="ios-analytics"></Icon>
                                webUI测试
                            </template>
                            <MenuItem name="4-1">页面元素管理</MenuItem>
                            <MenuItem name="4-2">测试用例</MenuItem>
                            <MenuItem name="4-3">测试集</MenuItem>
                            <MenuItem name="4-4">执行测试</MenuItem>
                            <MenuItem name="4-5">测试报告</MenuItem>
                        </Submenu>
                    </Menu>
                </Sider>
                <Layout :style="{padding: '0 24px 24px'}">
                    <Breadcrumb :style="{margin: '24px 0'}">
                        <BreadcrumbItem>Home</BreadcrumbItem>
                        <BreadcrumbItem>Components</BreadcrumbItem>
                        <BreadcrumbItem>Layout</BreadcrumbItem>
                    </Breadcrumb>
                    <Content :style="{padding: '24px', minHeight: '280px', background: '#fff'}">
                        Content
                    </Content>
                </Layout>
            </Layout>
        </Layout>
    </div>
</template>
<script>
    export default {

    }
</script>

<!--</template>-->

<!--<script>-->
<!--// @ is an alias to /src-->
<!--import HelloWorld from '@/components/HelloWorld.vue'-->

<!--export default {-->
<!--  name: 'Home',-->
<!--  components: {-->
<!--    HelloWorld-->
<!--  }-->
<!--}-->
<!--</script>-->
