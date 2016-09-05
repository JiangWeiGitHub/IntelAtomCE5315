# Preconditions for Testing

### Defautl Parameters
  + Default Users: 
    - `alice`
    ```
      // first user & admin
      {
        uuid: aliceUUID,
        username: 'alice',
        password: null,
        avatar: null,
        email: null,
        isFirstUser: true,
        isAdmin: true,
        home: aliceHome,
        library: aliceLib
      }
    ```
    - `bob`
    ```
      // admin
      {
        uuid: bobUUID,
        username: 'bob',
        password: null,
        avatar: null,
        email: null,
        isAdmin: true,
        home: bobHome,
        library: bobLib
      }
    ```
   
    - `frank`
    ```
      // admin
      {
        uuid: frankUUID,
        username: 'frank',
        password: null,
        avatar: null,
        email: null,
        isAdmin: true,
        home: frankHome,
        library: frankLib
      }
    ```
    
    - `henry`
    ```
      // admin
      {
        uuid: henryUUID,
        username: 'henry',
        password: null,
        avatar: null,
        email: null,
        isAdmin: true,
        home: henryHome,
        library: henryLib
      }
    ```      
    
    - `ian`
    ```
      // admin
      {
        uuid: ianUUID,
        username: 'ian',
        password: null,
        avatar: null,
        email: null,
        isAdmin: true,
        home: ianHome,
        library: ianLib
      }
    ```      
    
    - `charlie`
    ```
      // normal user
      {
        uuid: charlieUUID,
        username: 'charlie',
        password: null,
        avatar: null,
        email: null,
        home: charlieHome,
        library: charlieLib
      }
    ```
    
    - `david`
    ```
      // normal user
      {
        uuid: davidUUID,
        username: 'david',
        password: null,
        avatar: null,
        email: null,
        home: davidHome,
        library: davidLib
      }
    ```
    
    - `jane`
    ```
      // normal user
      {
        uuid: janeUUID,
        username: 'jane',
        password: null,
        avatar: null,
        email: null,
        home: janeHome,
        library: janeLib
      }
    ```

    - `kate`
    ```
      // normal user
      {
        uuid: kateUUID,
        username: 'kate',
        password: null,
        avatar: null,
        email: null,
        home: kateHome,
        library: kateLib
      }
    ```

  + Default Drivers: 
 ```
*********************************************************************

   {
     label: 'one owner & empty writelist & empty readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [],
     readlist: [],
     cache: true
   }
   
*********************************************************************
   
   {
     label: 'one owner & one admin in writelist & empty readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID ],
     readlist: [],
     cache: true
   }
   
   {
     label: 'one owner & two admins in writelist & empty readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID, frankUUID ],
     readlist: [],
     cache: true
   }
   
   {
     label: 'one owner & one admin one normal user in writelist & empty readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID, charlieUUID ],
     readlist: [],
     cache: true
   }
   
   {
     label: 'one owner & one normal user in writelist & empty readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ charlieUUID ],
     readlist: [],
     cache: true
   }
   
   {
     label: 'one owner & two normal users in writelist & empty readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ charlieUUID, davidUUID ],
     readlist: [],
     cache: true
   }
   
*********************************************************************

   {
     label: 'one owner & empty writelist & one admin in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [],
     readlist: [ bobUUID ],
     cache: true
   }

   {
     label: 'one owner & empty writelist & two admins in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [],
     readlist: [ bobUUID, frankUUID ],
     cache: true
   }

   {
     label: 'one owner & empty writelist & one admin and one normal user in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [],
     readlist: [ bobUUID, davidUUID ],
     cache: true
   }

   {
     label: 'one owner & empty writelist & one normal user in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [],
     readlist: [ davidUUID ],
     cache: true
   }

   {
     label: 'one owner & empty writelist & two normal users in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [],
     readlist: [ janeUUID, davidUUID],
     cache: true
   }

*********************************************************************

   {
     label: 'one owner & one admin in writelist & one admin in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID ],
     readlist: [ frankUUID ],
     cache: true
   }
   
   {
     label: 'one owner & two admins in writelist & one admin in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID, frankUUID ],
     readlist: [ henryUUID ],
     cache: true
   }
   
   {
     label: 'one owner & one admin one normal user in writelist & one admin in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID, charlieUUID ],
     readlist: [ frankUUID ],
     cache: true
   }
   
   {
     label: 'one owner & one normal user in writelist & one admin in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ charlieUUID ],
     readlist: [ bobUUID ],
     cache: true
   }
   
   {
     label: 'one owner & two normal users in writelist & one admin in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ charlieUUID, davidUUID ],
     readlist: [ bobUUID ],
     cache: true
   }

*********************************************************************

   {
     label: 'one owner & one admin in writelist & two admins in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID ],
     readlist: [ frankUUID, henryUUID ],
     cache: true
   }
   
   {
     label: 'one owner & two admins in writelist & two admins in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID, frankUUID ],
     readlist: [ henryUUID, ianUUID ],
     cache: true
   }
   
   {
     label: 'one owner & one admin one normal user in writelist & two admins in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID, charlieUUID ],
     readlist: [ frankUUID, henryUUID ],
     cache: true
   }
   
   {
     label: 'one owner & one normal user in writelist & two admins in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ charlieUUID ],
     readlist: [ bobUUID, frankUUID ],
     cache: true
   }
   
   {
     label: 'one owner & two normal users in writelist & two admins in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ charlieUUID, davidUUID ],
     readlist: [ bobUUID, frankUUID ],
     cache: true
   }

*********************************************************************

   {
     label: 'one owner & one admin in writelist & one admin and one normal user in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID ],
     readlist: [ frankUUID, davidUUID ],
     cache: true
   }
   
   {
     label: 'one owner & two admins in writelist & one admin and one normal user in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID, frankUUID ],
     readlist: [ henryUUID, kateUUID ],
     cache: true
   }
   
   {
     label: 'one owner & one admin one normal user in writelist & one admin and one normal user in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID, charlieUUID ],
     readlist: [ frankUUID, kateUUID ],
     cache: true
   }
   
   {
     label: 'one owner & one normal user in writelist & one admin and one normal user in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ charlieUUID ],
     readlist: [ bobUUID, davidUUID ],
     cache: true
   }
   
   {
     label: 'one owner & two normal users in writelist & one admin and one normal user in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ charlieUUID, davidUUID ],
     readlist: [ bobUUID, janeUUID ],
     cache: true
   }

*********************************************************************

   {
     label: 'one owner & one admin in writelist & one normal user in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID ],
     readlist: [ davidUUID ],
     cache: true
   }
   
   {
     label: 'one owner & two admins in writelist & one normal user in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID, frankUUID ],
     readlist: [ kateUUID ],
     cache: true
   }
   
   {
     label: 'one owner & one admin one normal user in writelist & one normal user in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID, charlieUUID ],
     readlist: [ kateUUID ],
     cache: true
   }
   
   {
     label: 'one owner & one normal user in writelist & one normal user in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ charlieUUID ],
     readlist: [ davidUUID ],
     cache: true
   }
   
   {
     label: 'one owner & two normal users in writelist & one normal user in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ charlieUUID, davidUUID ],
     readlist: [ janeUUID ],
     cache: true
   }

*********************************************************************

   {
     label: 'one owner & one admin in writelist & two normal users in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID ],
     readlist: [ davidUUID, janeUUID ],
     cache: true
   }
   
   {
     label: 'one owner & two admins in writelist & two normal users in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID, frankUUID ],
     readlist: [ kateUUID, janeUUID ],
     cache: true
   }
   
   {
     label: 'one owner & one admin one normal user in writelist & two normal users in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ bobUUID, charlieUUID ],
     readlist: [ kateUUID, janeUUID ],
     cache: true
   }
   
   {
     label: 'one owner & one normal user in writelist & two normal users in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ charlieUUID ],
     readlist: [ davidUUID, kateUUID ],
     cache: true
   }
   
   {
     label: 'one owner & two normal users in writelist & two normal users in readlist',
     fixedOwner: true,
     URI: 'fruitmix',
     uuid: aliceHome,
     owner: [ aliceUUID ],
     writelist: [ charlieUUID, davidUUID ],
     readlist: [ janeUUID, kateUUID ],
     cache: true
   }

*********************************************************************


*********************************************************************


*********************************************************************


*********************************************************************



*********************************************************************

















```


