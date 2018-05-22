### table基础使用
```

<Grid txt="/admin/store/list" @dataWrap="renderData" :valueArr="valueArr" :q="q">
      <el-header slot="formSearch" height="50px">
        <el-row :gutter="20">
          <el-col :span="3">
            <el-input placeholder="门店名称" v-model="q.storeName" clearable></el-input>
          </el-col>
          <el-col :span="3">
            <el-input placeholder="联系电话" v-model="q.storePhone" clearable></el-input>
          </el-col>
          <el-col :span="3">
            <el-button type="primary" @click="search">搜索</el-button>
            <el-button type="default" @click="search('reset')">重置</el-button>
          </el-col>
          <el-col :span="3" :offset="12">
            <el-button type="primary" @click="addStore">新增</el-button>
          </el-col>
        </el-row>
      </el-header>

      <el-table-column
              slot="columns"
              type="index"
              width="50">
      </el-table-column>

      <el-table-column
              slot="columns"
              label="门店名称"
              width="180">
        <template slot-scope="scope">
          <span>{{ scope.row.storeName}}</span>
        </template>
      </el-table-column>

      <el-table-column
              slot="columns"
              label="所在地区"
              width="180">
        <template slot-scope="scope">
          <span>{{ scope.row.storeProvince }}-{{scope.row.storeCity}}-{{scope.row.storeCounty}}</span>
        </template>
      </el-table-column>

      <el-table-column
              slot="columns"
              label="详细地址"
              width="180">
        <template slot-scope="scope">
          <span>{{ scope.row.storeAddress }}</span>
        </template>
      </el-table-column>

      <el-table-column
              slot="columns"
              label="联系电话"
              width="180">
        <template slot-scope="scope">
          <span>{{ scope.row.storePhone }}</span>
        </template>
      </el-table-column>

      <el-table-column
              slot="columns"
              label="负责人"
              width="100">
        <template slot-scope="scope">
          <span>{{ scope.row.storeCharge }}</span>
        </template>
      </el-table-column>

      <el-table-column
              slot="columns"
              label="状态"
              width="60">
        <template slot-scope="scope">
          <span>{{ scope.row.storeStatus | storeStatus}}</span>
        </template>
      </el-table-column>

      <el-table-column
              slot="columns"
              label="操作">
        <template slot-scope="scope">
          <el-button type="info" @click="forbidden(scope.$index, scope.row)">禁用</el-button>
          <el-button type="info" @click="editStore(scope.$index, scope.row)">编辑</el-button>
        </template>
      </el-table-column>

    </Grid>

    <script>
       export default{
         data(){
            return{
                valueArr: [],
                q: {},
                loading: false
            }
         },
       }
    </script>

```