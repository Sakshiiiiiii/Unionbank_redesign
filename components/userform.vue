<template>

<v-container>
 <h4 class="hey"> Please Fill Your Details </h4> 
<v-row>
 
 
<col sm="10" md="10" cols="10">

  <form>
    
    <v-text-field
      v-model="name"
      :error-messages="nameErrors"
      :counter="10"
      color="#r02589D"
      label="Name"
      required
      @input="$v.name.$touch()"
      @blur="$v.name.$touch()"
    ></v-text-field>

    <v-text-field
      v-model="Surname"
      :error-messages="nameErrors"
      :counter="10"
      label="Surname"
      required
      @input="$v.name.$touch()"
      @blur="$v.name.$touch()"
    ></v-text-field>

    <v-text-field
      v-model="Surname"
      :error-messages="nameErrors"
      :counter="10"
      label="Mobile No."
      required
      @input="$v.name.$touch()"
      @blur="$v.name.$touch()"
    ></v-text-field>

    <v-text-field
      v-model="Surname"
      :error-messages="nameErrors"
      :counter="10"
      label="Phone No."
      required
      @input="$v.name.$touch()"
      @blur="$v.name.$touch()"
    ></v-text-field>
    
    <v-text-field
      v-model="email"
      :error-messages="emailErrors"
      label="E-mail"
      required
      @input="$v.email.$touch()"
      @blur="$v.email.$touch()"
    ></v-text-field>
    <v-select
      v-model="select"
      :items="items"
      :error-messages="selectErrors"
      label="Location"
      required
      @change="$v.select.$touch()"
      @blur="$v.select.$touch()"
    ></v-select>
    
     <v-row>
     <v-col cols="3">

    <v-img
      class="mx-auto"
      height="30px"
      width="160px"
      src="Captcha.jpg"
      
    >
     
    </v-img>

  </v-col>
  </v-row>
    <v-text-field
      v-model="Surname"
      :error-messages="nameErrors"
      :counter="10"
      label="Captcha"
      required
      @input="$v.name.$touch()"
      @blur="$v.name.$touch()"
    ></v-text-field>
    <v-checkbox
      v-model="isFormValid"
      :error-messages="checkboxErrors"
      label="I / We authorize Union Bank of India and its representatives to call me or SMS me with reference to my loan enquiry / application. "
      required
      @change="$v.checkbox.$touch()"
      @blur="$v.checkbox.$touch()"
    ></v-checkbox>

  <v-row justify="center">
    <v-dialog v-model="dialog" persistent max-width="290">
      <template v-slot:activator="{ on, attrs }">
        <v-btn
        :disabled="!isFormValid"
    
          color="primary"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Apply Loan
        </v-btn>
      </template>
      <v-card>
        <v-card-title class="headline">Task Successful!</v-card-title>
        <v-card-text>Your loan application is successfully done.<br> Thank you for banking with us.</v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          
          <v-btn color="green darken-1" text @click="dialog = false">Ok</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row> 
 
    
  </form>
  </v-row>
  </v-container>
</template>

