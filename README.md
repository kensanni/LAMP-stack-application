# LAMP-stack-application


## Prerequisites
To follow along with this automation, you need to have the following

1. Ansible installed on your local machine
2. An Ubuntu instance with SSH key-based authentication


#### Installation and automation

1. Clone the repository to your local machine

    ```sh
    git clone https://github.com/kensanni/LAMP-stack-application.git
    ```
2. Navigate to the `LAMP-stack-application` directory
   
    ```bash
      cd LAMP-stack-application
    ```
    
3. Open the `main.yml` file in `mysql/defaults` directory and edit the file to pass in your database values. Leave the my_sql_user untouched.
    
    ```yml
    ---
    wp_mysql_db: wordpressDatabase
    wp_mysql_user: WORDPRESS_DATABASE_USER
    wp_mysql_password: WORDPRESS_DATABASE_PASSWORD
    my_sql_user: root
    ```
4. Open the `inventory` file and pass in your values. check the `inventory.example` file for guidance

5. On your terminal, make sure you're on the root directory of this project and run the command below
    
    ```bash
     ansible-playbook -i inventory wordpress.yml
    ```
 6. Once the command in step 5 has finished running, copy and paste in your server IP address into your browser. You should see a wordpress site on your browser.
