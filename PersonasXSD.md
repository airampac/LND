# Personas

Proporcionar un XML schema que refleje esta jerarquía suponiendo que nacimiento es un elemento opcional y hay al menos una dirección. Para la jerarquía de datos que se muestra a continuación, y teniendo en cuenta los siguientes requisitos:
    
   • Dependiendo de si la persona es hombre o mujer, aparecerá en el documento elemento varón(como en el gráfico) o el elemento hembra.
   
   • Los valores del atributo dia están comprendidos entre 1 y 31. Definir el tipo tipoDia para ello. Los valores del atributo mes son de tipo cadena y tienen que coincidir con uno de los meses del año. Definir el tipo tipoMes para ello.
   
   • Los valores del atributo anyo están comprendidos entre 1900 y 2011. Definir el tipo tipoAnyo para ello.
   
   
   • Los valores de nombre, calle, población y provincia tienen como máximo 50 caracteres. Definir el tipo tipoNombre para ello.
   
   • El código postal es un entero de 5 dígitos. Definir el tipo tipoCodPostal para ello
    
   ![68747470733a2f2f36643031333166392d612d36326362336131612d732d73697465732e676f6f676c6567726f7570732e636f6d2f736974652f746f646f786d6c6474642f656a6572636963696f732f656e756e636961646f732f33352d656a6572636963696f732d786](https://user-images.githubusercontent.com/61906112/139713733-a8316ec1-6144-4552-8da7-57932f96316b.jpg)


```
<?xml version="1.0" encoding="ISO-8859-1"?>
<xsd:schema xmlns:xsd="http://www.w3.org/2001/xmlschema">

<xsd:element name="personas">
	<xsd:complexType>
		<xsd:sequence>
		<xsd:element ref="persona" maxOccurs="unbounded"/>
		</xsd:sequence>
	</xsd:complexType>
</xsd:element>

<xsd:element name="persona">
	<xsd:complexType>
		<xsd:sequence>
			<xsd:element ref="nombre"/>
			<xsd:element ref="nacimiento"/>
			<xsd:element ref="direccion"/>
			<xsd:choice><xsd:element ref="varon"/><xsd:element ref="hembra"/></xsd:choice>
		</xsd:sequence>
	</xsd:complexType>
</xsd:element>

<xsd:element name="nombre" type="tipoNombre"/>
<xsd:element name="apellidos" type="tipoNombre"/>
<xsd:element name="calle" type="tipoDireccion"/>
<xsd:element name="poblacion" type="tipoDireccion"/>
<xsd:element name="provincia" type="tipoDireccion"/>

<xsd:element name="nacimiento">
	<xsd:complexType>
		<xsd:simpleContent>
			<xsd:extension base="string">
				<xsd:attribute name="dia" type="tipoDia"/>
				<xsd:attribute name="mes" type="tipoMes"/>
				<xsd:attribute name="anyo" type="tipoAnyo"/>
			</xsd:extension>
		</xsd:simpleContent>		
	</xsd:complexType>

<xsd:element name="direccion">
	<xsd:complexType>
		<xsd:sequence>
			<xsd:element ref="calle"/>
			<xsd:element ref="poblacion"/>
			<xsd:element ref="provincia"/>
			<xsd:element ref="cpostal"/>
		</xsd:sequence>
	</xsd:complexType>
</xsd:element>

<xsd:element name="varon"/>
<xsd:element name="hembra"/>
<xsd:element name="cpostal" type="tipoCPostal"/>

<!-- definiendo los tipos -->

<xsd:simpleType name="tipoNombre">
	<xsd:restriction base="xsd:string">
		<xsd:maxLength value="50"/>
	</xsd:restriction>
</xsd:simpleType>

<xsd:simpleType name="tipoDia">
	<xds:restriction base="xsd:integer">
		<xsd:minInclusive value="1"/>
		<xsd:maxInclusive value="31"/>
	</xds:restriction>
</xsd:simpleType>

<xsd:simpleType name="tipoMes">
	<xsd:restriction base="xsd:string">
		<xsd:enumeration value="enero"/>
			<xsd:enumeration value="febrero"/>
			<xsd:enumeration value="marzo"/>
			<xsd:enumeration value="abril"/>
			<xsd:enumeration value="mayo"/>
			<xsd:enumeration value="junio"/>
			<xsd:enumeration value="julio"/>
			<xsd:enumeration value="agosto"/>
			<xsd:enumeration value="septiembre"/>
			<xsd:enumeration value="octubre"/>
			<xsd:enumeration value="noviembre"/>
			<xsd:enumeration value="diciembre"/>
		</xsd:restriction>
</xsd:simpleType>

<xsd:simpleType name="tipoAnyo">
	<xsd:restriction base="xsd:integer">
		<xsd:minInclusive value="1900"/>
		<xsd:maxInclusive value="2011"/>
	</xsd:restriction>
</xsd:simpleType>

<xsd:simpleType name="tipoCPostal">
	<xsd:restriction base="integer">
		<xsd:totalDigits value="5"/>
	</xsd:restriction>
</xsd:simpleType>
</xsd:schema>



<personas>
<persona>
	<nombre> Juan Pardo </nombre>
	<nacimiento dia="10" mes="abril" anyo="1982">  </nacimiento>
	<direccion> 
			<calle> caoba, 1 </calle>
			<poblacion> Madrid </poblacion>
			<provincia> Madrid </provincia>
			<cpostal> 28005 </cpostal>
	</direccion>
	<varon> si </varon>
</persona>
<persona>
	<nombre> María López </nombre>
	<nacimiento dia="" mes="" anyo="">  </nacimiento>
	<direccion> 
			<calle> Roncato,1,Illescas </calle>
			<poblacion> Toledo </poblacion>
			<provincia> Madrid </provincia>
			<cpostal> 45200 </cpostal>
	</direccion>
	<direccion>
		<calle> Paseo de la Esperanza,15,1ºA </calle>
		<poblacion> Madrid </poblacion>
		<provincia> Madrid </provincia>
		<cpostal> 28005 </cpostal>
	</direccion>
	</persona>
	<hembra>  </hembra>
	</persona>
</personas>
```
