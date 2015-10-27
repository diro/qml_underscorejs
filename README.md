# qml_underscorejs
Underscore.js for QML
The original Underscore.js will attach [_] object to [this] , but in QML we cannot add global object. http://doc.qt.io/qt-5/qtqml-javascript-hostenvironment.html#javascript-environment-restrictions


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
                                  
