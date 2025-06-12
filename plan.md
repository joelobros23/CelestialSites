# Project Plan: CelestialSites

**Description:** A simplified web hosting platform allowing users to manage their domains and basic hosting configurations, built with Ruby on Rails, SQLite, Tailwind CSS, and Devise.


## Development Goals

- [ ] Configure Tailwind CSS using the `tailwindcss-rails` gem.
- [ ] Customize the Devise views to use Tailwind CSS for improved aesthetics.
- [ ] Implement user authentication using Devise, ensuring users can register, log in, and log out.
- [ ] Modify the Domain model to establish a relationship with the User model (one-to-many). Add `belongs_to :user` to the Domain model and `has_many :domains` to the User model.
- [ ] Update the Domains controller to ensure that only logged-in users can create, edit, and delete their own domains. Use `before_action :authenticate_user!` to require login.
- [ ] In the Domains controller's `create` action, set the `user_id` of the new domain to `current_user.id`.
- [ ] Modify the Domains index view to only display domains associated with the currently logged-in user. Use `@domains = current_user.domains`.
- [ ] Add validations to the Domain model (e.g., presence of name and plan, uniqueness of name within the user's domains).
- [ ] Implement different hosting plans with associated features (e.g., storage space, bandwidth). This can initially be done using a simple enum in the Domain model.
- [ ] Design a simple dashboard for users to manage their domains, profile, and plan details.
- [ ] Add a 'status' field to the Domain model to indicate whether the domain is active, pending, or suspended. Update the Domain scaffold accordingly.
- [ ] Add basic error handling and user feedback using flash messages.
- [ ] Implement role-based authorization (e.g., using Pundit or CanCanCan) to allow administrative users to manage all domains and users.
