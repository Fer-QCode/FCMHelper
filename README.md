# FCMHelper
Java Example::

String TOKEN_TEST = "c3PLwtxrsyw:APA91bFZFfFaqFqJG4ZVmekRqniww2qcXjShVxqlwxgEYVeMVwwIqCwZomSV_mYdX_nRsMzGt7dLLESfbZuhTQ1hXvvt-n51qYyxa9FcGOu1TTO3cJsRz69Ius1vYFOT_eUu8rjGV-gY";
System.out.println("token:: " + TOKEN_TEST);
JsonObject dataObject = new JsonObject(); 
dataObject.addProperty("title", "Push Notification Test");
dataObject.addProperty("body", "Notification from " + this.getClass().getCanonicalName());
FCMHelper fcm = FCMHelper.getInstance();
try {
    fcm.sendData(FCMHelper.TYPE_TO, TOKEN_TEST, dataObject);
} catch (Exception e) {
    System.out.println("Error sendingData... " + e.getLocalizedMessage());
e.printStackTrace();
}



POM::
<dependency>
  <groupId>com.google.code.gson</groupId>
  <artifactId>gson</artifactId>
  <version>2.7</version>
</dependency>
<!-- https://mvnrepository.com/artifact/org.apache.httpcomponents/httpclient -->
<dependency>
  <groupId>org.apache.httpcomponents</groupId>
  <artifactId>httpclient</artifactId>
  <version>4.5.2</version>
</dependency>
