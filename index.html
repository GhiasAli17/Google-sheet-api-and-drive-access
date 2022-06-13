const {google} = require('googleapis');
let privatekey = require("./private_keys.json");

const auth = new google.auth.GoogleAuth({
    keyFile: "private_keys.json", //the key file
    //url to spreadsheets API
    scopes: ["https://www.googleapis.com/auth/spreadsheets",
    "https://www.googleapis.com/auth/drive"], 
});

const drive=google.drive({version: 'v3',auth});
var spId;
//async function createAndUploadFile(auth){
 
  // let  fileMetaData = {
  //   'name':'testSheet',
  //   'parent':['1WR2Asxw5lJoZwb0ljG_HavRZCAim-9b3']
  // }

  // let media = {
  //   mimeType: 'image/png',
  //   body : FileSystem.crea
  // }
//}

async function callAPIs(){
const authClientObject = await auth.getClient();
const googleSheetsInstance = google.sheets({ version: "v4", auth: authClientObject });

//creating spread sheet through service account
const requestBody = {
  properties: {
    title: "testSheet9"
  },
};


await googleSheetsInstance.spreadsheets.create({
  requestBody,
  fields: '',
}, async (err, spreadsheet) =>{
  if (err) {
    // Handle error.
    console.log(err);
  } else {
    //console.log('spreadsheet', spreadsheet);
    spId =  spreadsheet.data.spreadsheetId;
    console.log(`Spreadsheet ID: ${spreadsheet.data.spreadsheetId}`);

    // write to the file
    googleSheetsInstance.spreadsheets.values.update({
      auth, //auth object
      spreadsheetId:spId,
      range: "Sheet1!C3", 
      valueInputOption: "RAW", 
      resource: {
          values: [['sheet5', 'b.ed']]
      },
  }, (err, result) => {
      if (err) {
        // Handle error
        console.log('error-------', err);
      } else {
        console.log(' cells updated.');
       
      }
    });

    var body = {
      'type': 'user',
      'role': 'reader',
      'emailAddress': 'ghiasali17@gmail.com',
    };

    // var drive=google.drive({version: 'v3',auth});

     drive.permissions.create({
      'fileId': spId,  //sheetID returned from create sheet response
      'resource': body,
    }, function(err, response) {if (err) {
      console.error('error-------', err);
      return;
      } else{
        ///console.log(JSON.parse(JSON.stringify(response))) ;
        console.log('successfully shared ')
      }
    });

    
    setTimeout(()=>{

      const email = "ghiasali17@gmail.com"; // Please set the email address you want to delete the permission.
    
    drive.permissions.list(
      { fileId: spId, fields: "permissions(emailAddress,id)" },
      function (err, response) {
        if (err) {
          console.error("error-------", err);
          return;
        } else {
          var permission = response.data.permissions.find(({ emailAddress }) => emailAddress == email);
          if (permission) {
            console.log('permissionId', permission.id)
            drive.permissions.delete({ fileId: spId, permissionId: permission.id },
              function (err, response) {
                if (err) {
                  console.error("error-------", err);
                  return;
                } else {
                 // console.log(JSON.parse(JSON.stringify(response)));
                  console.log('successfully  removed access after 30s');
                }
              });
          }
        }
      });
    
    
    },30000)


  }
})
   
    // var permissions = [
    //   {
    //     'type': 'user',
    //     'role': 'writer',
    //     'emailAddress': 'ghiasali17@gmail.com'
    //   },
      // {
      //   'type': 'otheruser',
      //   'role': 'reader',
      //   'emailAddress': 'otheruser@gmail.com'
      // }
    //];

  //   // write to the file
  //   googleSheetsInstance.spreadsheets.values.update({
  //     auth, //auth object
  //     spreadsheetId:spId,
  //     range: "Sheet1!C3", 
  //     valueInputOption: "RAW", 
  //     resource: {
  //         values: [['sheet4', 'b.ed']]
  //     },
  // }, (err, result) => {
  //     if (err) {
  //       // Handle error
  //       console.log('error-------', err);
  //     } else {
  //       console.log(' cells updated.');
       
  //     }
  //   });

    // var body = {
    //   'type': 'user',
    //   'role': 'reader',
    //   'emailAddress': 'ghiasali17@gmail.com',
    // };

    // // var drive=google.drive({version: 'v3',auth});

    //  drive.permissions.create({
    //   'fileId': spId,  //sheetID returned from create sheet response
    //   'resource': body,
    // }, function(err, response) {if (err) {
    //   console.error('error-------', err);
    //   return;
    //   } else{
    //     ///console.log(JSON.parse(JSON.stringify(response))) ;
    //     console.log('successfully shared ')
    //   }
    // });

    
    // setTimeout(()=>{

    //   const email = "ghiasali17@gmail.com"; // Please set the email address you want to delete the permission.
    
    // drive.permissions.list(
    //   { fileId: spId, fields: "permissions(emailAddress,id)" },
    //   function (err, response) {
    //     if (err) {
    //       console.error("error-------", err);
    //       return;
    //     } else {
    //       var permission = response.data.permissions.find(({ emailAddress }) => emailAddress == email);
    //       if (permission) {
    //         console.log('permissionId', permission.id)
    //         drive.permissions.delete({ fileId: spId, permissionId: permission.id },
    //           function (err, response) {
    //             if (err) {
    //               console.error("error-------", err);
    //               return;
    //             } else {
    //              // console.log(JSON.parse(JSON.stringify(response)));
    //               console.log('successfully  deleted after 1000ms');
    //             }
    //           });
    //       }
    //     }
    //   });
    
    
    // },1000)
  }




