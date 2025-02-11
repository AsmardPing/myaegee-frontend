<template>
  <div class='tile is-ancestor resources'>
    <div class='tile is-parent is-vertical'>

      <section v-for="(block, name) in resources" v-bind:key="name">
        <div class="title">{{ name }}</div>

        <section class="resources-block">
          <div class="resources-item" v-for="resource in block" v-bind:key="resource.url">
            <a :href="resource.url" target="_blank">
              <div class="card">
                <header role="tab" class="card-header">
                  <div class="card-header-title" :style="{ 'background-color': resource.color }">
                    <span>{{ resource.title }}</span>
                  </div>
                </header>
                <div class="card-content">
                  <div class="card-content-box" v-html="resource.description"></div>
                </div>
              </div>
            </a>
          </div>
        </section>
      </section>

    </div>
  </div>
</template>

<style>
.resources .resources-item {
  margin-right: 30px;
  margin-bottom: 30px;
  width: 300px;
  height: 150px;
}
.resources .resources-item .card:hover .card-content {
  background-color: #fafafa;
}
.resources .resources-item .card {
  height: 100%;
}
.resources .resources-item .card-header {
  height: 50px;
}
.resources .resources-item .card-content {
  height: 100px;
}
.resources .resources-block {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: 20px;
  margin-top: 50px;
}
.resources .not-bold {
  font-weight: normal;
}
</style>

<script>
export default {
  data () {
    return {
      resources: {
        'External': [
          {
            url: 'https://aegee.org',
            title: 'AEGEE Website',
            description: 'Official website',
            color: '#4CA0FF'
          },
          {
            url: 'https://aegee.us7.list-manage.com/subscribe?u=7a170c64e0d3990f3f6629d21&id=fc8908d780',
            title: 'External Newsletter',
            description: 'Bi-monthly newsletter for Partners & Supporters',
            color: '#4CA0FF'
          },
          {
            url: 'https://www.aegee.org/external/key-to-europe/',
            title: 'Key to Europe',
            description: 'Yearbook - the annual report publication',
            color: '#4CA0FF'
          }
        ],
        'Members': [
          {
            url: '/pages/mailing-lists',
            title: 'Mailing Lists',
            description: 'AEGEE mailing lists',
            color: '#FFDB4C'
          },
          {
            url: 'https://aegee.org/wiki',
            title: 'AEGEE Wiki',
            description: 'A collaborative knowledge backbone of AEGEE',
            color: '#FFDB4C'
          },
          {
            url: 'https://drive.google.com/drive/folders/1IOg5hnbGmhgZ8pajYQgbY3CBTsETijS_',
            title: 'AEGEE Materials Database',
            description: 'Knowledge library of AEGEE materials',
            color: '#FFDB4C'
          },
          {
            url: 'https://www.facebook.com/groups/aegeeans/',
            title: 'Facebook Group',
            description: 'AEGEE\'s official group on Facebook',
            color: '#FFDB4C'
          },
          {
            url: 'https://www.zeus.aegee.org/magazine/',
            title: 'The AEGEEan Magazine',
            description: 'AEGEE\'s online Magazine',
            color: '#FFDB4C'
          },
          {
            url: 'https://drive.google.com/file/d/10iLCFY40_kGATtZLwkwIs0PJwt5VNXX5/view',
            title: 'Strategic Plan',
            description: 'Strategic Plan of AEGEE-Europe 2020-2023',
            color: '#FFDB4C'
          },
          {
            url: 'https://drive.google.com/file/d/1XU-1S_QkPRybkVfgYuFnZvCWfXFcjmjt/view',
            title: 'Action Agenda',
            description: 'Action Agenda 2021-2022',
            color: '#FFDB4C'
          },
          {
            url: 'https://aegee-academy.eu/request-a-training/',
            title: 'AEGEE-Academy',
            description: 'Request a trainer for your training events',
            color: '#FFDB4C'
          },
          {
            url: 'https://calendar.google.com/calendar/embed?src=powerhost.gr_uo2hj0qhr1493oqhpjel5v4lo8%40group.calendar.google.com&ctz=Europe%2FBrussels',
            title: 'Calendar of CD',
            description: 'Find out more about how the schedule of CD looks like',
            color: '#FFDB4C'
          },
          {
            url: 'https://podio.com/webforms/2318137/167577',
            title: 'AEGEE Newsletter',
            description: 'Submitting content for the AEGEE newsletter',
            color: '#FFDB4C'
          },
          {
            url: 'https://podio.com/webforms/13269615/901752',
            title: 'CD House Guest Request',
            description: 'Visiting the CD house',
            color: '#FFDB4C'
          },
          {
            url: 'https://forms.gle/ZMfSByo5QEUAwoY4A',
            title: 'ASRF Application Form',
            description: 'Apply for the AEGEE Social Responsibility Fund',
            color: '#FFDB4C'
          }
        ],
        'Network': [
          {
            url: 'https://docs.google.com/forms/d/e/1FAIpQLSfheOjWEQjqua1UqaqYofuqlrBV2bQK_m8OOypeqq6fnfgQLQ/viewform',
            title: 'Board Submission Form',
            description: 'Submitting new board to NetCom',
            color: '#C2DE5D'
          },
          {
            url: 'https://docs.google.com/forms/d/e/1FAIpQLSd2u-r1jFGyNwYCwsSnMf9-dApH7ZGeGltZusxqWqkB_VQ0zg/viewform',
            title: 'AEGEE Contact in your City',
            description: 'Leave your contact details behind to start the process of founding an AEGEE Contact in your city',
            color: '#C2DE5D'
          },
          {
            url: 'https://docs.google.com/forms/d/e/1FAIpQLSfmbGAjG_us00KMuV-pMeasja_gfjLXVwhaqRK9y5rbTSb0xw/viewform',
            title: 'Suggest a City for a Potential Contact',
            description: 'Provide a suggestion for where AEGEE should have a Contact',
            color: '#C2DE5D'
          },
          {
            url: 'https://docs.google.com/document/d/1rQRddt8H3J1RUYMpdxRxuhNqyV3BcP8mV8ykNLNup3o/edit',
            title: 'Set up your own Contact',
            description: 'Find out how to set up a Contact in this step by step guide',
            color: '#C2DE5D'
          },
          {
            url: 'https://docs.google.com/document/d/1e0jdTLvn7-JdwOlxMXcf55I5mcNwEmI_loN0djj0U2c/edit',
            title: 'Develop your Contact',
            description: 'Find out how to develop your Contact with tips and tricks in this toolkit',
            color: '#C2DE5D'
          }
        ],
        'Statutory': [
          {
            url: 'https://www.zeus.aegee.org/statutoryvote/jc/',
            title: 'Online Voting',
            description: 'Online Voting for Agorae/General Assembly',
            color: '#C44BC2'
          },
          {
            url: 'https://drive.google.com/drive/folders/1GKd6jWeolMDRw7EXZO-ROXupBQUzAgk2',
            title: 'CIA',
            description: 'Statutes, regulation, working formats and motions',
            color: '#C44BC2'
          }
        ],
        'Useful guides': [
          {
            url: 'https://drive.google.com/drive/folders/1FosqlM9zjSnpvAxZkOg0yoCW7swHdwM1',
            title: 'Visual Identity',
            description: 'Manual, logos, PR materials and more',
            color: '#FF5543'
          },
          {
            url: 'https://drive.google.com/drive/folders/1J9qCQP4Kbuol3Nutid3h04b-E-BM3QN5',
            title: 'Internal Education',
            description: 'LTC packages',
            color: '#FF5543'
          }
        ]
      }
    }
  }
}
</script>
