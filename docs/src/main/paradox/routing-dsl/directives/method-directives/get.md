# get

Matches requests with HTTP method `GET`.

@@@ div { .group-scala }

## Signature

@@signature [MethodDirectives.scala](/akka-http/src/main/scala/akka/http/scaladsl/server/directives/MethodDirectives.scala) { #get }

@@@

## Description

This directive filters the incoming request by its HTTP method. Only requests with
method `GET` are passed on to the inner route. All others are rejected with a
@apidoc[MethodRejection], which is translated into a `405 Method Not Allowed` response
by the default @ref[RejectionHandler](../../rejections.md#the-rejectionhandler).

## Example

Scala
:  @@snip [MethodDirectivesExamplesSpec.scala]($test$/scala/docs/http/scaladsl/server/directives/MethodDirectivesExamplesSpec.scala) { #get-method }

Java
:  @@snip [MethodDirectivesExamplesTest.java]($test$/java/docs/http/javadsl/server/directives/MethodDirectivesExamplesTest.java) { #get }
