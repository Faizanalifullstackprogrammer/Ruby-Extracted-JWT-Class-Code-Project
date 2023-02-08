# Extracted JWT Module Class

![Linter workflow](https://github.com/Div685/Ruby-Extracted-JWT-Class/actions/workflows/linters.yml/badge.svg)

## About the Project

The main purpose of this project was to extract a single class from the project. A piece of code I'm proud of and why? 
> I decided to use the `JWT_auth` module class I coded while I was building this API. Why am I proud of this particular class? Well, it's because when I was creating Rails API I didn't have any knowledge about JWT authentication and I had to build user authentication considering the deadline. so I've done some research, read the documentation, and learned JWT authentication from scratch and I was able to implement it in this project. 

This Class has following features:
- created `JWT_auth` module class
- Added `Secret_key` and `Expiry_date` constant
- `Secret_key` and `Expires_In` constant has stored in the credential file.
- Added function to encode the token.
- Added function to decode the encoded token.
- Added function so token can pass through Authorization in API header.
- Added function to check for an authorized user via login method.
- `logged_in_user` method confirmed the decoded token to find the current user.
- To authorize the users, this app uses [JWT](https://jwt.io/) and [Rack-cors](https://github.com/cyu/rack-cors)


## Built With

* [Ruby on Rails](https://rubyonrails.org/)
* [Ruby](https://www.ruby-lang.org/en/)


## Getting Started

To get a local copy up and running follow these simple example steps.
- [ ] Open your terminal
- [ ]  Navigate to the directory where you will like to install the repo by running `cd FOLDER-NAME` 
- [ ] Clone this repository
 > `git clone https://github.com/Div685/Ruby-Extracted-JWT-Class.git`
- [ ] To install all dependencies and necessary gems, run `bundle installl`, `yarn install`

## How to allow the frontend app to interact with this API
1. Go to puma.rb, located in config/puma.rb, and rewrite the port from 3000 to 3001 like below:
e.g. `port ENV.fetch("PORT") { 3001 }`

2. Go to cors.rb, located in config/initializers, and rewrite the origins path for your frontend path in both local and production


## Authentication

- To manage Appointments and items, user needs to login with a username and a password. Then you need to pass token, which is issued when user logged in, Pass the token in the header like below:
`headers: {
  'Content-Type': 'application/json',
  Authorization: `Bearer ${token}`,
},`
- To manage items, user or administrator needs to log in as a admin.
- To login as a admin Account follow the section below called "How to create admin user".


## Authors

👤 **Mian Faizan Ali Full Stack Programmer**

- GitHub: [@Faizanalifullstackprogrammer](https://github.com/Faizanalifullstackprogrammer)
- Twitter: [@mianfaizanali](https://twitter.com/mianfaizanali)
- LinkedIn: [Mianfaizanali](https://pk.linkedin.com/in/mianfaizanali)


## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

Feel free to connect anytime


## Contributing

Contributions, issues, and feature requests are welcome!
Feel free to check the [issues page](../../issues).

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## Show your support

Give a ⭐️ if you like this project!

## Acknowledgements
* [Ruby on Rails guide](https://guides.rubyonrails.org/api_documentation_guidelines.html)
* [JWT](https://jwt.io/)
* [Rack-cors](https://github.com/cyu/rack-cors)
