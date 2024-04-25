The Java Application Descriptor (JAD) file is a text file commonly used in conjunction with [[Java ME (Micro Edition)]] applications, particularly MIDlets, which are Java programs designed to run on mobile devices. JAD files are used to describe the properties and attributes of a Java ME application or MIDlet suite.

The JAD file contains information about the MIDlet suite, which is a collection of MIDlets packaged together. This information includes details about the MIDlet suite's configuration and its requirements.

JAD files include metadata such as the name of the MIDlet suite, the vendor, version, size, and a description. They also contain configuration data, such as which MIDlets are included in the suite and their specific properties. The JAD file is used by the device or application store to determine how to install the MIDlet suite. It includes URLs pointing to the [[Java Archive (JAR)|JAR]] file (where the actual application bytecode resides) and other information necessary for downloading and installing the application.

Common attributes in a JAD file include `MIDlet-Name`, `MIDlet-Version`, `MIDlet-Vendor`, `MIDlet-Jar-URL`, `MIDlet-Jar-Size`, and specific configuration properties for each MIDlet in the suite. The format of a JAD file is simple text with key-value pairs, making it easy to create and read. Each line in the file represents a property of the MIDlet suite.

JAD files can also specify the security and permission requirements for the MIDlet suite, indicating what actions the application is allowed to perform on the mobile device. It can include information about device compatibility and dependencies, ensuring that the MIDlet suite is only installed on compatible devices.

With the decline of Java ME in favor of more advanced mobile platforms like Android and iOS, the usage of JAD files has significantly decreased. In the context of Java ME, JAD files were often used for distributing MIDlet suites over the air (OTA) or through application stores.

>[!info]
>While JAD files are largely associated with legacy mobile applications, they were an important part of mobile application deployment in the era of feature phones and early smartphones.