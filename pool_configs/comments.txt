{
    "enabled": false,
    "coin": "verium.json",

	//pools wallet address
    "address": "n4jSe18kZMCdGcZqaYprShXW6EH1wivUK1",

	//only for nomp standalone use. remove for mpos usage
    "rewardRecipients": {
        "n37vuNFkXfk15uFnGoVyHZ6PYQxppD3QqK": 1.5,
        "22851477d63a085dbc2398c8430af1c09e7343f6": 0.1
    },

	//only for nomp standalone use. set to false for mpos usage
    "paymentProcessing": {
        "enabled": true,
        "paymentInterval": 20,
        "minimumPayment": 70,
        "daemon": {
            "host": "127.0.0.1",
            "port": 19332,
            "user": "testuser",
            "password": "testpass"
        }
    },

	//port difficulty settings. edit as needed
	"ports": {
        "3332": {
            "diff": 0.005,
            "varDiff": {
              "minDiff": 0.0007,
              "maxDiff": 0.03,
              "targetTime": 90,
              "retargetTime": 120,
              "variancePercent": 30
            
            }
        },
        "3333": {
            "diff": 0.03,
            "varDiff": {
                "minDiff": 0.03,
                "maxDiff": 0.1,
                "targetTime": 90,
                "retargetTime": 120,
                "variancePercent": 30
            }
        },
        "3334": {
            "diff": 0.1,
            "varDiff": {
                "minDiff": 0.1,
                "maxDiff": 0.3,
                "targetTime": 90,
                "retargetTime": 120,
                "variancePercent": 30
            }
        },
		"3335": {
            "diff": 0.03
        },
		"3336": {
            "diff": 0.1
        },
		"3337": {
            "diff": 0.25
        },
		
    },

	//wallet rpc connection details
    "daemons": [
        {
            "host": "127.0.0.1",
            "port": 33987,
            "user": "poolrpc",
            "password": "poolrpcpasswd"
        }
    ],

    "p2p": {
        "enabled": false,
        "host": "127.0.0.1",
        "port": 19333,
        "disableTransactions": true
    },

	//set to true for mpos usage
    "mposMode": {
        "enabled": false,
        "host": "127.0.0.1",
        "port": 3306,
        "user": "dbuser", //dont use the root user here
        "password": "dbpasswd",
        "database": "dbname", //defined at the mpos installation
        "checkPassword": true,
        "autoCreateWorker": false
    }

}
