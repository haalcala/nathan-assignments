# 7 XML Parser

Sample command:

    parst_xml file1.xml

Sample output:

    file1.xml
        xml
        ├ tag1
        │  ├ tag2 (attr1="this is attr1 value")
        │  └ tag3
        └ tag2
        ├ tag3
        │  └ "Hello world"
        └ tag3
            └ "another text"

Data:

    <xml>
        <tag1>
            <tag2 attr1="this is attr1 value"/>
            <tag3><tag3/>
        </tag1>
        <tag2 attr2="tag2 value">
            Hello world
        </tag2>
        <tag3>another text</tag3>
    </xml>
