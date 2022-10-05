<template>
  <div class="container">
    <h1>Projects</h1>
    <p>Things I've built</p>

    <GitHubCard
      title="Professional Website made for Insurance Company"
      link="https://github.com/L11um/energyinsure"
      :info="dowwwInfo"
      :loading="loading"
    >
      <p>
        Check it out here:
        <a href="https://l11um.github.io/energyinsure/">Energy Insure</a>.
      </p>
    </GitHubCard>

    <GitHubCard
      title="📈 Substats"
      link=""
      :info="substatsInfo"
      :loading="loading"
    >
      <p>
        Serverless function to count how many people are subscribed to you in your favorite services. Supporting Feedly,
       GitHub, Twitter, and much more.
      </p>
    </GitHubCard>

    <GitHubCard title="📖 BIThesis" link="" :info="bithesisInfo" :loading="loading">
      <p>
    
      </p>
    </GitHubCard>

    <GitHubCard
      title="💡 FATES"
      link=""
      :info="fatesInfo"
      :loading="loading"
    >
      <p>
        <b>The Fully Anonymous Teaching Evaluation System:</b> a project that won National 2nd Prize on the
      </p>
    </GitHubCard>

    <GitHubCard
      title="💻 My dotfiles"
      link=""
      :info="dotfilesInfo"
      :loading="loading"
    >
      <p>Project1</p>
    </GitHubCard>
  </div>
</template>

<script>
import GitHubCard from '@/components/GitHubCard.vue'

export default {
  components: {
    GitHubCard,
  },
  data() {
    return {
      loading: true,
      dowwwInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      substatsInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      bithesisInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      fatesInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      dotfilesInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
    }
  },
  mounted() {
    const githubApiUrl = 'https://api.github.com/repos'

    const dowwwAxios = this.axios.get(`${githubApiUrl}/spencerwooo/dowww`)
    const substatsAxios = this.axios.get(`${githubApiUrl}/spencerwooo/Substats`)
    const bithesisAxios = this.axios.get(`${githubApiUrl}/BITNP/BIThesis`)
    const fatesAxios = this.axios.get(`${githubApiUrl}/SecureCats/Evaluation_BackEnd`)
    const dotfilesAxios = this.axios.get(`${githubApiUrl}/spencerwooo/dotfiles`)

    this.axios
      .all([dowwwAxios, substatsAxios, bithesisAxios, fatesAxios, dotfilesAxios])
      .then(
        this.axios.spread((...resp) => {
          this.loading = false
          this.dowwwInfo = resp[0].data
          this.substatsInfo = resp[1].data
          this.bithesisInfo = resp[2].data
          this.fatesInfo = resp[3].data
          this.dotfilesInfo = resp[4].data
        }),
      )
      .catch(err => {
        this.loading = false
        // eslint-disable-next-line no-console
        console.error(err)
      })
  },
}
</script>

<style scoped>
.container .github-project-card:not(:last-child) {
  margin-bottom: 40px;
}
</style>