<script>
  import { validationMixin } from 'vuelidate'
  import { required, maxLength, email } from 'vuelidate/lib/validators'

  export default {
    mixins: [validationMixin],

    validations: {
      name: { required, maxLength: maxLength(10) },
      email: { required, email },
      select: { required },
      checkbox: {
        checked (val) {
          return val
        },
      },
    },

    data: () => ({
      name: '',
      email: '',
      select: null,
      items: [
        'AGARTALA',
'AGRA',
'AHMEDABAD',
'AIZWAL',
'AJMER',
'ALLAHABAD',
'ALLEPPEY',
'ALIBAUG',
'ALMORA',
'ALSISAR',
'ALWAR',
'AMBALA',
'AMLA',
'AMRITSAR',
'ANAND',
'ANKLESHWAR',
'ASHTAMUDI',
'AULI',
'AURANGABAD',

'BADDI',
'BADRINATH',
'BALASINOR',
'BALRAMPUR',
'BAMBORA',
'BANDHAVGARH',
'BANDIPUR',
'BANGALORE',
'BARBIL',
'BAREILLY',
'BEHROR',
'BELGAUM',
'BERHAMPUR',
'BETALGHAT',
'BHARATPUR',
'BHANDARDARA',
'BHARUCH',
'BHAVANGADH',
'BHAVNAGAR',
'BHILAI',
'BHIMTAL',
'BHOPAL',
'BHUBANESHWAR',
'BHUJ',
'BIKANER',
'BINSAR',
'BODHGAYA',
'BUNDI',

'CALICUT',
'CANANNORE',
'CHAIL',
'CHAMBA',
'CHANDIGARH',
'CHENNAI',
'CHIKMAGALUR',
'CHIPLUN',
'CHITRAKOOT',
'CHITTORGARH',
'COIMBATORE',
'COONOOR',
'COORG',
'CORBETT NATIONAL PARK',
'CUTTACK',

'DABHOSA',
'DALHOUSIE',
'DAMAN',
'DANDELI',
'DAPOLI',
'DARJEELING',
'DAUSA',
'DEHRADUN',
'DHARAMSHALA',
'DIBRUGARH',
'DIGHA',
'DIU',
'DIVE AGAR',
'DOOARS',
'DURGAPUR',
'DURSHET',
'DWARKA',

'FARIDABAD',
'FIROZABAD',

'GANGOTRI',
'GANGTOK',
'GANAPATIPULE',
'GANDHIDHAM',
'GANDHINAGAR',
'GARHMUKTESHWAR',
'GARHWAL',
'GAYA',
'GHAZIABAD',
'GOA',
'GOKHARNA',
'GONDAL',
'GORAKHPUR',
'GREATER NOIDA',
'GULMARG',
'GURGAON',
'GURUVAYOOR',
'GUWAHATI',
'GWALIOR',



'HALEBID',
'HAMPI',
'HANSI',
'HARIDWAR',
'HASSAN',
'HOSPET',
'HOSUR',
'HUBLI',
'HYDERABAD',

'IDUKKI',
'IGATPURI',
'IMPHAL',
'INDORE',

'JABALPUR',
'JAIPUR',
'JAISALMER',
'JALANDHAR',
'JALGAON',
'JAMBUGODHA',
'JAMMU',
'JAMNAGAR',
'JAMSHEDPUR',
'JAWHAR',
'JHANSI',
'JODHPUR',
'JOJAWAR',
'JORHAT',
'JUNAGADH',

'KABINI',
'KALIMPONG',
'KANATAL',
'KANCHIPURAM',
'KANHA',
'KANPUR',
'KANYAKUMARI',
'KARGIL',
'KARJAT',
'KARNAL',
'KARUR',
'KARWAR',
'KASARGOD',
'KASAULI',
'KASHIPUR',
'KASHID',
'KATRA',
'KAUSANI',
'KAZA',
'KAZIRANGA',
'KEDARNATH',
'KHAJJIAR',
'KHAJURAHO',
'KHANDALA',
'KHIMSAR',
'KOCHIN',
'KODAIKANAL',
'KOLHAPUR',
'KOLKATA',
'KOLLAM',
'KOTA',
'KOTAGIRI',
'KOTTAYAM',
'KOVALAM',
'KUFRI',
'KUMBALGARH',
'KULLU',
'KUMARAKOM',
'KUMBAKONAM',
'KUMILY',
'KURSEONG',
'KUSHINAGAR',
'L',
'LACHUNG',
'LEH',
'LAKSHADWEEP',
'LONAVALA',
'LOTHAL',
'LUCKNOW',
'LUDHIANA',
'LUMBINI',


'MADURAI',
'MAHABALESHWAR',
'MAHABALIPURAM',
'MALAPPURAM',
'MALPE',
'MALSHEJ GHAT',
'MALVAN',
'MANALI',
'MANDAVI',
'MANDAWA',
'MANESAR',
'MARARRI',
'MANDORMONI',
'MANGALORE',
'MANMAD',
'MARCHULA',
'MATHERAN',
'MATHURA',
'MCLEODGANJ',
'MOHALI',
'MOUNT ABU',
'MORADABAD',
'MORBI',
'MUKTESHWAR',
'MUMBAI',
'MUNDRA',
'MUNNAR',
'MURUD JANJIRA',
'MUSSOORIE',
'MYSORE',

'NADUKANI',
'NAGAPATTINAM',
'NAGARHOLE',
'NAGAUR FORT',
'NAGOTHANE',
'NAGPUR',
'NAHAN',
'NAINITAL',
'NALDHERA',
'NANDED',
'NAPNE',
'NASIK',
'NAVI MUMBAI',
'NERAL',
'NEW DELHI',
'NILGIRI',
'NOIDA',

'OOTY',
'ORCHHA',
'OSIAN',

'PACHMARHI',
'PALAMPUR',
'PALANPUR',
'PALI',
'PAHALGAM',
'PALITANA',
'PALLAKAD',
'PANCHGANI',
'PANCHKULA',
'PANNA',
'PANHALA',
'PANVEL',
'PANTNAGAR',
'PARWANOO',
'PATIALA',
'PATHANKOT',
'PATNA',
'PATNITOP',
'PELLING',
'PENCH',
'PHAGWARA',
'PHALODI',
'PINJORE',
'PONDICHERRY',
'POOVAR',
'PORBANDAR',
'PORT BLAIR',
'POSHINA',
'PRAGPUR',
'PUNE',
'PURI',
'PUSKHAR',
'PUTTAPARTHI',


'RAI BAREILLY',
'RAICHAK',
'RAIPUR',
'RAJASTHAN',
'RAJGIR',
'RAJKOT',
'RAJPIPLA',
'RAJSAMAND',
'RAJAHMUNDRY',
'RAMESHWARAM',
'RAM NAGAR',
'RAMGARH',
'RANAKPUR',
'RANCHI',
'RANIKHET',
'RANNY',
'RANTHAMBORE',
'RATNAGIRI',
'RAVANGLA',
'RISHIKESH',
'RISHYAP',
'ROHETGARH',
'ROURKELA',

'SAJAN',
'SALEM',
'SAPUTARA',
'SASAN GIR',
'SATTAL',
'SAWAI MADHOPUR',
'SAWANTWADI',
'SECUNDERABAD',
'SHILLONG',
'SHIMLA',
'SHIMLIPAL',
'SHIRDI',
'SHARAVANBELGOLA',
'SHIVANASAMUDRA',
'SIANA',
'SILIGURI',
'SILVASSA',
'SIVAGANGA DISTRICT',
'SOLAN',
'SONAULI',
'SRINAGAR',
'SUNDERBAN',
'SURAT',

'TANJORE',
'TAPOLA',
'TARAPITH',
'THANE',
'THEKKADY',
'THIRVANNAMALAI',
'THIRUVANANTHAPURAM',
'TIRUCHIRAPALLI',
'TIRUPUR',
'TIRUPATI',
'THRISSUR',

'UDAIPUR',
'UDHAMPUR',
'UDUPI',
'UJJAIN',
'UTTARKASHI',

'VADODARA',
'VAGAMON',
'VARKALA',
'VAPI',
'VARANASI',
'VELANKANNI',
'VELLORE',
'VERAVAL',
'VIJAYAWADA',
'VIKRAMGADH',
'VISHAKAPATNAM',

'WAYANAD',
'WANKANER',

'YAMUNOTRI',
'YERCAUD',
'YUKSOM'
        
      ],
      checkbox: false,
    }),

    computed: {
      checkboxErrors () {
        const errors = []
        if (!this.$v.checkbox.$dirty) return errors
        !this.$v.checkbox.checked && errors.push('You must agree to continue!')
        // The above text in orange is a sort of alert which users get when they fail to fill a particular section in a form 
        return errors
      },
      selectErrors () {
        const errors = []
        if (!this.$v.select.$dirty) return errors
        !this.$v.select.required && errors.push('Item is required')
        return errors
      },
      nameErrors () {
        const errors = []
        if (!this.$v.name.$dirty) return errors
        !this.$v.name.maxLength && errors.push('Item must be at most 10 characters long')
        !this.$v.name.required && errors.push('Item is required.')
        return errors
      },
      emailErrors () {
        const errors = []
        if (!this.$v.email.$dirty) return errors
        !this.$v.email.email && errors.push('Must be valid')
        !this.$v.email.required && errors.push('Item is required')
        return errors
      },
    },

    methods: {
      submit () {
        this.$v.$touch()
      },
      clear () {
        this.$v.$reset()
        this.name = ''
        this.email = ''
        this.select = null
        this.checkbox = false
      },
    },
  }
</script>
<style>
.hey {color:rgb(47, 64, 143) ;
font-family: Arial;
/* this can hange the color and font of text */
}
</style>