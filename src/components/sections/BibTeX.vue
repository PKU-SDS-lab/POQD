<script>
export default {
  data() {
    return {
      bibtex: [
        "@misc{liu2025poqdperformanceorientedquerydecomposer,",
        "  title={POQD: Performance-Oriented Query Decomposer for Multi-vector retrieval},",
        "  author={Yaoyang Liu and Junlin Li and Yinjun Wu and Zhen Chen},",
        "  year={2025},",
        "  eprint={2505.19189},",
        "  archivePrefix={arXiv},",
        "  primaryClass={cs.IR},",
        "  url={https://arxiv.org/abs/2505.19189},",
        "}",
        // "@inproceedings{chen2025core,",
        // "  title={Core Context Aware Transformers for Long Context Language Modeling}, ",
        // "  author={Yaofo Chen and Zeng You and Shuhai Zhang and Haokun Li and Yirui Li and Yaowei Wang and Mingkui Tan},",
        // "  booktitle={International Conference on Machine Learning},",
        // "  year={2025}",
        // "}",
      ],
    }
  },
  methods: {
    copyVal() {
      let oInput = document.createElement('textarea');
      let text = document.getElementById('bibtex').innerText;
      oInput.value = text;
      document.body.appendChild(oInput);
      oInput.select();
      document.execCommand('Copy');
      this.$message.success('Copy Successfully');
      oInput.remove();
    }
  }
}

</script>

<template>
  <div>
    <el-divider />
      
      <el-row justify="center">
        <h1 class="section-title">BibTeX</h1>
      </el-row>
      
      <el-row justify="center">
        <el-col class='bibtex' :xs="24" :sm="20" :md="14" :lg="12" :xl="12" @click="copyVal()" >
          <div style="text-align: center; color: var(--el-text-color-secondary); margin-top: 20px;">🖱️ Click here to copy BibTex.</div> 
          <el-row>
              <el-scrollbar style="margin: 0px 20px 5px 20px;">
                <pre id="bibtex"><code v-for="b in bibtex">{{ b }}<br/></code></pre>
              </el-scrollbar>
          </el-row>
        </el-col>
      </el-row>

  </div>
</template>

<style scoped>

.scrollbar-flex-content {
  display: flex;
}

/* 卡片属性 */
.bibtex {
  margin: 20px 0px;
  padding-top: 5px;
  box-shadow: var(--el-box-shadow-light); 
  border-radius: 10px;
}

/* 卡片悬浮 */
.bibtex:hover {
  box-shadow: var(--el-box-shadow); 
}

/* 卡片点击 */
.bibtex:active{
  box-shadow: var(--el-box-shadow-lighter); 
}

pre {
  border: none;
  border-radius: 0px;
  padding: 10px;
  background: none;
}

pre code {
  font-size: 18px;
  background: #ffffff;
}



</style>