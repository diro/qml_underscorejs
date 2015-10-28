# qml_underscorejs
 A port of underscore.js to Qt/QML.
The original Underscore. js will attach _ object to this object , but in QML we cannot add global object.
Please refer to:
http://doc.qt.io/qt-5/qtqml-javascript-hostenvironment.html#javascript-environment-restrictions

In this port, we attach _ object to the global object Qt, and then you could use all the underscore.js function in your QML.

# example
    import "underscore.js" as Underscore
    Item
    {
    ...
    enabled: Qt._.every([inptBoxIP, inptBoxUser, inptBoxPassword],
                                          function f(e) {
                                            return e.text !== ""
                                          })
    ...
    }
                                  
