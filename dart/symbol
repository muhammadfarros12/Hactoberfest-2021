import 'dart:core'; 
import 'dart:mirrors'; 
import 'Foo.dart';  

main() { 
   Symbol lib = new Symbol("foo_lib");   
   //library name stored as Symbol 
   
   Symbol clsToSearch = new Symbol("Foo");  
   // class name stored as Symbol  
   
   if(checkIf_classAvailableInlibrary(lib, clsToSearch))  
   // searches Foo class in foo_lib library 
      print("class found.."); 
}  
   
bool checkIf_classAvailableInlibrary(Symbol libraryName, Symbol className) { 
   MirrorSystem mirrorSystem = currentMirrorSystem(); 
   LibraryMirror libMirror = mirrorSystem.findLibrary(libraryName); 
      
   if (libMirror != null) { 
      print("Found Library"); 
      print("checkng...class details.."); 
      print("No of classes found is : ${libMirror.declarations.length}"); 
      libMirror.declarations.forEach((s, d) => print(s));  
         
      if (libMirror.declarations.containsKey(className)) return true; 
      return false; 
   } 
}
