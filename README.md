# MainWebsite-Documentation

All Documentation, designs, etc. that are not in other MainWebsite repositories will be here.

## Frontend

The frontend tech stack broadly consists of a Node environment in Javascript running React.js with routing, deployed on GitHub Pages. It also contains fragments of HTML and has all components styled with CSS.

Each deployment is thoroughly tested, firstly with unit and integration testing to ensure a stable development branch. Then, the development branch undergoes review every week with manual E2E testing on multiple platforms / devices to ensure quality assurance.

## Backend

The backend tech stack consists of a Node environment in Javascript running Express.js, deployed as an AWS Lambda function. It uses a PostgreSQL database hosted on AWS RDS to securely store basic user information.

Each endpoint is thoroughly tested, first manually using resources like Postman on top of unit testing to ensure a stable development branch. Then, the development branch undergoes full E2E testing in conjunction with the frontend branch on multiple platforms / devices to ensure quality assurance.

The Lambda function handles the heavy architecture by directly listening to each endpoint as a proxy, supporting security practices that prevent malicious access to any endpoint, such as throttling.

The RDS Database utilizes VPC security groups to ensure connection is only established between itself and the Lambda function to prevent malicious access in the case that the host is leaked to face the public.