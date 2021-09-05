# 30 Data Converter : XML to CSV

Sample command:

    convert_xml_to_csv file.xml file.csv


Sample output:
    tag1,tag2,tag3,tag4
    this is tag1,this is tag2,,
    ,Hello world,,
    ,,,another text


Data:
    <xml>
        <RecordSet>
            <Record>
                <tag1>This is tag1</tag1>
                <tag2 attr1="this is attr1 value">this is tag2</tag2>
                <tag3><tag3/>
            </Record>
            <Record attr2="tag2 value">
                <tag2>Hello world</tag2>
            </Record>
            <Record attr2="tag2 value">
                <tag4>another text</tag4>
            </Record>
        </RecordSet>
    </xml>

