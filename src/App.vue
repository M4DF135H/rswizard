<template>
  <rs-wizard :steps="getSteps()" />
</template>

<script>
import rsWizard from './components/rs-wizard.vue';
import rsWizardInstruction from './components/rs-wizard-instruction.vue';

export default {
  components: { rsWizard, rsWizardInstruction },
  data() {
    return {};
  },
  methods: {
    getSteps() {
      return [
        {
          id: 1,
          title: 'Инструкция',
          header: 'Инструкция по установке интеграции smsru',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nisl lorem, aliquam vitae lobortis quis, posuere nec odio. Vivamus congue augue felis, faucibus malesuada odio dapibus non. Aenean laoreet arcu vel ligula pharetra, nec tincidunt quam malesuada. Nullam euismod vulputate diam et pharetra. Vestibulum commodo lorem eu est mattis malesuada. Praesent rutrum id velit vitae malesuada. Vestibulum vel dolor nisl. Etiam vestibulum sapien eget sodales aliquam. Aenean in elementum dolor. Ut ante nisl, imperdiet nec tincidunt nec, aliquet vitae justo. Sed maximus convallis congue.\n' +
          '\n' +
          'Pellentesque sed justo auctor, euismod orci in, scelerisque sem. Mauris eu convallis nisi, condimentum gravida nisl. Curabitur malesuada quam sed justo porta tempus. Fusce bibendum augue ac ultricies faucibus. Praesent nec rutrum odio. Sed fringilla elementum mauris ultrices accumsan. In ut pretium lectus. Mauris aliquet sollicitudin lorem, at consequat erat convallis non. Praesent in nibh sapien. Praesent tempor lacus ipsum. Curabitur vitae volutpat orci. In accumsan nisl eget erat efficitur, a tincidunt lacus ullamcorper. Sed scelerisque, velit sit amet suscipit vehicula, est arcu pulvinar orci, vel hendrerit dolor metus venenatis libero.\n' +
          '\n',
          complited: false,
          active: true,
          component: rsWizardInstruction,
        },
        {
          id: 2,
          title: 'Подключение скрипта',
          header: 'Подключение скрипта смс сендера',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nisl lorem, aliquam vitae lobortis quis, posuere nec odio. Vivamus congue augue felis, faucibus malesuada odio dapibus non. Aenean laoreet arcu vel ligula pharetra, nec tincidunt quam malesuada. Nullam euismod vulputate diam et pharetra. Vestibulum commodo lorem eu est mattis malesuada. Praesent rutrum id velit vitae malesuada. Vestibulum vel dolor nisl. Etiam vestibulum sapien eget sodales aliquam. Aenean in elementum dolor. Ut ante nisl, imperdiet nec tincidunt nec, aliquet vitae justo. Sed maximus convallis congue.\n' +
          '\n' +
          'Pellentesque sed justo auctor, euismod orci in, scelerisque sem. Mauris eu convallis nisi, condimentum gravida nisl. Curabitur malesuada quam sed justo porta tempus. Fusce bibendum augue ac ultricies faucibus. Praesent nec rutrum odio. Sed fringilla elementum mauris ultrices accumsan. In ut pretium lectus. Mauris aliquet sollicitudin lorem, at consequat erat convallis non. Praesent in nibh sapien. Praesent tempor lacus ipsum. Curabitur vitae volutpat orci. In accumsan nisl eget erat efficitur, a tincidunt lacus ullamcorper. Sed scelerisque, velit sit amet suscipit vehicula, est arcu pulvinar orci, vel hendrerit dolor metus venenatis libero.\n' +
          '\n',
          complited: false,
          active: false,
          component: rsWizardInstruction,
        },
        {
          id: 3,
          title: 'Настройка доп.полей',
          header: 'Настройка доп.полей для отправки смс',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nisl lorem, aliquam vitae lobortis quis, posuere nec odio. Vivamus congue augue felis, faucibus malesuada odio dapibus non. Aenean laoreet arcu vel ligula pharetra, nec tincidunt quam malesuada. Nullam euismod vulputate diam et pharetra. Vestibulum commodo lorem eu est mattis malesuada. Praesent rutrum id velit vitae malesuada. Vestibulum vel dolor nisl. Etiam vestibulum sapien eget sodales aliquam. Aenean in elementum dolor. Ut ante nisl, imperdiet nec tincidunt nec, aliquet vitae justo. Sed maximus convallis congue.\n' +
          '\n' +
          'Pellentesque sed justo auctor, euismod orci in, scelerisque sem. Mauris eu convallis nisi, condimentum gravida nisl. Curabitur malesuada quam sed justo porta tempus. Fusce bibendum augue ac ultricies faucibus. Praesent nec rutrum odio. Sed fringilla elementum mauris ultrices accumsan. In ut pretium lectus. Mauris aliquet sollicitudin lorem, at consequat erat convallis non. Praesent in nibh sapien. Praesent tempor lacus ipsum. Curabitur vitae volutpat orci. In accumsan nisl eget erat efficitur, a tincidunt lacus ullamcorper. Sed scelerisque, velit sit amet suscipit vehicula, est arcu pulvinar orci, vel hendrerit dolor metus venenatis libero.\n' +
          '\n' + 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nisl lorem, aliquam vitae lobortis quis, posuere nec odio. Vivamus congue augue felis, faucibus malesuada odio dapibus non. Aenean laoreet arcu vel ligula pharetra, nec tincidunt quam malesuada. Nullam euismod vulputate diam et pharetra. Vestibulum commodo lorem eu est mattis malesuada. Praesent rutrum id velit vitae malesuada. Vestibulum vel dolor nisl. Etiam vestibulum sapien eget sodales aliquam. Aenean in elementum dolor. Ut ante nisl, imperdiet nec tincidunt nec, aliquet vitae justo. Sed maximus convallis congue.\n' +
          '\n' +
          'Pellentesque sed justo auctor, euismod orci in, scelerisque sem. Mauris eu convallis nisi, condimentum gravida nisl. Curabitur malesuada quam sed justo porta tempus. Fusce bibendum augue ac ultricies faucibus. Praesent nec rutrum odio. Sed fringilla elementum mauris ultrices accumsan. In ut pretium lectus. Mauris aliquet sollicitudin lorem, at consequat erat convallis non. Praesent in nibh sapien. Praesent tempor lacus ipsum. Curabitur vitae volutpat orci. In accumsan nisl eget erat efficitur, a tincidunt lacus ullamcorper. Sed scelerisque, velit sit amet suscipit vehicula, est arcu pulvinar orci, vel hendrerit dolor metus venenatis libero.\n' +
          '\n' + 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nisl lorem, aliquam vitae lobortis quis, posuere nec odio. Vivamus congue augue felis, faucibus malesuada odio dapibus non. Aenean laoreet arcu vel ligula pharetra, nec tincidunt quam malesuada. Nullam euismod vulputate diam et pharetra. Vestibulum commodo lorem eu est mattis malesuada. Praesent rutrum id velit vitae malesuada. Vestibulum vel dolor nisl. Etiam vestibulum sapien eget sodales aliquam. Aenean in elementum dolor. Ut ante nisl, imperdiet nec tincidunt nec, aliquet vitae justo. Sed maximus convallis congue.\n' +
          '\n' +
          'Pellentesque sed justo auctor, euismod orci in, scelerisque sem. Mauris eu convallis nisi, condimentum gravida nisl. Curabitur malesuada quam sed justo porta tempus. Fusce bibendum augue ac ultricies faucibus. Praesent nec rutrum odio. Sed fringilla elementum mauris ultrices accumsan. In ut pretium lectus. Mauris aliquet sollicitudin lorem, at consequat erat convallis non. Praesent in nibh sapien. Praesent tempor lacus ipsum. Curabitur vitae volutpat orci. In accumsan nisl eget erat efficitur, a tincidunt lacus ullamcorper. Sed scelerisque, velit sit amet suscipit vehicula, est arcu pulvinar orci, vel hendrerit dolor metus venenatis libero.\n' +
          '\n' + 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nisl lorem, aliquam vitae lobortis quis, posuere nec odio. Vivamus congue augue felis, faucibus malesuada odio dapibus non. Aenean laoreet arcu vel ligula pharetra, nec tincidunt quam malesuada. Nullam euismod vulputate diam et pharetra. Vestibulum commodo lorem eu est mattis malesuada. Praesent rutrum id velit vitae malesuada. Vestibulum vel dolor nisl. Etiam vestibulum sapien eget sodales aliquam. Aenean in elementum dolor. Ut ante nisl, imperdiet nec tincidunt nec, aliquet vitae justo. Sed maximus convallis congue.\n' +
          '\n' +
          'Pellentesque sed justo auctor, euismod orci in, scelerisque sem. Mauris eu convallis nisi, condimentum gravida nisl. Curabitur malesuada quam sed justo porta tempus. Fusce bibendum augue ac ultricies faucibus. Praesent nec rutrum odio. Sed fringilla elementum mauris ultrices accumsan. In ut pretium lectus. Mauris aliquet sollicitudin lorem, at consequat erat convallis non. Praesent in nibh sapien. Praesent tempor lacus ipsum. Curabitur vitae volutpat orci. In accumsan nisl eget erat efficitur, a tincidunt lacus ullamcorper. Sed scelerisque, velit sit amet suscipit vehicula, est arcu pulvinar orci, vel hendrerit dolor metus venenatis libero.\n' +
          '\n' + 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nisl lorem, aliquam vitae lobortis quis, posuere nec odio. Vivamus congue augue felis, faucibus malesuada odio dapibus non. Aenean laoreet arcu vel ligula pharetra, nec tincidunt quam malesuada. Nullam euismod vulputate diam et pharetra. Vestibulum commodo lorem eu est mattis malesuada. Praesent rutrum id velit vitae malesuada. Vestibulum vel dolor nisl. Etiam vestibulum sapien eget sodales aliquam. Aenean in elementum dolor. Ut ante nisl, imperdiet nec tincidunt nec, aliquet vitae justo. Sed maximus convallis congue.\n' +
          '\n' +
          'Pellentesque sed justo auctor, euismod orci in, scelerisque sem. Mauris eu convallis nisi, condimentum gravida nisl. Curabitur malesuada quam sed justo porta tempus. Fusce bibendum augue ac ultricies faucibus. Praesent nec rutrum odio. Sed fringilla elementum mauris ultrices accumsan. In ut pretium lectus. Mauris aliquet sollicitudin lorem, at consequat erat convallis non. Praesent in nibh sapien. Praesent tempor lacus ipsum. Curabitur vitae volutpat orci. In accumsan nisl eget erat efficitur, a tincidunt lacus ullamcorper. Sed scelerisque, velit sit amet suscipit vehicula, est arcu pulvinar orci, vel hendrerit dolor metus venenatis libero.\n' +
          '\n' + 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nisl lorem, aliquam vitae lobortis quis, posuere nec odio. Vivamus congue augue felis, faucibus malesuada odio dapibus non. Aenean laoreet arcu vel ligula pharetra, nec tincidunt quam malesuada. Nullam euismod vulputate diam et pharetra. Vestibulum commodo lorem eu est mattis malesuada. Praesent rutrum id velit vitae malesuada. Vestibulum vel dolor nisl. Etiam vestibulum sapien eget sodales aliquam. Aenean in elementum dolor. Ut ante nisl, imperdiet nec tincidunt nec, aliquet vitae justo. Sed maximus convallis congue.\n' +
          '\n' +
          'Pellentesque sed justo auctor, euismod orci in, scelerisque sem. Mauris eu convallis nisi, condimentum gravida nisl. Curabitur malesuada quam sed justo porta tempus. Fusce bibendum augue ac ultricies faucibus. Praesent nec rutrum odio. Sed fringilla elementum mauris ultrices accumsan. In ut pretium lectus. Mauris aliquet sollicitudin lorem, at consequat erat convallis non. Praesent in nibh sapien. Praesent tempor lacus ipsum. Curabitur vitae volutpat orci. In accumsan nisl eget erat efficitur, a tincidunt lacus ullamcorper. Sed scelerisque, velit sit amet suscipit vehicula, est arcu pulvinar orci, vel hendrerit dolor metus venenatis libero.\n' +
          '\n',
          complited: false,
          active: false,
          component: rsWizardInstruction,
        },
      ];
    },
  },
};
</script>
