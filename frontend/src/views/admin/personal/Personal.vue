<template>
  <a-row :gutter="20">
    <a-col :span="8" style="text-align: center;padding-top: 50px">
      <i style="font-size: 30px;text-align: center;">校企信息</i>
      <img alt="example" style="height: 500px;" src="/static/img/data.png"/>
    </a-col>
    <a-col :span="16">
      <a-card :loading="loading" :bordered="false">
        <a-form :form="form" layout="vertical">
          <a-row :gutter="20">
            <a-col :span="8">
              <a-form-item label='校企名称' v-bind="formItemLayout">
                <a-input v-decorator="[
            'name',
            { rules: [{ required: true, message: '请输入名称!' }] }
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='单位简称或代号' v-bind="formItemLayout">
                <a-input v-decorator="[
            'abbreviation',
            { rules: [{ required: true, message: '请输入单位简称!' }] }
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='统一社会信用代码' v-bind="formItemLayout">
                <a-input v-decorator="[
            'creditCode'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='单位性质' v-bind="formItemLayout">
                <a-input v-decorator="[
            'nature'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='二级校企单位性质' v-bind="formItemLayout">
                <a-input v-decorator="[
            'natureTwo'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='经营状态' v-bind="formItemLayout">
                <a-input v-decorator="[
            'status'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='法定代表人' v-bind="formItemLayout">
                <a-input v-decorator="[
            'corporateRepresentative'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='法定代表人身份证号' v-bind="formItemLayout">
                <a-input v-decorator="[
            'corporateRepresentativeId'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='法定代表人电话' v-bind="formItemLayout">
                <a-input v-decorator="[
            'corporateRepresentativePhone'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='注册资本（万元）' v-bind="formItemLayout">
                <a-input v-decorator="[
            'registeredCapital'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='注册资金币种' v-bind="formItemLayout">
                <a-input v-decorator="[
            'registeredCapitalCurrency'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='成立日期' v-bind="formItemLayout">
                <a-input v-decorator="[
            'establishmentDate'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='营业期限始期' v-bind="formItemLayout">
                <a-input v-decorator="[
            'businessBeginDate'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='营业期限止期' v-bind="formItemLayout">
                <a-input v-decorator="[
            'businessEndDate'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='注册地址' v-bind="formItemLayout">
                <a-input v-decorator="[
            'registeredAddress'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='经营范围' v-bind="formItemLayout">
                <a-input v-decorator="[
            'businessScope'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='省' v-bind="formItemLayout">
                <a-input v-decorator="[
            'province'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='市' v-bind="formItemLayout">
                <a-input v-decorator="[
            'city'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='区' v-bind="formItemLayout">
                <a-input v-decorator="[
            'district'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='英文校企名称' v-bind="formItemLayout">
                <a-input v-decorator="[
            'enName'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="8">
              <a-form-item label='所属行业' v-bind="formItemLayout">
                <a-input v-decorator="[
            'industry'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="24">
              <a-form-item label='单位简介' v-bind="formItemLayout">
                <a-textarea :rows="6" v-decorator="[
            'unitDescription'
            ]"/>
              </a-form-item>
            </a-col>
            <a-col :span="24">
              <a-form-item label='校企照片' v-bind="formItemLayout">
                <a-upload
                  name="avatar"
                  action="http://127.0.0.1:9527/file/fileUpload/"
                  list-type="picture-card"
                  :file-list="fileList"
                  @preview="handlePreview"
                  @change="picHandleChange"
                >
                  <div v-if="fileList.length < 1">
                    <a-icon type="plus" />
                    <div class="ant-upload-text">
                      Upload
                    </div>
                  </div>
                </a-upload>
                <a-modal :visible="previewVisible" :footer="null" @cancel="handleCancel">
                  <img alt="example" style="width: 100%" :src="previewImage" />
                </a-modal>
              </a-form-item>
            </a-col>
          </a-row>
        </a-form>
        <a-button key="submit" type="primary" :loading="loading" @click="handleSubmit">
          修改
        </a-button>
      </a-card>
    </a-col>
    <a-col :span="8"></a-col>
  </a-row>
</template>

<script>
import {mapState} from 'vuex'

function getBase64 (file) {
  return new Promise((resolve, reject) => {
    const reader = new FileReader()
    reader.readAsDataURL(file)
    reader.onload = () => resolve(reader.result)
    reader.onerror = error => reject(error)
  })
}
const formItemLayout = {
  labelCol: { span: 24 },
  wrapperCol: { span: 24 }
}
export default {
  name: 'User',
  computed: {
    ...mapState({
      currentUser: state => state.account.user
    })
  },
  data () {
    return {
      form: this.$form.createForm(this),
      formItemLayout,
      loading: false,
      fileList: [],
      previewVisible: false,
      previewImage: '',
      enterpriseInfo: null
    }
  },
  mounted () {
    this.getEnterpriseInfo(this.currentUser.userId)
  },
  methods: {
    getEnterpriseInfo (expertId) {
      this.$get(`/cos/enterprise-info/detail/id/${expertId}`).then((r) => {
        this.enterpriseInfo = r.data.data
        console.log(this.enterpriseInfo)
        this.setFormValues(this.enterpriseInfo)
      })
    },
    handleCancel () {
      this.previewVisible = false
    },
    async handlePreview (file) {
      if (!file.url && !file.preview) {
        file.preview = await getBase64(file.originFileObj)
      }
      this.previewImage = file.url || file.preview
      this.previewVisible = true
    },
    picHandleChange ({ fileList }) {
      this.fileList = fileList
    },
    imagesInit (images) {
      if (images !== null && images !== '') {
        let imageList = []
        images.split(',').forEach((image, index) => {
          imageList.push({uid: index, name: image, status: 'done', url: 'http://127.0.0.1:9527/imagesWeb/' + image})
        })
        this.fileList = imageList
      }
    },
    setFormValues ({...enterprise}) {
      this.rowId = enterprise.id
      let fields = ['name', 'abbreviation', 'creditCode', 'code', 'nature', 'natureTwo', 'status', 'corporateRepresentative', 'corporateRepresentativeId', 'corporateRepresentativePhone', 'registeredCapital', 'registeredCapitalCurrency', 'establishmentDate', 'businessBeginDate', 'businessEndDate', 'registeredAddress', 'businessScope', 'source', 'province', 'city', 'district', 'enName', 'industry', 'unitDescription', 'images']
      let obj = {}
      Object.keys(enterprise).forEach((key) => {
        if (key === 'images') {
          this.fileList = []
          this.imagesInit(enterprise['images'])
        }
        if (fields.indexOf(key) !== -1) {
          this.form.getFieldDecorator(key)
          obj[key] = enterprise[key]
        }
      })
      this.form.setFieldsValue(obj)
    },
    handleSubmit () {
      // 获取图片List
      let images = []
      this.fileList.forEach(image => {
        if (image.response !== undefined) {
          images.push(image.response)
        } else {
          images.push(image.name)
        }
      })
      this.form.validateFields((err, values) => {
        values.id = this.rowId
        values.images = images.length > 0 ? images.join(',') : null
        if (!err) {
          this.loading = true
          this.$put('/cos/enterprise-info', {
            ...values
          }).then((r) => {
            this.$message.success('更新成功')
            this.loading = false
            this.getEnterpriseInfo(this.currentUser.userId)
          }).catch(() => {
            this.loading = false
          })
        }
      })
    }
  }
}
</script>

<style scoped>

</style>
