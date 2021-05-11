1) Textfeld
 ```xml
<label>Textfeld</label>
<config>
  <type>input</type>
  <size>20</size>
  <max>30</max>
  <eval>trim</eval>
</config>
 ```

2) Datumsfeld
```xml
<label>Datumsfeld</label>
<config>
  <type>input</type>
  <size>8</size>
  <max>8</max>
  <eval>date</eval>
  <checkbox>1</checkbox>
</config>
 ```

3) Checkbox
```xml
<label>Checkbox</label>
<config>
  <type>check</type>
</config>
 ```

4) Textarea
 ```xml
<label>Textarea</label>
<config>
  <type>text</type>
  <cols>24</cols>
  <rows>3</rows>
</config>
 ```

5) Textarea mit RTE
```xml
<label>Textarea</label>
<config>
  <type>text</type>
  <cols>24</cols>
  <rows>3</rows>
</config>
<defaultExtras>richtext[*]:rte_transform[mode=ts_css]</defaultExtras>
 ```

6) Radio-Buttons
 ```xml
<label>Radiobuttons</label>
<config>
  <type>radio</type>
  <items type="array">
    <numIndex index="0" type="array">
      <numIndex index="0">Auswahl1</numIndex>
      <numIndex index="1">wert1</numIndex>
    </numIndex>
    <numIndex index="1" type="array">
      <numIndex index="0">Auswahl2</numIndex>
      <numIndex index="1">wert2</numIndex>
    </numIndex>
    <numIndex index="3" type="array">
      <numIndex index="0">Auswahl3</numIndex>
      <numIndex index="1">wert3</numIndex>
    </numIndex>
  </items>
</config>
 ```

7) Selectbox mit fixen Werten
 ```xml
<label>Selectbox</label>
<config>
  <type>select</type>
  <items type="array">
    <numIndex index="0" type="array">
      <numIndex index="0">Auswahl1</numIndex>
      <numIndex index="1">wert1</numIndex>
    </numIndex>
    <numIndex index="1" type="array">
      <numIndex index="0">Auswahl2</numIndex>
      <numIndex index="1">wert2</numIndex>
    </numIndex>
    <numIndex index="3" type="array">
      <numIndex index="0">Auswahl3</numIndex>
      <numIndex index="1">wert3</numIndex>
    </numIndex>
  </items>
</config>
 ```

8) Selectbox mit Mehrfachauswahl
 ```xml
<label>Selectbox mehrfach</label>
<config>
  <type>select</type>
  <items type="array">
    <numIndex index="0" type="array">
      <numIndex index="0">Auswahl1</numIndex>
      <numIndex index="1">wert1</numIndex>
    </numIndex>
    <numIndex index="1" type="array">
      <numIndex index="0">Auswahl2</numIndex>
      <numIndex index="1">wert2</numIndex>
    </numIndex>
    <numIndex index="3" type="array">
      <numIndex index="0">Auswahl3</numIndex>
      <numIndex index="1">wert3</numIndex>
    </numIndex>
  </items>
  <maxitems>3</maxitems>
  <size>3</size>
</config>
 ```

Hier besteht auch die Möglichkeit, einzelne Werte zur Mehrfachauswahl freizugeben. Dies wird mit

```xml 
<multiple>1</multiple>
 ```
realisiert.

9) Selectbox aus Datenbank-Abfrage

 ```xml
<label>Selectbox aus DB</label>
<config>
  <type>select</type>
  <items type="array">
    <numIndex index="0" type="array">
      <numIndex index="0"></numIndex>
      <numIndex index="1"></numIndex>
    </numIndex>
  </items>
  <foreign_table>tt_content</foreign_table>
  <foreign_table_where>
     AND tt_content.pid = 22
  </foreign_table_where>
</config>
 ```

10) Auswahl einer Seite

 ```xml
<config>
  <type>group</type>
  <internal_type>db</internal_type>
  <allowed>pages</allowed>
  <size>1</size>
  <maxitems>1</maxitems>
  <minitems>0</minitems>
  <show_thumbs>1</show_thumbs>
</config>
 ```