// // spreadsheet id
// const spreadsheetId = "199MfsWshW5zGbpapi7_4yWX9oTzXOQ7KL7R-fqZTiUg";

// // Get metadata about spreadsheet
// const sheetInfo = await googleSheetsInstance.spreadsheets.get({
//     auth,
//     spreadsheetId,
// });

//Read from the spreadsheet
// const readData = await googleSheetsInstance.spreadsheets.values.get({
//     auth, //auth object
//     spreadsheetId:'1IqzcV1G6nLHRk6lmSGR319PawV8qmLwBNnpdCyGsodQ', // spreadsheet id
//     range: "Sheet1!C3:D3", //range of cells to read from.
// },(error,resopnse)=>{
//   if(error){
//     console.log('error ---',error)
//   }
//   else{
//     console.log('----',resopnse.data);
//   }
// })

// //write data into the google sheets
// await googleSheetsInstance.spreadsheets.values.update({
//     auth, //auth object
//     spreadsheetId,
//     range: "Sheet1!C3", 
//     valueInputOption: "RAW", 
//     resource: {
//         values: [['categories', 'b.ed']]
//     },
// }, (err, result) => {
//     if (err) {
//       // Handle error
//       console.log('error-------', err);
//     } else {
//       console.log(' cells updated.');
//     }
//   });



callAPIs()

 // Deleting a file
// async  function deletedata(){
//   var drive=google.drive({version: 'v3',auth});
//   // 05580536704833493268

//  try {
//   const result = await drive.permissions.delete({
//     fileId:'1IqzcV1G6nLHRk6lmSGR319PawV8qmLwBNnpdCyGsodQ',
//     permissionId:"05580536704833493268"
//   })

//   return {
//     statusCode: 200,
//     headers: {
//       'Access-Control-Allow-Origin': '*',

//     },
//     body: JSON.stringify({ ...result, Body: result.toString('utf-8') })
//   }
// } catch (e) {
//   console.log(e.message)
//   return { statusCode: 500, body: e.message }
// }
// }

//deletedata();


// getting permissionId of specific user

// async function getPermissionIdAndDelete(){

//   var drive=google.drive({version: 'v3',auth});
// const spId = "1IBejuYPd9_RjIshiTqsz3gsbLFUziyEgAfL0TAF2k14"; // Please set the file ID.
// const email = "ghiasali17@gmail.com"; // Please set the email address you want to delete the permission.

// drive.permissions.list(
//   { fileId: spId, fields: "permissions(emailAddress,id)" },
//   function (err, response) {
//     if (err) {
//       console.error("error-------", err);
//       return;
//     } else {
//       var permission = response.data.permissions.find(({ emailAddress }) => emailAddress == email);
//       if (permission) {
//         console.log('permissionId', permission.id)
//         drive.permissions.delete({ fileId: spId, permissionId: permission.id },
//           function (err, response) {
//             if (err) {
//               console.error("error-------", err);
//               return;
//             } else {
//              // console.log(JSON.parse(JSON.stringify(response)));
//               console.log('successfully  deleted');
//             }
//           });
//       }
//     }
//   });

// }

// getPermissionIdAndDelete();

