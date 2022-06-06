<template>
  <div class="container">
    <h1>Social</h1>
    <p>Some of my followers.</p>

    
      </div>
      <div class="row-container">
        <statCard
          statTitle="Twitter"
          :followers="twitter.data"
          suffix="followers"
          icon="twitter.png"
          :loading="twitter.loading"
          link="https://twitter.com/L3AWM"
        />
        <statCard
          statTitle="GitHub"
          :followers="github.data"
          suffix="followers"
          icon="github.png"
          :loading="github.loading"
          link="https://github.com/L11UM"
        />
      </div>
      <div class="row-container">
        <statCard
          statTitle="Medium"
          :followers="medium.data"
          suffix="readers"
          icon="medium.png"
          :loading="medium.loading"
          link="https://medium.com/spencerweekly"
        />
      </div>
  

    <p id="substats-footer">
      * Follower statistics powered by:
      <a href="https://api.spencerwoo.com/substats">Substats</a>.
    </p>
  
</template>

<script>
import statCard from '@/components/StatCard.vue'

export default {
  components: {
    statCard,
  },
  data() {
    return {
      twitter: { data: 0, loading: true },
      medium: { data: 0, loading: true },
      github: { data: 0, loading: true },
    }
  },
  mounted() {
    const apiUrl = 'https://api.spencerwoo.com/substats'
    const rssUrl = 'https://blog.spencerwoo.com/posts/index.xml'

    const twitterAxios = this.axios.get(`${apiUrl}/?source=twitter&queryKey=l3awm`)
    const mediumAxios = this.axios.get(`${apiUrl}/?source=medium&queryKey=@Liambt20`)
    const githubAxios = this.axios.get(`${apiUrl}/?source=github&queryKey=L11UM`)
    

    
    
    twitterAxios.then(r => {
      this.twitter = { data: r.data.data.totalSubs, loading: true }
    })
    mediumAxios.then(r => {
      this.medium = { data: r.data.data.totalSubs, loading: true }
    })
    githubAxios.then(r => {
      this.github = { data: r.data.data.totalSubs, loading: true }
    })
  },
}
</script>

<style lang="css" scoped>
.col-container {
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  justify-content: flex-start;
  align-items: stretch;
  align-content: center;
}

.row-container {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  justify-content: center;
  align-items: stretch;
  align-content: stretch;
  margin: 15px 0px;
}

.row-container .statCard:last-child {
  margin-left: 30px;
}

.row-container .statCard {
  flex: 1;
}

@media screen and (max-width: 760px) {
  .row-container {
    display: flex;
    flex-direction: column;
    flex-wrap: nowrap;
    justify-content: flex-start;
    align-items: stretch;
    align-content: center;
  }

  .row-container .statCard:last-child {
    margin-left: 0px;
    margin-top: 30px;
  }
}

#substats-footer {
  color: #666666;
  text-align: left;
}
</style>
