# notes-api-client

Notes

- API version: 1.0.0

The “Notes”,  a simple application allowing user to store its everyday notes.


*Automatically generated by the [OpenAPI Generator](https://openapi-generator.tech)*

## Requirements

Building the API client library requires:

1. Java 1.8+
2. Maven/Gradle

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn clean install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn clean deploy
```

Refer to the [OSSRH Guide](http://central.sonatype.org/pages/ossrh-guide.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
  <groupId>com.pwl</groupId>
  <artifactId>notes-api-client</artifactId>
  <version>0.0.1-SNAPSHOT</version>
  <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "com.pwl:notes-api-client:0.0.1-SNAPSHOT"
```

### Others

At first generate the JAR by executing:

```shell
mvn clean package
```

Then manually install the following JARs:

- `target/notes-api-client-0.0.1-SNAPSHOT.jar`
- `target/lib/*.jar`

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

import com.pwl.client.*;
import com.pwl.client.auth.*;
import com.pwl.api.v1.model.*;
import com.pwl.client.v1.NotesApi;

public class NotesApiExample {

    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("http://localhost");
        
        NotesApi apiInstance = new NotesApi(defaultClient);
        String title = "title_example"; // String | Note title
        String text = "text_example"; // String | Note text
        String tag = "BUSINESS"; // String | note tag
        try {
            Note result = apiInstance.addNote(title, text, tag);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling NotesApi#addNote");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*NotesApi* | [**addNote**](docs/NotesApi.md#addNote) | **POST** /notes | Add a new note
*NotesApi* | [**deleteNote**](docs/NotesApi.md#deleteNote) | **DELETE** /notes/{id} | Delete note
*NotesApi* | [**getNotes**](docs/NotesApi.md#getNotes) | **GET** /notes | Return notes with search criteria
*NotesApi* | [**updateNote**](docs/NotesApi.md#updateNote) | **PUT** /notes | Update an existing note


## Documentation for Models



## Documentation for Authorization

All endpoints do not require authorization.
Authentication schemes defined for the API:

## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author

p.pawliszcze@gmail.com

