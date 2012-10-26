== Zaakpay-demo

Zaakpay-demo is a rails application that demonstrates integration of a ruby-on-rails application with Zaakpay's api. It follow the php-demo implementation in functionality.

== Which are the relevant code files?
- Checksum processing logic is in lib/zaakpay.rb
- app/controllers/payments_controller.rb contains actions where URls are routed. Routing declarations are in config/routes.rb
- All the views are contained in app/views/payments,
  merchant_test.html.erb is equivalent to merchant_test.html of the php-demo
  post_to_zaakpay.html.erb is equivalent to posttozaakpay.php
  z_response.html.erb is equivalent to response.php

== How to run it?
- ruby, rubygems and rails must be installed (best instructions here http://rubyonrails.org/download)
- goto app directory and run 'bundle install' (needs internet connection)
- run 'rails server' if above succeeds
- goto 'localhost:3000/merchant_test'
- To test the response part, the app must be deployed on a public server.
For a local running app, curl could be used. eg -

curl -d "merchantIdentifier=b19e8f103bce406cbd&orderId=223453&responseTime=2011-08-30&responseCode=123&responseDescription=some-description&checksum=checksum123" localhost:3000/z_response


