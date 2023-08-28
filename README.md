# myfirstdjangorestapi

## Project Setup
Started off creating a project directory. Then I created a python virtual environment where I installed django and the djangorestframework. Afterwords I used django-admin to start a project called tutorial and start an app named quickstart. Next step is to sync our databases(migrate) and create an admin.

## Serializers
Imported a serializers class from the rest_framework created a UserSerializer class and GroupSerlializer class which is a subclass of the serializers.HyperlinkedModelSerializer. Using hyperlinked relations is better than primary key and other relationships for RESTful design

## Views
Imported User + Group models as wells as the Serializers. Also imported viewsets and permissions from the rest_framework. Created 2 Modelviewset classes called UserViewSet and GroupViewSet. The are simlar in that they allow the Users or Groups to be viewed or edited if you are authenticated.

## URLs
Here we imported routers from the rest framework and our views. Then we created a default router using routers.DefaultRouter() and registered the router with users and group views. Then we included router.urls path in the urlpatterns and added an api-auth/ path which includes rest_framework.urls.

## Pagination
In settings crated a REST_FRAMEWORK variable and added pagination with page size 10

## Settings
Also added rest_framework in the django Settings

## Testing
To test used httpie command http -a admin:password123 http://127.0.0.1:8000/users/
