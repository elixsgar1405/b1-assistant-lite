# B1 Alexa SAmple
A small Alexa Skill integration with SAP Business One for the SMB Summit 2019 Hackathon
[![SAP](https://i.imgur.com/80Ohjn6.png)](http://cloudplatform.sap.com/)

## More info:
Detailed how to of a similar app - http://bit.ly/2dGJv9d

## Prerequisites
* [Amazon developer account](https://developer.amazon.com/)
* [Configure your SAP Cloud Platform enviroment](https://developers.sap.com/uk/tutorials/hcp-cf-getting-started.html)


## Installation - 
### Step 1 - Deployment of the Backend
* Download or clone this repository.
* Update the hostname and other parameters on the [MANIFEST](manifest.yml) file.
* From the root directory of this app. Execute:
```sh
$ cf push --random-route
```
At the end of the process, Cloud Platform should return a Route as shown below. We will need it later.
![SAP](https://i.imgur.com/exuU9vu.png)

### Step 2 - Creation of Alexa Skill
* Follow [these steps to create a new Alexa Skill](https://developer.amazon.com/docs/devconsole/create-a-skill-and-choose-the-interaction-model.html#create-a-new-skill)
* When asked for a *Model* choose *Custom*.
* Once the skill is created, option JSON Editor in the skill menu. Replace its content [with our model](skill/IntentSchema.json)
* On the skills endpoit, set it with the route showed previously.
* For the certificate option choose *My development endpoints is a sub-domain...*
* You are ready to test your skill

## Test
<img src="https://i.imgur.com/xkw6lXx.png" alt="drawing" width="600"/>
* You can test your skill from the development console (as shown above)
* Or from your Amazon Device, as long as it is logged with the same account you used on Amazon Developer

## License
B1 Assistant prototype is released under the terms of the MIT license. See [LICENSE](LICENSE) for more information or see https://opensource.org/licenses/MIT.
