https://stackoverflow.com/a/71235559

# Unofffical QtGraphicalEffects for Qt6

**The QtGraphicalEffects module has been deprecated and is no longer part of Qt.**

However, to unofficially employ QtGraphicalEffects in Qt 6, do the following:

$ git clone git://code.qt.io/qt/qtgraphicaleffects.git
$ cd qtgraphicaleffects/
$ git checkout 59ab3e11433a5157aac0f3af7c0d7fe70a373373 & cd ..
$ ~/Qt/<VERSION>/gcc_64/bin/qmake qtgraphicaleffects
$ make
$ find qtgraphicaleffects/src/effects/ -maxdepth 1 -name \*.qml -exec cp {} qml/QtGraphicalEffects \;
$ cp -r qtgraphicaleffects/src/effects/private/ qml/QtGraphicalEffects
$ cp -r qml/QtGraphicalEffects ~/Qt/<VERSION>/gcc_64/qml/
