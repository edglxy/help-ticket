# Command used by this project

### Run these command
- composer update
- npm update

#### Project Idea
1. User can create a new help ticket
2. Admin can reply on help ticket
3. Admin can reject or resolve the ticket
4. When admin update on the ticket then user will get one notification via email that ticket status is updated
5. User can give ticket title and description
6. User can upload a document like pdf or image

#### Table Structure
1. Tickets 
    - title (string) {required} 
    - description (text) {required}
    - status (open {default}, resolved, rejected) 
    - attachment(string) {nullable}
    - user_id {required} filled by laravel
    - status_changed_by_id {nullable}
2. Replies 
    - body (text) {required}
    - user_id {required} filled by laravel
    - ticket_id {required} filled by laravel

#### Commands
To create migration, resource controller, and form request at the same time type the command:
- php artisan make:model Ticket -m -r -R
- php artisan migrate

To see the list of route of this application:
- php artisan route:list

To create a new component from view:
- php artisan make:component Textarea
- php artisan make:component file-input