<template>
  <div class="layout">
        <Layout>
            <Header>
                <Menu mode="horizontal" theme="dark" active-name="1">
                        <MenuItem name="titel">
                            <Icon type="ios-stats"></Icon>
                            諾·测试管理平台
                        </MenuItem>
                    <div class="layout-nav">
                        <MenuItem name="1">
                            <Select v-model="model1" style="width:200px">
                                <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
                            </Select>
                        </MenuItem>
                    </div>
                </Menu>
            </Header>
            <Layout>
                <Sider hide-trigger :style="{background: '#fff'}">
                    <Menu active-name="1-2" theme="light" width="auto" :open-names="['1']">
<!--                        <Submenu name="1">-->
                            <MenuItem name="1">
                                <Icon type="ios-home"></Icon>
                                首页
                            </MenuItem>
<!--                        </Submenu>-->
                        <Submenu name="2">
                            <template slot="title">
                                <Icon type="ios-bug"></Icon>
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
                                <Icon type="md-analytics"></Icon>
                                性能测试
                            </template>
                            <MenuItem name="3-1">测试用例</MenuItem>
                            <MenuItem name="3-2">测试集</MenuItem>
                            <MenuItem name="3-3">执行测试</MenuItem>
                            <MenuItem name="3-4">测试报告</MenuItem>
                        </Submenu>
                        <Submenu name="4">
                            <template slot="title">
                                <Icon type="logo-chrome"></Icon>
                                webUI测试
                            </template>
                            <MenuItem name="4-1">页面元素管理</MenuItem>
                            <MenuItem name="4-2">测试用例</MenuItem>
                            <MenuItem name="4-3">测试集</MenuItem>
                            <MenuItem name="4-4">执行测试</MenuItem>
                            <MenuItem name="4-5">测试报告</MenuItem>
                        </Submenu>
                        <Submenu name="5">
                            <template slot="title">
                                <Icon type="ios-time" />
                                测试计划安排
                            </template>
                            <MenuItem name="5-1">任务计划</MenuItem>
                        </Submenu>
                        <Submenu name="6">
                            <template slot="title">
                                <Icon type="ios-paper" />
                                日志
                            </template>
                            <MenuItem name="6-1">接口测试</MenuItem>
                            <MenuItem name="6-2">性能测试</MenuItem>
                            <MenuItem name="6-3">webUI测试</MenuItem>
                            <MenuItem name="6-4">任务计划</MenuItem>
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

<style lang="scss">
.layout{
    border: 1px solid #d7dde4;
    background: #f5f7f9;
    position: relative;
    border-radius: 4px;
    overflow: hidden;
    height: 100%;
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
.ivu-layout{
    height: 100%;
}
html{
height: 100%;
}
body{
height: 100%;
}
</style>
<script>
    export default {
        data () {
            return {
                cityList: [
                    {
                        value: '项目1',
                        label: '项目1'
                    },
                    {
                        value: '项目2',
                        label: '项目2'
                    },
                    {
                        value: '项目3',
                        label: '项目3'
                    },
                    {
                        value: '项目4',
                        label: '项目4'
                    }
                ],
                model1: ''
            }
        }
    }
</script>