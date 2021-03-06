---

copyright:
  years: 2014, 2018
lastupdated: "2018-4-20"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# {{site.data.keyword.containerlong_notm}} Referencia de la CLI
{: #cs_cli_reference}

Consulte estos mandatos para crear y gestionar clústeres de Kubernetes en {{site.data.keyword.containerlong}}.
{:shortdesc}

Para instalar el plugin de CLI, consulte [Instalación de la CLI](cs_cli_install.html#cs_cli_install_steps).

¿Está buscando mandatos `bx cr`? Revise la guía de [consulta de la CLI de {{site.data.keyword.registryshort_notm}}](/docs/cli/plugins/registry/index.html). ¿Está buscando mandatos `kubectl`? Consulte la [documentación de Kubernetes ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands).
{:tip}

## Mandatos bx cs
{: #cs_commands}

**Sugerencia:** Para ver la versión del plug-in de {{site.data.keyword.containershort_notm}}, consulte el siguiente mandato.

```
bx plugin list
```
{: pre}



<table summary="Mandatos de API">
<col width="25%">
<col width="25%">
<col width="25%">
 <thead>
    <th colspan=4>Mandatos de API</th>
 </thead>
 <tbody>
  <tr>
    <td>[bx cs api-key-info](#cs_api_key_info)</td>
    <td>[bx cs api-key-reset](#cs_api_key_reset)</td>
    <td>[bx cs apiserver-config-get](#cs_apiserver_config_get)</td>
    <td>[bx cs apiserver-config-set](#cs_apiserver_config_set)</td>
  </tr>
  <tr>
    <td>[bx cs apiserver-config-unset](#cs_apiserver_config_unset)</td>
    <td>[bx cs apiserver-refresh](#cs_apiserver_refresh)</td>
    <td></td>
    <td></td>
 </tr>
</tbody>
</table>

<br>

<table summary="Mandatos de uso del plug-in de CLI">
<col width="25%">
<col width="25%">
<col width="25%">
 <thead>
    <th colspan=4>Mandatos de uso del plug-in de CLI</th>
 </thead>
 <tbody>
  <tr>
    <td>[bx cs help](#cs_help)</td>
    <td>[bx cs init](#cs_init)</td>
    <td>[bx cs messages](#cs_messages)</td>
    <td></td>
  </tr>
</tbody>
</table>

<br>

<table summary="Mandatos de clúster: Gestión">
<col width="25%">
<col width="25%">
<col width="25%">
 <thead>
    <th colspan=4>Mandatos de clúster: Gestión</th>
 </thead>
 <tbody>
  <tr>
    <td>[bx cs cluster-config](#cs_cluster_config)</td>
    <td>[bx cs cluster-create](#cs_cluster_create)</td>
    <td>[bx cs cluster-feature-enable](#cs_cluster_feature_enable)</td>
    <td>[bx cs cluster-get](#cs_cluster_get)</td>
  </tr>
  <tr>
    <td>[bx cs cluster-rm](#cs_cluster_rm)</td>
    <td>[bx cs cluster-update](#cs_cluster_update)</td>
    <td>[bx cs clusters](#cs_clusters)</td>
    <td>[bx cs kube-versions](#cs_kube_versions)</td>
  </tr>
</tbody>
</table>

<br>

<table summary="Mandatos de clúster: Servicios e integraciones">
<col width="25%">
<col width="25%">
<col width="25%">
 <thead>
    <th colspan=4>Mandatos de clúster: Servicios e integraciones</th>
 </thead>
 <tbody>
  <tr>
    <td>[bx cs cluster-service-bind](#cs_cluster_service_bind)</td>
    <td>[bx cs cluster-service-unbind](#cs_cluster_service_unbind)</td>
    <td>[bx cs cluster-services](#cs_cluster_services)</td>
    <td>[bx cs webhook-create](#cs_webhook_create)</td>
  </tr>
</tbody>
</table>

</br>

<table summary="Mandatos de clúster: Subredes">
<col width="25%">
<col width="25%">
<col width="25%">
 <thead>
    <th colspan=4>Mandatos de clúster: Subredes</th>
 </thead>
 <tbody>
  <tr>
    <td>[bx cs cluster-subnet-add](#cs_cluster_subnet_add)</td>
    <td>[bx cs cluster-subnet-create](#cs_cluster_subnet_create)</td>
    <td>[bx cs cluster-user-subnet-add](#cs_cluster_user_subnet_add)</td>
    <td>[bx cs cluster-user-subnet-rm](#cs_cluster_user_subnet_rm)</td>
  </tr>
  <tr>
    <td>[bx cs subnets](#cs_subnets)</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
</tbody>
</table>

</br>

<table summary="Mandatos de infraestructura">
<col width="25%">
<col width="25%">
<col width="25%">
 <thead>
    <th colspan=4>Mandatos de infraestructura</th>
 </thead>
 <tbody>
  <tr>
    <td>[bx cs credentials-set](#cs_credentials_set)</td>
    <td>[bx cs credentials-unset](#cs_credentials_unset)</td>
    <td>[bx cs machine-types](#cs_machine_types)</td>
    <td>[bx cs vlans](#cs_vlans)</td>
  </tr>
</tbody>
</table>

</br>

<table summary="Mandatos de equilibrador de carga de aplicación (ALB) de Ingress">
<col width = 25%>
<col width = 25%>
<col width = 25%>
  <thead>
    <tr>
      <th colspan=4>Mandatos del equilibrador de carga de aplicación (ALB) de Ingress</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>[bx cs alb-cert-deploy](#cs_alb_cert_deploy)</td>
      <td>[bx cs alb-cert-get](#cs_alb_cert_get)</td>
      <td>[bx cs alb-cert-rm](#cs_alb_cert_rm)</td>
      <td>[bx cs alb-certs](#cs_alb_certs)</td>
    </tr>
    <tr>
      <td>[bx cs alb-configure](#cs_alb_configure)</td>
      <td>[bx cs alb-get](#cs_alb_get)</td>
      <td>[bx cs alb-types](#cs_alb_types)</td>
      <td>[bx cs albs](#cs_albs)</td>
    </tr>
  </tbody>
</table>

</br>

<table summary="Mandatos de registro">
<col width = 25%>
<col width = 25%>
<col width = 25%>
  <thead>
    <tr>
      <th colspan=4>Mandatos de registro</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>[bx cs logging-config-create](#cs_logging_create)</td>
      <td>[bx cs logging-config-get](#cs_logging_get)</td>
      <td>[bx cs logging-config-refresh](#cs_logging_refresh)</td>
      <td>[bx cs logging-config-rm](#cs_logging_rm)</td>
    </tr>
    <tr>
      <td>[bx cs logging-config-update](#cs_logging_update)</td>
      <td>[bx cs logging-filter-create](#cs_log_filter_create)</td>
      <td>[bx cs logging-filter-update](#cs_log_filter_update)</td>
      <td>[bx cs logging-filter-get](#cs_log_filter_view)</td>
    </tr>
    <tr>
      <td>[bx cs logging-filter-rm](#cs_log_filter_delete)</td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

</br>

<table summary="Mandatos de región">
<col width="25%">
<col width="25%">
<col width="25%">
 <thead>
    <th colspan=4>Mandatos de región</th>
 </thead>
 <tbody>
  <tr>
    <td>[bx cs locations](#cs_datacenters)</td>
    <td>[bx cs region](#cs_region)</td>
    <td>[bx cs region-set](#cs_region-set)</td>
    <td>[bx cs regions](#cs_regions)</td>
  </tr>
</tbody>
</table>

</br>

<table summary="Mandatos de nodo trabajador">
<col width="25%">
<col width="25%">
<col width="25%">
 <thead>
    <th colspan=4>Mandatos de nodo trabajador</th>
 </thead>
 <tbody>
    <tr>
      <td>[bx cs worker-add](#cs_worker_add)</td>
      <td>[bx cs worker-get](#cs_worker_get)</td>
      <td>[bx cs worker-reboot](#cs_worker_reboot)</td>
      <td>[bx cs worker-reload](#cs_worker_reload)</td></staging>
    </tr>
    <tr>
      <td>[bx cs worker-rm](#cs_worker_rm)</td>
      <td>[bx cs worker-update](#cs_worker_update)</td>
      <td>[bx cs workers](#cs_workers)</td>
      <td></td>
    </tr>
  </tbody>
</table>

## Mandatos de API
{: #api_commands}

### bx cs api-key-info CLUSTER
{: #cs_api_key_info}

Visualice el nombre y la dirección de correo electrónico del propietario de la clave de API IAM en una región de {{site.data.keyword.containershort_notm}}.

La clave de API de Identity and Access Management (IAM) se establece automáticamente para una región cuando se realiza la primera acción que requiere la política de acceso de administrador de {{site.data.keyword.containershort_notm}}. Por ejemplo, uno de los usuarios administrativos crea el primer clúster en la región `us-south`. De ese modo, la clave de API IAM para este usuario se almacena en la cuenta para esta región. La clave de API se utiliza para pedir recursos en la infraestructura de IBM Cloud (SoftLayer), como nodos trabajadores nuevos o VLAN.

Cuando un usuario distinto realiza una acción en esta región que requiere interacción con el portafolio de infraestructura de IBM Cloud (SoftLayer), como crear un nuevo clúster o recargar un nodo trabajador, la clave de API almacenada se utiliza para determinar si existen suficientes permisos para realizar esa acción. Para asegurarse de que las acciones relacionadas con la infraestructura en el clúster se realicen correctamente, puede asignar a los usuarios administradores de {{site.data.keyword.containershort_notm}} la política de acceso a infraestructura **Superusuario**. Para obtener más información, consulte [Gestión de acceso de usuario](cs_users.html#infra_access).

Si necesita actualizar la clave de API que hay almacenada para una región, puede hacerlo mediante la ejecución del mandato [bx cs api-key-reset](#cs_api_key_reset). Este mandato requiere la política de acceso de administrador de {{site.data.keyword.containershort_notm}} y almacena la clave de API del usuario que ejecuta este mandato en la cuenta.

**Nota:** La clave de API que se devuelve en este mandato no puede utilizarse si las credenciales de infraestructura de IBM Cloud (SoftLayer) se han establecido manualmente mediante el mandato [bx cs credentials-set](#cs_credentials_set).

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs api-key-info my_cluster
  ```
  {: pre}


### bx cs api-key-reset
{: #cs_api_key_reset}

Sustituya la clave de API IAM actual en una región de {{site.data.keyword.containershort_notm}}.

Este mandato requiere la política de acceso de administrador de {{site.data.keyword.containershort_notm}} y almacena la clave de API del usuario que ejecuta este mandato en la cuenta. La clave de API IAM es necesaria para pedir infraestructura del portfolio de infraestructura de IBM Cloud (SoftLayer). Una vez almacenada, la clave de API se utiliza para cada acción en una región que requiere permisos de infraestructura, con independencia del usuario que ejecute este mandato. Para obtener más información sobre cómo funcionan las claves de API IAM, consulte el [mandato `bx cs api-key-info`](#cs_api_key_info).

**Importante:** Antes de utilizar este mandato, asegúrese de que el usuario que lo ejecuta tiene los [permisos de infraestructura de IBM Cloud (SoftLayer) e {{site.data.keyword.containershort_notm}}](cs_users.html#users) necesarios.

**Ejemplo**:

  ```
  bx cs api-key-reset
  ```
  {: pre}


### bx cs apiserver-config-get
{: #cs_apiserver_config_get}

Obtener información sobre una opción para la configuración de servidor de API de Kubernetes de un clúster. Este mandato debe combinarse con uno de los siguientes submandatos para la opción de configuración de la que desea información.

#### bx cs apiserver-config-get audit-webhook CLUSTER
{: #cs_apiserver_api_webhook_get}

Ver el URL para el servicio de registro remoto al que está enviando registros de auditoría de servidor de API. El URL se ha especificado al crear el programa de fondo del webhook para la configuración del servidor de API.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs apiserver-config-get audit-webhook my_cluster
  ```
  {: pre}

### bx cs apiserver-config-set
{: #cs_apiserver_config_set}

Establecer una opción para la configuración de servidor de API de Kubernetes de un clúster. Este mandato debe combinarse con uno de los siguientes submandatos para la opción de configuración que desea establecer.

#### bx cs apiserver-config-set audit-webhook CLUSTER [--remoteServer SERVER_URL_OR_IP][--caCert CA_CERT_PATH] [--clientCert CLIENT_CERT_PATH][--clientKey CLIENT_KEY_PATH]
{: #cs_apiserver_api_webhook_set}

Establecer el programa de fondo del webhook para la configuración del servidor de API. El programa de fondo del webhook reenvía registros de auditoría del servidor de API a un servidor remoto. Se crea una configuración de webhook basándose en la información que proporciona en los distintivos de este mandato. Si no proporciona ninguna información en los distintivos, se utiliza una configuración de webhook predeterminada.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code>--remoteServer <em>SERVER_URL</em></code></dt>
   <dd>La dirección IP o el URL del servicio de registro remoto al que desea enviar registros de auditoría. Si proporciona un URL de servidor no seguro, se ignoran los certificados. Este valor es opcional.</dd>

   <dt><code>--caCert <em>CA_CERT_PATH</em></code></dt>
   <dd>La vía de acceso de archivo del certificado de CA que se utiliza para verificar el servicio de registro remoto. Este valor es opcional.</dd>

   <dt><code>--clientCert <em>CLIENT_CERT_PATH</em></code></dt>
   <dd>La vía de acceso de archivo del certificado de cliente que se utiliza para autenticarse en el servicio de registro remoto. Este valor es opcional.</dd>

   <dt><code>--clientKey <em> CLIENT_KEY_PATH</em></code></dt>
   <dd>La vía de acceso de archivo de la clave de cliente correspondiente que se utiliza para conectarse al servicio de registro remoto. Este valor es opcional.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs apiserver-config-set audit-webhook my_cluster --remoteServer https://audit.example.com/audit --caCert /mnt/etc/kubernetes/apiserver-audit/ca.pem --clientCert /mnt/etc/kubernetes/apiserver-audit/cert.pem --clientKey /mnt/etc/kubernetes/apiserver-audit/key.pem
  ```
  {: pre}


### bx cs apiserver-config-unset
{: #cs_apiserver_config_unset}

Inhabilitar una opción para la configuración de servidor de API de Kubernetes de un clúster. Este mandato debe combinarse con uno de los siguientes submandatos para la opción de configuración que desea eliminar.

#### bx cs apiserver-config-unset audit-webhook CLUSTER
{: #cs_apiserver_api_webhook_unset}

Inhabilitar la configuración del programa de fondo del webhook para el servidor de API del clúster. Al inhabilitar el programa de fondo del webhook, se detiene el reenvío registros de auditoría del servidor de API a un servidor remoto.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs apiserver-config-unset audit-webhook my_cluster
  ```
  {: pre}

### bx cs apiserver-refresh CLUSTER
{: #cs_apiserver_refresh}

Reinicie el maestro de Kubernetes en el clúster para aplicar los cambios a la configuración del servidor de API.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs apiserver-refresh my_cluster
  ```
  {: pre}


<br />


## Mandatos de uso del plug-in de CLI
{: #cli_plug-in_commands}

### bx cs help
{: #cs_help}

Ver una lista de mandatos y parámetros admitidos.

<strong>Opciones del mandato</strong>:

   Ninguno

**Ejemplo**:

  ```
  bx cs help
  ```
  {: pre}


### bx cs init [--host HOST]
{: #cs_init}

Inicialice el plug-in de {{site.data.keyword.containershort_notm}} o especifique la región donde desea crear o acceder a clústeres de Kubernetes.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code>--host <em>HOST</em></code></dt>
   <dd>El punto final de API de {{site.data.keyword.containershort_notm}} que se va a utilizar.  Este valor es opcional. [Ver valores disponibles de punto final de API.](cs_regions.html#container_regions)</dd>
   </dl>

**Ejemplo**:


```
bx cs init --host https://uk-south.containers.bluemix.net
```
{: pre}


### bx cs messages
{: #cs_messages}

Ver los mensajes actuales para el usuario IBMid.

**Ejemplo**:

```
bx cs messages
```
{: pre}


<br />


## Mandatos de clúster: Gestión
{: #cluster_mgmt_commands}


### bx cs cluster-config CLUSTER [--admin][--export]
{: #cs_cluster_config}

Después de iniciar una sesión, descargue certificados y datos de configuración de Kubernetes para conectar el clúster y ejecutar mandatos `kubectl`. Los archivos se descargan en `user_home_directory/.bluemix/plugins/container-service/clusters/<cluster_name>`.

**Opciones del mandato**:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code>--admin</code></dt>
   <dd>Descargar los certificados TLS y archivos de permisos para el rol de superusuario. Puede utilizar los certificados para automatizar las tareas de un clúster sin tener que volverse a autenticar. Los archivos se descargan en `<user_home_directory>/.bluemix/plugins/container-service/clusters/<cluster_name>-admin`. Este valor es opcional.</dd>

   <dt><code>--export</code></dt>
   <dd>Descargar los datos de configuración y certificados de Kubernetes sin ningún mensaje aparte del mandato de exportación. Como no se muestran mensajes, puede utilizar este distintivo cuando cree scripts automatizados. Este valor es opcional.</dd>
   </dl>

**Ejemplo**:

```
bx cs cluster-config my_cluster
```
{: pre}


### bx cs cluster-create [--file FILE_LOCATION][--hardware HARDWARE] --location LOCATION --machine-type MACHINE_TYPE --name NAME [--kube-version MAJOR.MINOR.PATCH][--no-subnet] [--private-vlan PRIVATE_VLAN][--public-vlan PUBLIC_VLAN] [--workers WORKER][--disable-disk-encrypt] [--trusted]
{: #cs_cluster_create}

Cree un clúster en la organización. Para los clústeres gratuitos, especifique el nombre de clúster; todo lo demás se establece en un valor predeterminado. Un clúster gratuito se suprime automáticamente después de 21 días. Puede disponer de un clúster gratuito al mismo tiempo. Para aprovechar todas las funciones de Kubernetes, cree un clúster estándar.

<strong>Opciones del mandato</strong>

<dl>
<dt><code>--file <em>FILE_LOCATION</em></code></dt>

<dd>La vía de acceso al archivo YAML para crear el clúster estándar. En lugar de definir las características de su clúster mediante las opciones que se proporcionan en este mandato, puede utilizar un archivo YAML.  Este valor es opcional para clústeres estándares y no está disponible para clústeres gratuitos.

<p><strong>Nota:</strong> Si especifica la misma opción en el mandato y como parámetro en el archivo YAML, el valor en el mandato prevalece sobre el valor del archivo YAML. Por ejemplo, supongamos que define una ubicación en el archivo YAML y utiliza la opción <code>--location</code> en el mandato; el valor que especifique en la opción del mandato prevalece sobre el valor del archivo YAML.

<pre class="codeblock">
<code>name: <em>&lt;cluster_name&gt;</em>
location: <em>&lt;location&gt;</em>
no-subnet: <em>&lt;no-subnet&gt;</em>
machine-type: <em>&lt;machine_type&gt;</em>
private-vlan: <em>&lt;private_VLAN&gt;</em>
public-vlan: <em>&lt;public_VLAN&gt;</em>
hardware: <em>&lt;shared_or_dedicated&gt;</em>
workerNum: <em>&lt;number_workers&gt;</em>
kube-version: <em>&lt;kube-version&gt;</em>
diskEncryption: <em>false</em>
trusted: <em>true</em>
</code></pre>


<table>
    <caption>Tabla. Visión general de los componentes del archivo YAML</caption>
    <thead>
    <th colspan=2><img src="images/idea.png" alt="Icono Idea"/> Visión general de los componentes del archivo YAML</th>
    </thead>
    <tbody>
    <tr>
    <td><code><em>name</em></code></td>
    <td>Sustituya <code><em>&lt;cluster_name&gt;</em></code> por el nombre del clúster. El nombre debe empezar por una letra, puede contener letras, números, guiones (-) y debe tener 35 caracteres como máximo. Tenga en cuenta que el nombre del clúster y la región en la que el clúster se despliega forman el nombre de dominio completo para el subdominio de Ingress. Para garantizar que el subdominio de Ingress es exclusivo dentro de una región, el nombre del clúster podría ser truncado y añadírsele un valor aleatorio dentro del nombre de dominio de Ingress. </td>
    </tr>
    <tr>
    <td><code><em>location</em></code></td>
    <td>Sustituya <code><em>&lt;location&gt;</em></code> por la ubicación en la que desea crear el clúster. Las ubicaciones disponibles dependen de la región en la que ha iniciado la sesión. Para ver una lista de las ubicaciones disponibles, ejecute <code>cs bx ubicaciones</code>. </td>
     </tr>
     <tr>
     <td><code><em>no-subnet</em></code></td>
     <td>De forma predeterminada, se crea una subred portátil pública y una privada en la VLAN asociada con el clúster. Sustituya <code><em>&lt;no-subnet&gt;</em></code> por <code><em>true</em></code> para evitar crear subredes con el clúster. Puede [crear](#cs_cluster_subnet_create) o [añadir](#cs_cluster_subnet_add) subredes a un clúster más adelante.</td>
      </tr>
     <tr>
     <td><code><em>machine-type</em></code></td>
     <td>Sustituya <code><em>&lt;machine_type&gt;</em></code> por el tipo de máquina en el que desea desplegar los nodos trabajadores. Puede desplegar los nodos trabajadores como máquinas virtuales en hardware dedicado o compartido, o como máquinas físicas en servidores nativos. Los tipos de máquinas físicas y virtuales varían según la ubicación en la que se despliega el clúster. Para obtener más información, consulte la documentación del [mandato](cs_cli_reference.html#cs_machine_types) `bx cs machine-type`.</td>
     </tr>
     <tr>
     <td><code><em>private-vlan</em></code></td>
     <td>Sustituya <code><em>&lt;private_VLAN&gt;</em></code> por el ID de la VLAN privada que desea utilizar para sus nodos trabajadores. Para ver una lista de las VLAN disponibles, ejecute <code>bx cs vlans <em>&lt;location&gt;</em></code> y busque direccionadores de VLAN que empiecen por <code>bcr</code> ("back-end router", direccionador de fondo).</td>
     </tr>
     <tr>
     <td><code><em>public-vlan</em></code></td>
     <td>Sustituya <code><em>&lt;public_VLAN&gt;</em></code> por el ID de la VLAN pública que desea utilizar para sus nodos trabajadores. Para ver una lista de las VLAN disponibles, ejecute <code>bx cs vlans <em>&lt;location&gt;</em></code> y busque direccionadores de VLAN que empiecen por <code>fcr</code> ("front-end router", direccionador frontal).</td>
     </tr>
     <tr>
     <td><code><em>hardware</em></code></td>
     <td>Para tipos de máquina virtual: El nivel de aislamiento del hardware del nodo trabajador. Utilice el valor dedicated si desea tener recursos físicos disponibles dedicados solo a usted, o el valor shared para permitir que los recursos físicos se compartan con otros clientes de IBM. El valor predeterminado es <code>shared</code>.</td>
     </tr>
     <tr>
     <td><code><em>workerNum</em></code></td>
     <td>Sustituya <code><em>&lt;number_workers&gt;</em></code> por el número de nodos trabajadores que desea desplegar.</td>
     </tr>
     <tr>
      <td><code><em>kube-version</em></code></td>
      <td>La versión Kubernetes del nodo maestro del clúster. Este valor es opcional. Cuando no se especifica la versión, el clúster se crea con el valor predeterminado de las versiones de Kubernetes soportadas. Para ver todas las versiones disponibles, ejecute <code>bx cs kube-versions</code>. </td></tr>
      <tr>
      <td><code>diskEncryption: <em>false</em></code></td>
      <td>Los nodos trabajadores tienen cifrado de disco de forma predeterminada; [más información](cs_secure.html#worker). Para inhabilitar el cifrado, incluya esta opción y establezca el valor en <code>false</code>.</td></tr>
      <tr>
      <td><code>trusted: <em>true</em></code></td>
      <td>**Solo nativos**: Habilite [Trusted Compute](cs_secure.html#trusted_compute) para verificar que los nodos trabajadores nativos no se manipulan de forma indebida. Si no habilita la confianza durante la creación del clúster pero desea hacerlo posteriormente, puede utilizar el [mandato](cs_cli_reference.html#cs_cluster_feature_enable) `bx cs feature-enable`. Una vez que habilita la confianza, no puede inhabilitarla posteriormente.</td></tr>
     </tbody></table>
    </p></dd>

<dt><code>--hardware <em>HARDWARE</em></code></dt>
<dd>El nivel de aislamiento del hardware del nodo trabajador. Utilice el valor dedicated para tener recursos físicos disponibles dedicados solo a usted, o shared para permitir que los recursos físicos se compartan con otros clientes de IBM. El valor predeterminado es shared.  Este valor es opcional para clústeres estándares y no está disponible para clústeres gratuitos.</dd>

<dt><code>--location <em>LOCATION</em></code></dt>
<dd>La ubicación en la que desea crear el clúster. Las ubicaciones disponibles dependen de la región de {{site.data.keyword.Bluemix_notm}} en la que haya iniciado la sesión. Para obtener el mejor rendimiento, seleccione la región que esté físicamente más cercana a su ubicación.  Este valor es obligatorio para clústeres estándares y opcional para clústeres gratuitos.

<p>Consulte [ubicaciones disponibles](cs_regions.html#locations).
</p>

<p><strong>Nota:</strong> Si selecciona una ubicación que se encuentra fuera de su país, tenga en cuenta que es posible que se requiera autorización legal para poder almacenar datos físicamente en un país extranjero.</p>
</dd>

<dt><code>--machine-type <em>MACHINE_TYPE</em></code></dt>
<dd>Elija un tipo de máquina. Puede desplegar los nodos trabajadores como máquinas virtuales en hardware dedicado o compartido, o como máquinas físicas en servidores nativos. Los tipos de máquinas físicas y virtuales varían según la ubicación en la que se despliega el clúster. Para obtener más información, consulte la documentación del [mandato](cs_cli_reference.html#cs_machine_types) `bx cs machine-types`. Este valor es obligatorio para clústeres estándares y no está disponible para clústeres gratuitos.</dd>

<dt><code>--name <em>NAME</em></code></dt>
<dd>El nombre del clúster.  Este valor es obligatorio. El nombre debe empezar por una letra, puede contener letras, números, guiones (-) y debe tener 35 caracteres como máximo. Tenga en cuenta que el nombre del clúster y la región en la que el clúster se despliega forman el nombre de dominio completo para el subdominio de Ingress. Para garantizar que el subdominio de Ingress es exclusivo dentro de una región, el nombre del clúster podría ser truncado y añadírsele un valor aleatorio dentro del nombre de dominio de Ingress. </dd>

<dt><code>--kube-version <em>MAJOR.MINOR.PATCH</em></code></dt>
<dd>La versión Kubernetes del nodo maestro del clúster. Este valor es opcional. Cuando no se especifica la versión, el clúster se crea con el valor predeterminado de las versiones de Kubernetes soportadas. Para ver todas las versiones disponibles, ejecute <code>bx cs kube-versions</code>. </dd>

<dt><code>--no-subnet</code></dt>
<dd>De forma predeterminada, se crea una subred portátil pública y una privada en la VLAN asociada con el clúster. Incluya el distintivo <code>--no-subnet</code> para evitar crear subredes con el clúster. Puede [crear](#cs_cluster_subnet_create) o [añadir](#cs_cluster_subnet_add) subredes a un clúster más adelante.</dd>

<dt><code>--private-vlan <em>PRIVATE_VLAN</em></code></dt>
<dd>

<ul>
<li>Este parámetro no está disponible para clústeres gratuitos.</li>
<li>Si este es el primer clúster estándar que crea en esta ubicación, no incluya este distintivo. Al crear clústeres se crea automáticamente una VLAN privada.</li>
<li>Si previamente ha creado un clúster estándar en esta ubicación o una VLAN privada en la infraestructura de IBM Cloud (SoftLayer), debe especificar la VLAN privada.

<p><strong>Nota:</strong> {[matching_VLANs]}</p></li>
</ul>

<p>Para saber si ya tiene una VLAN privada para una ubicación específica o para encontrar el nombre de una VLAN privada existente, ejecute <code>bx cs vlans <em>&lt;location&gt;</em></code>.</p></dd>

<dt><code>--public-vlan <em>PUBLIC_VLAN</em></code></dt>
<dd>
<ul>
<li>Este parámetro no está disponible para clústeres gratuitos.</li>
<li>Si este es el primer clúster estándar que crea en esta ubicación, no utilice este distintivo. Al crear el clúster se crea automáticamente una VLAN pública.</li>
<li>Si previamente ha creado un clúster estándar en esta ubicación o una VLAN pública en la infraestructura de IBM Cloud (SoftLayer), debe especificar la VLAN pública.

<p><strong>Nota:</strong> {[matching_VLANs]}</p></li>
</ul>

<p>Para saber si ya tiene una VLAN pública para una ubicación específica o para encontrar el nombre de una VLAN pública existente, ejecute <code>bx cs vlans <em>&lt;location&gt;</em></code>.</p></dd>

<dt><code>--workers WORKER</code></dt>
<dd>El número de nodos trabajadores que desea desplegar en el clúster. Si no especifica esta opción, se crea un clúster con 1 nodo trabajador. Este valor es opcional para clústeres estándares y no está disponible para clústeres gratuitos.

<p><strong>Nota:</strong> A cada nodo trabajador se la asigna un ID exclusivo y un nombre de dominio que no se debe cambiar de forma manual después de haber creado el clúster. Si se cambia el nombre de dominio o el ID se impide que el maestro de Kubernetes gestione el clúster.</p></dd>

<dt><code>--disable-disk-encrypt</code></dt>
<dd>Los nodos trabajadores tienen cifrado de disco de forma predeterminada; [más información](cs_secure.html#worker). Para inhabilitar el cifrado, incluya esta opción.</dd>

<dt><code>--trusted</code></dt>
<dd><p>**Solo nativos**: Habilite [Trusted Compute](cs_secure.html#trusted_compute) para verificar que los nodos trabajadores nativos no se manipulan de forma indebida. Si no habilita la confianza durante la creación del clúster pero desea hacerlo posteriormente, puede utilizar el [mandato](cs_cli_reference.html#cs_cluster_feature_enable) `bx cs feature-enable`. Una vez que habilita la confianza, no puede inhabilitarla posteriormente.</p>
<p>Para comprobar si el tipo de máquina nativa es compatible con la confianza, compruebe el campo `Trustable` en la salida del [mandato](#cs_machine_types) `bx cs machine-types <location>`. Para verificar que un clúster tiene habilitada la confianza, consulte el campo **Trust ready** en la salida del [mandato](#cs_cluster_get) `bx cs cluster-get`. Para verificar que un nodo trabajador nativo tiene habilitada la confianza, consulte el campo **Trust** en la salida del [mandato](#cs_worker_get) `bx cs worker-get`.</p></dd>
</dl>

**Ejemplos**:

  

  Ejemplo para un clúster estándar:
  {: #example_cluster_create}

  ```
  bx cs cluster-create --location dal10 --public-vlan my_public_VLAN_ID --private-vlan my_private_VLAN_ID --machine-type u2c.2x4 --name my_cluster --hardware shared --workers 2
  ```
  {: pre}

  Ejemplo para un clúster gratuito:

  ```
  bx cs cluster-create --name my_cluster
  ```
  {: pre}

  Ejemplo para un entorno {{site.data.keyword.Bluemix_dedicated_notm}}:

  ```
  bx cs cluster-create --machine-type machine-type --workers number --name cluster_name
  ```
  {: pre}

### bx cs cluster-feature-enable CLUSTER [--trusted]
{: #cs_cluster_feature_enable}

Habilite una característica en un clúster existente.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code><em>--trusted</em></code></dt>
   <dd><p>Incluya el distintivo para habilitar [Trusted Compute](cs_secure.html#trusted_compute) en todos los nodos trabajadores nativos soportados que están en el clúster. Después de habilitar la confianza, no puede inhabilitarla posteriormente para el clúster.</p>
   <p>Para comprobar si el tipo de máquina nativa es compatible con la confianza, compruebe el campo **Trustable** en la salida del [mandato](#cs_machine_types) `bx cs machine-types <location>`. Para verificar que un clúster tiene habilitada la confianza, consulte el campo **Trust ready** en la salida del [mandato](#cs_cluster_get) `bx cs cluster-get`. Para verificar que un nodo trabajador nativo tiene habilitada la confianza, consulte el campo **Trust** en la salida del [mandato](#cs_worker_get) `bx cs worker-get`.</p></dd>
   </dl>

**Mandato de ejemplo**:

  ```
  bx cs cluster-feature-enable my_cluster --trusted=true
  ```
  {: pre}

### bx cs cluster-get CLUSTER [--showResources]
{: #cs_cluster_get}

Ver información sobre un clúster de la organización.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code><em>--showResources</em></code></dt>
   <dd>Muestre más recursos del clúster, como complementos, VLAN, subredes y almacenamiento.</dd>
   </dl>

**Mandato de ejemplo**:

  ```
  bx cs cluster-get my_cluster --showResources
  ```
  {: pre}

**Salida de ejemplo**:

  ```
  Name:        my_cluster
  ID:          abc1234567
  State:       normal
  Trust ready: false
  Created:     2018-01-01T17:19:28+0000
  Location:    dal10
  Master URL:  https://169.xx.xxx.xxx:xxxxx
  Ingress subdomain: my_cluster.us-south.containers.mybluemix.net
  Ingress secret:    my_cluster
  Workers:     3
  Version:     1.7.16_1511* (1.8.11_1509 latest)
  Owner Email: name@example.com
  Monitoring dashboard: https://metrics.ng.bluemix.net/app/#/grafana4/dashboard/db/link

  Addons
  Name                   Enabled
  customer-storage-pod   true
  basic-ingress-v2       true
  storage-watcher-pod    true

  Subnet VLANs
  VLAN ID   Subnet CIDR         Public   User-managed
  2234947   10.xxx.xx.xxx/29    false    false
  2234945   169.xx.xxx.xxx/29  true    false

  ```
  {: screen}

### bx cs cluster-rm [-f] CLUSTER
{: #cs_cluster_rm}

Eliminar un clúster de la organización.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code>-f</code></dt>
   <dd>Utilice esta opción para forzar la eliminación de un clúster sin solicitudes de usuario. Este valor es opcional.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs cluster-rm my_cluster
  ```
  {: pre}


### bx cs cluster-update [-f] CLUSTER [--kube-version MAJOR.MINOR.PATCH][--force-update]
{: #cs_cluster_update}

Actualice el maestro de Kubernetes a la versión predeterminada de la API. Durante la actualización, no puede acceder ni cambiar el clúster. Los nodos trabajadores, las apps y los recursos que los usuarios del clúster despliegan no se modifican y continúan ejecutándose. 

Es posible que tenga que modificar los archivos YAML para futuros despliegues. Revise esta [nota del release](cs_versions.html) para ver detalles.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code>--kube-version <em>MAJOR.MINOR.PATCH</em></code></dt>
   <dd>La versión de Kubernetes del clúster. Si no especifica una versión, el maestro de Kubernetes se actualiza a la versión predeterminada de la API. Para ver todas las versiones disponibles, ejecute [bx cs kube-versions](#cs_kube_versions). Este valor es opcional.</dd>

   <dt><code>-f</code></dt>
   <dd>Utilice esta opción para forzar la actualización del maestro sin solicitudes de usuario. Este valor es opcional.</dd>

   <dt><code>--force-update</code></dt>
   <dd>Intente la actualización incluso si el cambio es superior a dos versiones anteriores. Este valor es opcional.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs cluster-update my_cluster
  ```
  {: pre}


### bx cs clusters
{: #cs_clusters}

Ver una lista de los clústeres de la organización.

<strong>Opciones del mandato</strong>:

  Ninguno

**Ejemplo**:

  ```
  bx cs clusters
  ```
  {: pre}


### bx cs kube-versions
{: #cs_kube_versions}

Visualice una lista de las versiones de Kubernetes soportadas en {{site.data.keyword.containershort_notm}}. Actualice su [clúster maestro](#cs_cluster_update) y [nodos trabajadores](cs_cli_reference.html#cs_worker_update) a la versión predeterminada para obtener las prestaciones más estables y recientes.

**Opciones del mandato**:

  Ninguno

**Ejemplo**:

  ```
  bx cs kube-versions
  ```
  {: pre}



<br />



## Mandatos de clúster: Servicios e integraciones
{: #cluster_services_commands}


### bx cs cluster-service-bind CLUSTER KUBERNETES_NAMESPACE SERVICE_INSTANCE_NAME
{: #cs_cluster_service_bind}

Añadir un servicio de {{site.data.keyword.Bluemix_notm}} a un clúster. Para ver los servicios de {{site.data.keyword.Bluemix_notm}} disponibles en el catálogo de {{site.data.keyword.Bluemix_notm}}, ejecute `bx service offerings`. **Nota**: Sólo puede añadir servicios de {{site.data.keyword.Bluemix_notm}} que den soporte a claves de servicio.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code><em>KUBERNETES_NAMESPACE</em></code></dt>
   <dd>El nombre del espacio de Kubernetes. Este valor es obligatorio.</dd>

   <dt><code><em>SERVICE_INSTANCE_NAME</em></code></dt>
   <dd>El nombre de la instancia de servicio de {{site.data.keyword.Bluemix_notm}} que desea vincular. Para encontrar el nombre de la instancia de servicio, ejecute <code>bx service list</code>. Si más de una instancia tiene el mismo nombre en la cuenta, utilice el ID de instancia de servicio en lugar del nombre. Para encontrar el ID, ejecute <code>bx service show <service instance name> --guid</code>. Uno de estos valores es obligatorio.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs cluster-service-bind my_cluster my_namespace my_service_instance
  ```
  {: pre}


### bx cs cluster-service-unbind CLUSTER KUBERNETES_NAMESPACE SERVICE_INSTANCE_GUID
{: #cs_cluster_service_unbind}

Eliminar un servicio de {{site.data.keyword.Bluemix_notm}} de un clúster.

**Nota:** Cuando se elimina un servicio de {{site.data.keyword.Bluemix_notm}}, las credenciales del servicio se eliminan del clúster. Si un pod sigue utilizando el servicio, falla porque no encuentra las credenciales del servicio.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code><em>KUBERNETES_NAMESPACE</em></code></dt>
   <dd>El nombre del espacio de Kubernetes. Este valor es obligatorio.</dd>

   <dt><code><em>SERVICE_INSTANCE_GUID</em></code></dt>
   <dd>El ID de la instancia de servicio de {{site.data.keyword.Bluemix_notm}} que desea eliminar. Para encontrar el ID de la instancia de servicio, ejecute `bx cs cluster-services <cluster_name_or_ID>`. Este valor es obligatorio.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs cluster-service-unbind my_cluster my_namespace 8567221
  ```
  {: pre}


### bx cs cluster-services CLUSTER [--namespace KUBERNETES_NAMESPACE][--all-namespaces]
{: #cs_cluster_services}

Crear una lista de los servicios que están vinculados a uno o a todos los espacios de nombres de Kubernetes de un clúster. Si no se especifica ninguna opción, se muestran los servicios correspondientes al espacio de nombres predeterminado.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code>--namespace <em>KUBERNETES_NAMESPACE</em></code>, <code>-n
<em>KUBERNETES_NAMESPACE</em></code></dt>
   <dd>Incluya los servicios que están vinculados a un determinado espacio de nombres de un clúster. Este valor es opcional.</dd>

   <dt><code>--all-namespaces</code></dt>
    <dd>Incluya los servicios que están vinculados a todos los espacios de nombres de un clúster. Este valor es opcional.</dd>
    </dl>

**Ejemplo**:

  ```
  bx cs cluster-services my_cluster --namespace my_namespace
  ```
  {: pre}



### bx cs webhook-create --cluster CLUSTER --level LEVEL --type slack --url URL
{: #cs_webhook_create}

Registrar un webhook.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code>--cluster <em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code>--level <em>LEVEL</em></code></dt>
   <dd>El nivel de notificación, como por ejemplo <code>Normal</code> o <code>Warning</code>. <code>Warning</code> es el valor predeterminado. Este valor es opcional.</dd>

   <dt><code>--type <em>slack</em></code></dt>
   <dd>El tipo de webhook. Actualmente se admite slack. Este valor es obligatorio.</dd>

   <dt><code>--url <em>URL</em></code></dt>
   <dd>El URL del webhook. Este valor es obligatorio.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs webhook-create --cluster my_cluster --level Normal --type slack --url http://github.com/mywebhook
  ```
  {: pre}


<br />


## Mandatos de clúster: Subredes
{: #cluster_subnets_commands}

### bx cs cluster-subnet-add CLUSTER SUBNET
{: #cs_cluster_subnet_add}

Poner la subred de la cuenta de una infraestructura de IBM Cloud (SoftLayer)
a disponibilidad de un determinado clúster.

**Nota:**
* Cuando pone una subred a disponibilidad de un clúster, las direcciones IP de esta subred se utilizan para la gestión de redes del clúster. Para evitar conflictos de direcciones IP, asegúrese de utilizar una subred con un solo clúster. No utilice una subred para varios clústeres o para otros fines externos a {{site.data.keyword.containershort_notm}} al mismo tiempo.
* Para direccionar entre subredes de la misma VLAN, se debe [activar la expansión de VLAN](/docs/infrastructure/vlans/vlan-spanning.html#enable-or-disable-vlan-spanning).

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code><em>SUBNET</em></code></dt>
   <dd>El ID de la subred. Este valor es obligatorio.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs cluster-subnet-add my_cluster 1643389
  ```
  {: pre}


### bx cs cluster-subnet-create CLUSTER SIZE VLAN_ID
{: #cs_cluster_subnet_create}

Crear una subred en una cuenta de infraestructura de IBM Cloud (SoftLayer) y ponerla a disponibilidad de un determinado clúster en {{site.data.keyword.containershort_notm}}.

**Nota:**
* Cuando pone una subred a disponibilidad de un clúster, las direcciones IP de esta subred se utilizan para la gestión de redes del clúster. Para evitar conflictos de direcciones IP, asegúrese de utilizar una subred con un solo clúster. No utilice una subred para varios clústeres o para otros fines externos a {{site.data.keyword.containershort_notm}} al mismo tiempo.
* Para direccionar entre subredes de la misma VLAN, se debe [activar la expansión de VLAN](/docs/infrastructure/vlans/vlan-spanning.html#enable-or-disable-vlan-spanning).

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio. Para obtener una lista de los clústeres, utilice el [mandato](#cs_clusters) `cs bx clusters`.</dd>

   <dt><code><em>SIZE</em></code></dt>
   <dd>El número de direcciones IP de la subred. Este valor es obligatorio. Los valores posibles son 8, 16, 32 o 64.</dd>

   <dt><code><em>VLAN_ID</em></code></dt>
   <dd>La VLAN en el que se va a crear la subred. Este valor es obligatorio. Para ver una lista de las VLAN disponibles, utilice el [mandato](#cs_vlans) `bx cs vlans <location>`. </dd>
   </dl>

**Ejemplo**:

  ```
  bx cs cluster-subnet-create my_cluster 8 1764905
  ```
  {: pre}


### bx cs cluster-user-subnet-add CLUSTER SUBNET_CIDR PRIVATE_VLAN
{: #cs_cluster_user_subnet_add}

Traer su propia subred privada a sus clústeres de {{site.data.keyword.containershort_notm}}.

Esta subred privada no es la que proporciona la infraestructura de IBM Cloud (SoftLayer). Por lo tanto, debe configurar el direccionamiento del tráfico de la red de entrada y de salida para la subred. Para añadir una subred de infraestructura de IBM Cloud (SoftLayer), utilice el [mandato](#cs_cluster_subnet_add) `bx cs cluster-subnet-add`.

**Nota**:
* Cuando añade una subred de usuario privada a un clúster, las direcciones IP de esta subred se utilizan para los equilibradores de carga privados del clúster. Para evitar conflictos de direcciones IP, asegúrese de utilizar una subred con un solo clúster. No utilice una subred para varios clústeres o para otros fines externos a {{site.data.keyword.containershort_notm}} al mismo tiempo.
* Para direccionar entre subredes de la misma VLAN, se debe [activar la expansión de VLAN](/docs/infrastructure/vlans/vlan-spanning.html#enable-or-disable-vlan-spanning).

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code><em>SUBNET_CIDR</em></code></dt>
   <dd>El Classless InterDomain Routing (CIDR) de la subred. Este valor es obligatorio y no debe estar en conflicto con ninguna subred que utilice la infraestructura de IBM Cloud (SoftLayer).

   Los prefijos válidos son los comprendidos entre `/30` (1 dirección IP) y `/24` (253 direcciones IP). Si establece el valor de CIDR en una longitud de prefijo y luego lo tiene que modificar, añada primero un nuevo CIDR y luego [elimine el CIDR antiguo](#cs_cluster_user_subnet_rm).</dd>

   <dt><code><em>PRIVATE_VLAN</em></code></dt>
   <dd>El ID de la VLAN privada. Este valor es obligatorio. Debe coincidir con el ID de VLAN privada de uno o varios nodos trabajadores del clúster.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs cluster-user-subnet-add my_cluster 169.xx.xxx.xxx/29 1502175
  ```
  {: pre}


### bx cs cluster-user-subnet-rm CLUSTER SUBNET_CIDR PRIVATE_VLAN
{: #cs_cluster_user_subnet_rm}

Elimine su propia subred privada de un clúster especificado.

**Nota:** Cualquier servicio que se haya desplegado en una dirección IP desde su propia subred privada permanece activo después de que se elimine la subred.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code><em>SUBNET_CIDR</em></code></dt>
   <dd>El Classless InterDomain Routing (CIDR) de la subred. Este valor es obligatorio y debe coincidir con el CIDR especificado mediante en [mandato](#cs_cluster_user_subnet_add) `bx cs cluster-user-subnet-add`.</dd>

   <dt><code><em>PRIVATE_VLAN</em></code></dt>
   <dd>El ID de la VLAN privada. Este valor es obligatorio y debe coincidir con el ID de VLAN especificado mediante en [mandato](#cs_cluster_user_subnet_add) `bx cs cluster-user-subnet-add`.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs cluster-user-subnet-rm my_cluster 169.xx.xxx.xxx/29 1502175
  ```
  {: pre}

### bx cs subnets
{: #cs_subnets}

Ver una lista de subredes que están disponibles en una cuenta de infraestructura de IBM Cloud (SoftLayer).

<strong>Opciones del mandato</strong>:

   Ninguno

**Ejemplo**:

  ```
  bx cs subnets
  ```
  {: pre}


<br />


## Mandatos del equilibrador de carga de aplicación (ALB) de Ingress
{: #alb_commands}

### bx cs alb-cert-deploy [--update] --cluster CLUSTER --secret-name SECRET_NAME --cert-crn CERTIFICATE_CRN
{: #cs_alb_cert_deploy}

Despliegue o actualice un certificado de la instancia de {{site.data.keyword.cloudcerts_long_notm}} al ALB de un clúster.

**Nota:**
* Sólo un usuario con el rol de acceso de Administrador puede ejecutar este mandato.
* Sólo puede actualizar certificados que importados de la misma instancia de {{site.data.keyword.cloudcerts_long_notm}}.

<strong>Opciones del mandato</strong>

   <dl>
   <dt><code>--cluster <em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code>--update</code></dt>
   <dd>Incluya este distintivo para actualizar el certificado para un secreto de ALB en un clúster. Este valor es opcional.</dd>

   <dt><code>--secret-name <em>SECRET_NAME</em></code></dt>
   <dd>El nombre del secreto de ALB. Este valor es obligatorio.</dd>

   <dt><code>--cert-crn <em>CERTIFICATE_CRN</em></code></dt>
   <dd>El CRN de certificado. Este valor es obligatorio.</dd>
   </dl>

**Ejemplos**:

Ejemplo para desplegar un secreto de ALB:

   ```
   bx cs alb-cert-deploy --secret-name my_alb_secret --cluster my_cluster --cert-crn crn:v1:staging:public:cloudcerts:us-south:a/06580c923e40314421d3b6cb40c01c68:0db4351b-0ee1-479d-af37-56a4da9ef30f:certificate:4bc35b7e0badb304e60aef00947ae7ff
   ```
   {: pre}

Ejemplo para actualizar un secreto de ALB existente:

 ```
 bx cs alb-cert-deploy --update --secret-name my_alb_secret --cluster my_cluster --cert-crn crn:v1:staging:public:cloudcerts:us-south:a/06580c923e40314421d3b6cb40c01c68:0db4351b-0ee1-479d-af37-56a4da9ef30f:certificate:7e21fde8ee84a96d29240327daee3eb2
 ```
 {: pre}


### bx cs alb-cert-get --cluster CLUSTER [--secret-name SECRET_NAME][--cert-crn CERTIFICATE_CRN]
{: #cs_alb_cert_get}

Visualice información sobre un secreto de ALB en un clúster.

**Nota:** Sólo un usuario con el rol de acceso de Administrador puede ejecutar este mandato.

<strong>Opciones del mandato</strong>

  <dl>
  <dt><code>--cluster <em>CLUSTER</em></code></dt>
  <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

  <dt><code>--secret-name <em>SECRET_NAME</em></code></dt>
  <dd>El nombre del secreto de ALB. Este valor es necesario para obtener información sobre un secreto de ALB específico en el clúster.</dd>

  <dt><code>--cert-crn <em>CERTIFICATE_CRN</em></code></dt>
  <dd>El CRN de certificado. Este valor es necesario para obtener información sobre todos los secretos de ALB coincidentes con un CRN de certificado determinado en el clúster.</dd>
  </dl>

**Ejemplos**:

 Ejemplo para captar un secreto de ALB:

 ```
 bx cs alb-cert-get --cluster my_cluster --secret-name my_alb_secret
 ```
 {: pre}

 Ejemplo para obtener información sobre todos los secretos de ALB que coinciden con un CRN de certificado especificado:

 ```
 bx cs alb-cert-get --cluster my_cluster --cert-crn  crn:v1:staging:public:cloudcerts:us-south:a/06580c923e40314421d3b6cb40c01c68:0db4351b-0ee1-479d-af37-56a4da9ef30f:certificate:4bc35b7e0badb304e60aef00947ae7ff
 ```
 {: pre}


### bx cs alb-cert-rm --cluster CLUSTER [--secret-name SECRET_NAME][--cert-crn CERTIFICATE_CRN]
{: #cs_alb_cert_rm}

Elimine un secreto de ALB en un clúster.

**Nota:** Sólo un usuario con el rol de acceso de Administrador puede ejecutar este mandato.

<strong>Opciones del mandato</strong>

  <dl>
  <dt><code>--cluster <em>CLUSTER</em></code></dt>
  <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

  <dt><code>--secret-name <em>SECRET_NAME</em></code></dt>
  <dd>El nombre del secreto de ALB. Este valor es necesario para eliminar un secreto de ALB específico en el clúster.</dd>

  <dt><code>--cert-crn <em>CERTIFICATE_CRN</em></code></dt>
  <dd>El CRN de certificado. Este valor es necesario para eliminar todos los secretos de ALB coincidentes con un CRN de certificado determinado en el clúster.</dd>
  </dl>

**Ejemplos**:

 Ejemplo para eliminar un secreto de ALB:

 ```
 bx cs alb-cert-rm --cluster my_cluster --secret-name my_alb_secret
 ```
 {: pre}

 Ejemplo para eliminar todos los secretos de ALB que coinciden con un CRN de certificado especificado:

 ```
 bx cs alb-cert-rm --cluster my_cluster --cert-crn crn:v1:staging:public:cloudcerts:us-south:a/06580c923e40314421d3b6cb40c01c68:0db4351b-0ee1-479d-af37-56a4da9ef30f:certificate:4bc35b7e0badb304e60aef00947ae7ff
 ```
 {: pre}


### bx cs alb-certs --cluster CLUSTER
{: #cs_alb_certs}

Visualice una lista de secretos de ALB en un clúster.

**Nota:** Únicamente los usuarios con el rol de acceso de Administrador puede ejecutar este mandato.

<strong>Opciones del mandato</strong>

   <dl>
   <dt><code>--cluster <em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>
   </dl>

**Ejemplo**:

 ```
 bx cs alb-certs --cluster my_cluster
 ```
 {: pre}




### bx cs alb-configure --albID ALB_ID [--enable][--disable][--user-ip USERIP]
{: #cs_alb_configure}

Habilite o inhabilite un ALB en el clúster estándar. El ALB público está habilitado de forma predeterminada.

**Opciones del mandato**:

   <dl>
   <dt><code><em>--albID </em>ALB_ID</code></dt>
   <dd>El ID de un ALB. Ejecute <code>bx cs albs <em>--cluster </em>CLUSTER</code> para ver los ID de los ALB de un clúster. Este valor es obligatorio.</dd>

   <dt><code>--enable</code></dt>
   <dd>Incluya este distintivo para habilitar un ALB en un clúster.</dd>

   <dt><code>--disable</code></dt>
   <dd>Incluya este distintivo para inhabilitar un ALB en un clúster.</dd>

   <dt><code>--user-ip <em>USER_IP</em></code></dt>
   <dd>

   <ul>
    <li>Este parámetro está disponible solo para un ALB privado.</li>
    <li>El ALB privado se despliega con una dirección IP de una subred privada proporcionada por un usuario. Si no se proporciona la dirección IP, el ALB se despliega con una dirección IP privada de la subred privada portátil que se suministra automáticamente cuando se crea el clúster.</li>
   </ul>
   </dd>
   </dl>

**Ejemplos**:

  Ejemplo para habilitar un ALB:

  ```
  bx cs alb-configure --albID private-cr18a61a63a6a94b658596aa93a087aaa9-alb1 --enable
  ```
  {: pre}

  Ejemplo para inhabilitar un ALB:

  ```
  bx cs alb-configure --albID public-cr18a61a63a6a94b658596aa93a087aaa9-alb1 --disable
  ```
  {: pre}

  Ejemplo para habilitar un ALB con una dirección IP proporcionada por un usuario:

  ```
  bx cs alb-configure --albID private-cr18a61a63a6a94b658596aa93a087aaa9-alb1 --enable --user-ip user_ip
  ```
  {: pre}



### bx cs alb-get --albID ALB_ID
{: #cs_alb_get}

Visualice los detalles de un ALB.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>--albID </em>ALB_ID</code></dt>
   <dd>El ID de un ALB. Ejecute <code>bx cs albs --cluster <em>CLUSTER</em></code> para ver los ID de los ALB de un clúster. Este valor es obligatorio.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs alb-get --albID public-cr18a61a63a6a94b658596aa93a087aaa9-alb1
  ```
  {: pre}

### bx cs alb-types
{: #cs_alb_types}

Visualice los tipos de ALB que están soportados en la región.

<strong>Opciones del mandato</strong>:

   Ninguno

**Ejemplo**:

  ```
  bx cs alb-types
  ```
  {: pre}


### bx cs albs --cluster CLUSTER
{: #cs_albs}

Visualice el estado de todos los ALB de un clúster. Si no se devuelve ningún ID de ALB, significa que el clúster no tiene subred portátil. Puede [crear](#cs_cluster_subnet_create) o [añadir](#cs_cluster_subnet_add) subredes a un clúster.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>--cluster </em>CLUSTER</code></dt>
   <dd>El nombre o ID del clúster en el que se listan los ALB disponibles. Este valor es obligatorio.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs albs --cluster my_cluster
  ```
  {: pre}


<br />


## Mandatos de infraestructura
{: #infrastructure_commands}

### bx cs credentials-set --infrastructure-api-key API_KEY --infrastructure-username USERNAME
{: #cs_credentials_set}

Defina las credenciales de cuenta de la infraestructura de IBM Cloud (SoftLayer) para su cuenta de {{site.data.keyword.containershort_notm}}.

Si tiene una cuenta de pago según uso de {{site.data.keyword.Bluemix_notm}}, tiene acceso al portafolio de infraestructura de IBM Cloud (de SoftLayer) de forma predeterminada. Sin embargo, es posible que desee utilizar otra cuenta de infraestructura de IBM Cloud (SoftLayer) que ya tenga para solicitar infraestructura. Puede enlazar esta cuenta de infraestructura a la cuenta de {{site.data.keyword.Bluemix_notm}} mediante este mandato.

Si las credenciales de infraestructura de IBM Cloud (SoftLayer) se establecen manualmente, estas credenciales se utilizan para pedir infraestructura, aunque ya exista una [clave de API IAM](#cs_api_key_info) para la cuenta. Si el usuario cuyas credenciales se almacenan no tiene los permisos necesarios para pedir infraestructura, entonces las acciones relacionadas con la infraestructura, como crear un clúster o recargar un nodo trabajador, pueden fallar.

No puede definir varias credenciales para una cuenta de {{site.data.keyword.containershort_notm}}. Cada cuenta de {{site.data.keyword.containershort_notm}} está vinculada a un portafolio de la infraestructura de IBM Cloud (SoftLayer).

**Importante:** Antes de utilizar este mandato, asegúrese de que el usuario cuyas credenciales se utilizan tiene los [permisos de infraestructura de IBM Cloud (SoftLayer) e {{site.data.keyword.containershort_notm}}](cs_users.html#users) necesarios.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code>--infrastructure-username <em>USERNAME</em></code></dt>
   <dd>Nombre usuario de la cuenta de infraestructura de IBM Cloud (SoftLayer). Este valor es obligatorio.</dd>


   <dt><code>--infrastructure-api-key <em>API_KEY</em></code></dt>
   <dd>Clave de API de la cuenta de infraestructura de IBM Cloud (SoftLayer). Este valor es obligatorio.

 <p>
  Para generar una clave de API:

  <ol>
  <li>Inicie sesión en el [portal de la infraestructura de IBM Cloud (SoftLayer) ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/).</li>
  <li>Seleccione <strong>Cuenta</strong> y, a continuación, <strong>Usuarios</strong>.</li>
  <li>Pulse <strong>Generar</strong> para generar una clave de API de la infraestructura de IBM Cloud (SoftLayer) para su cuenta.</li>
  <li>Copie la clave de la API para utilizar en este mandato.</li>
  </ol>

  Para ver una clave de API existente:
  <ol>
  <li>Inicie sesión en el [portal de la infraestructura de IBM Cloud (SoftLayer) ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/).</li>
  <li>Seleccione <strong>Cuenta</strong> y, a continuación, <strong>Usuarios</strong>.</li>
  <li>Pulse <strong>Ver</strong> para ver la clave de API existente.</li>
  <li>Copie la clave de la API para utilizar en este mandato.</li>
  </ol>
  </p></dd>
  </dl>

**Ejemplo**:

  ```
  bx cs credentials-set --infrastructure-api-key <api_key> --infrastructure-username dbmanager
  ```
  {: pre}


### bx cs credentials-unset
{: #cs_credentials_unset}

Elimine las credenciales de cuenta de la infraestructura de IBM Cloud (SoftLayer) de su cuenta de {{site.data.keyword.containershort_notm}}.

Una vez que elimina las credenciales, la [clave de API IAM](#cs_api_key_info) se utiliza para pedir recursos en la infraestructura de IBM Cloud (SoftLayer).

<strong>Opciones del mandato</strong>:

   Ninguno

**Ejemplo**:

  ```
  bx cs credentials-unset
  ```
  {: pre}


### bx cs machine-types LOCATION
{: #cs_machine_types}

Ver una lista de los tipos de máquinas disponibles para sus nodos trabajadores. Cada tipo de máquina incluye cantidad de CPU virtual, memoria y espacio de disco para cada nodo trabajador del clúster. De forma predeterminada, el directorio `/var/lib/docker`, donde están almacenados todos los datos de los contenedores, está cifrado mediante LUKS. Si la opción `disable-disk-encrypt` se incluye durante la creación de clústeres, los datos de Docker del host no se cifrarán. [Más información sobre el cifrado.](cs_secure.html#encrypted_disks)
{:shortdesc}

Puede suministrar el nodo trabajador como una máquina virtual en hardware dedicado o compartido, o como una máquina física en un servidor nativo.

<dl>
<dt>Máquinas físicas (nativas)</dt>
<dd>Puede suministrar el nodo trabajador como un servidor físico de arrendatario único, también conocido como nativo. Los servidores nativos ofrecen acceso directo a los recursos físicos en la máquina, como la memoria o la CPU. Esta configuración elimina el hipervisor de máquina virtual que asigna recursos físicos a máquinas virtuales que se ejecutan en el host. En su lugar, todos los recursos de una máquina nativa están dedicados exclusivamente al trabajador, por lo que no es necesario preocuparse por "vecinos ruidosos" que compartan recursos o ralenticen el rendimiento.
<p><strong>Facturación mensual</strong>: los servidores nativos son más caros que los servidores virtuales, y son más apropiados para apps de alto rendimiento que necesitan más recursos y control de host. Los servidores nativos se facturan de forma mensual. Si cancela un servidor nativo antes de fin de mes, se le facturará a finales de ese mes. La realización de pedidos de servidores nativos, y su cancelación, es un proceso manual que se realiza a través de su cuenta (SoftLayer) de la infraestructura de IBM Cloud. Puede ser necesario más de un día laborable para completar la tramitación. </p>
<p><strong>Opción para habilitar Trusted Compute</strong>: Habilite Trusted Compute para protegerse ante la manipulación indebida de nodos trabajadores. Si no habilita la confianza durante la creación del clúster pero desea hacerlo posteriormente, puede utilizar el [mandato](cs_cli_reference.html#cs_cluster_feature_enable) `bx cs feature-enable`. Una vez que habilita la confianza, no puede inhabilitarla posteriormente. Puede crear un nuevo clúster sin confianza. Para obtener más información sobre cómo funciona la confianza durante el proceso de inicio del nodo, consulte [{{site.data.keyword.containershort_notm}} con Trusted Compute](cs_secure.html#trusted_compute). Trusted Compute está disponible en los clústeres donde se ejecuta Kubernetes versión 1.9 o posterior y poseen determinados tipos de máquina nativos. Cuando ejecute el [mandato](cs_cli_reference.html#cs_machine_types) `bx cs machine-types <location>`, en el campo `Trustable` puede ver qué máquinas son compatibles con la confianza.</p>
<p><strong>Grupos de tipo de máquina nativa</strong>: Los tipos de máquina nativa vienen en grupos que tienen distintos recursos de cálculo que puede elegir para satisfacer las necesidades de la app.
Los tipos de máquina física tienen más almacenamiento local que virtual, y algunos tienen RAID para realizar copias de seguridad de datos locales. Para obtener más información sobre los distintos tipos de ofertas nativas, consulte el [mandato](cs_cli_reference.html#cs_machine_types) `bx cs machine-type`.
<ul><li>`mb1c.4x32`: Si no necesita RAM, u otros recursos intensivos de datos, seleccione este tipo para obtener una configuración equilibrada de los recursos de la máquina física para los nodos trabajadores. Equilibrado con 4 núcleos, 32 GB de memoria, disco primario SATA de 1 TB, disco secundario SATA de 2 TB, red adherida de 10 Gbps.</li>
<li>`mb1c.16x64`: Si no necesita RAM, u otros recursos intensivos de datos, seleccione este tipo para obtener una configuración equilibrada de los recursos de la máquina física para los nodos trabajadores. Equilibrado con 16 núcleos, 64 GB de memoria, disco primario SATA de 1 TB, disco secundario SSD de 1,7 TB, red adherida de 10 Gbps.</li>
<li>`mr1c.28x512`: Seleccione este tipo para maximizar la RAM disponible para los nodos trabajadores. Uso intensivo de RAM con 28 núcleos, 512 GB de memoria, disco primario SATA de 1 TB, disco secundario SSD de 1,7 TB, red adherida de 10 Gbps.</li>
<li>`md1c.16x64.4x4tb`: Seleccione este tipo si los nodos trabajadores requieren una cantidad significativa de almacenamiento en disco local, incluido RAID para realizar copia de seguridad de los datos almacenados localmente en la máquina. Los discos de almacenamiento primario de 1 TB están configurados para RAID1, y los discos de almacenamiento secundario de 4TB están configurados para RAID10. Uso intensivo de datos con 28 núcleos, 512 GB de memoria, 2 discos primarios RAID1 de 1 TB, 4 discos secundarios SATA de RAID10 de 4 TB, red adherida de 10 Gbps.</li>
<li>`md1c.28x512.4x4tb`: Seleccione este tipo si los nodos trabajadores requieren una cantidad significativa de almacenamiento en disco local, incluido RAID para realizar copia de seguridad de los datos almacenados localmente en la máquina. Los discos de almacenamiento primario de 1 TB están configurados para RAID1, y los discos de almacenamiento secundario de 4TB están configurados para RAID10. Uso intensivo de datos con 16 núcleos, 64 GB de memoria, 2 discos primarios RAID1 de 1 TB, 4 discos secundarios SATA de RAID10 de 4 TB, red adherida de 10 Gbps.</li>

</ul></p></dd>
<dt>Máquinas virtuales</dt>
<dd>Cuando se crea un clúster virtual estándar, debe seleccionar si desea que el hardware subyacente se comparta entre varios clientes de {{site.data.keyword.IBM_notm}} (tenencia múltiple) o se le dedique a usted exclusivamente (tenencia única).
<p>En una configuración de tenencia múltiple, los recursos físicos, como CPU y memoria, se comparten entre todas las máquinas virtuales desplegadas en el mismo hardware físico. Para asegurarse de que cada máquina virtual se pueda ejecutar de forma independiente, un supervisor de máquina virtual, también conocido como hipervisor, segmenta los recursos físicos en entidades aisladas y los asigna como recursos dedicados a una máquina virtual (aislamiento de hipervisor).</p>
<p>En una configuración de tenencia única, se dedican al usuario todos los recursos físicos. Puede desplegar varios nodos trabajadores como máquinas virtuales en el mismo host físico. De forma similar a la configuración de tenencia múltiple,
el hipervisor asegura que cada nodo trabajador recibe su parte compartida de los recursos físicos disponibles.</p>
<p>Los nodos compartidos suelen resultar más económicos que los nodos dedicados porque los costes del hardware subyacente se comparten entre varios clientes. Sin embargo, cuando decida entre nodos compartidos y dedicados, debe ponerse en contacto con el departamento legal y ver el nivel de aislamiento y de conformidad de la infraestructura que necesita el entorno de app.</p>
<p><strong>Tipos de máquinas virtuales `u2c` o `b2c`</strong>: Estas máquinas utilizan el disco local en lugar de la red de área de almacenamiento (SAN) por motivos de fiabilidad. Entre las ventajas de fiabilidad se incluyen un mejor rendimiento al serializar bytes en el disco local y una reducción de la degradación del sistema de archivos debido a anomalías de la red. Este tipo de máquinas contienen 25 GB de almacenamiento en disco local primario para el sistema de archivos de SO y 100 GB de almacenamiento en disco local secundario para `/var/lib/docker`, el directorio en el que se graban todos los datos del contenedor.</p>
<p><strong>Tipos de máquina en desuso `u1c` o `b1c`</strong>: Para empezar a utilizar los tipos de máquina `u2c` y `b2c`, [actualice los tipos de máquina añadiendo nodos trabajadores](cs_cluster_update.html#machine_type).</p></dd>
</dl>


<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>LOCATION</em></code></dt>
   <dd>Especifique la ubicación de la que desea ver una lista de tipos de máquina disponibles. Este valor es obligatorio. Consulte [ubicaciones disponibles](cs_regions.html#locations).</dd></dl>

**Mandato de ejemplo**:

  ```
  bx cs machine-types dal10
  ```
  {: pre}

**Salida de ejemplo**:

  ```
  Getting machine types list...
  OK
  Machine Types
  Name                 Cores   Memory   Network Speed   OS             Server Type   Storage   Secondary Storage   Trustable
  u2c.2x4              2       4GB      1000Mbps        UBUNTU_16_64   virtual       25GB      100GB               False
  b2c.4x16             4       16GB     1000Mbps        UBUNTU_16_64   virtual       25GB      100GB               False
  b2c.16x64            16      64GB     1000Mbps        UBUNTU_16_64   virtual       25GB      100GB               False
  b2c.32x128           32      128GB    1000Mbps        UBUNTU_16_64   virtual       25GB      100GB               False
  b2c.56x242           56      242GB    1000Mbps        UBUNTU_16_64   virtual       25GB      100GB               False
  mb1c.4x32            4       32GB     10000Mbps       UBUNTU_16_64   physical      1000GB    2000GB              False
  mb1c.16x64           16      64GB     10000Mbps       UBUNTU_16_64   physical      1000GB    1700GB              False
  mr1c.28x512          28      512GB    10000Mbps       UBUNTU_16_64   physical      1000GB    1700GB              False
  md1c.16x64.4x4tb     16      64GB     10000Mbps       UBUNTU_16_64   physical      1000GB    8000GB              False
  md1c.28x512.4x4tb    28      512GB    10000Mbps       UBUNTU_16_64   physical      1000GB    8000GB              False
  
  ```
  {: screen}


### bx cs vlans LOCATION [--all]
{: #cs_vlans}

Crear una lista de las VLAN públicas y privadas disponibles para una ubicación en la cuenta de infraestructura de IBM Cloud (SoftLayer). Para ver una lista de las VLAN disponibles,
debe tener una cuenta de pago.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>LOCATION</em></code></dt>
   <dd>Escriba la ubicación donde desea listar sus VLAN públicas y privadas. Este valor es obligatorio. Consulte [ubicaciones disponibles](cs_regions.html#locations).</dd>
   <dt><code>--all</code></dt>
   <dd>Obtenga una lista de todas las VLAN disponibles. De forma predeterminada, las VLAN se filtran para mostrar solo las VLAN que son válidas. Para ser válida, una VLAN debe estar asociada con infraestructura que pueda alojar un trabajador con almacenamiento en disco local.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs vlans dal10
  ```
  {: pre}


<br />


## Mandatos de registro
{: #logging_commands}

### bx cs logging-config-create CLUSTER --logsource LOG_SOURCE [--namespace KUBERNETES_NAMESPACE][--hostname LOG_SERVER_HOSTNAME_OR_IP] [--port LOG_SERVER_PORT][--space CLUSTER_SPACE] [--org CLUSTER_ORG][--app-containers CONTAINERS] [--app-paths PATHS_TO_LOGS] --type LOG_TYPE [--json][--skip-validation]
{: #cs_logging_create}

Crear una configuración de registro. Puede utilizar este mandato para reenviar los registros correspondientes a contenedores, aplicaciones, nodos trabajadores, clústeres de Kubernetes y equilibradores de carga de aplicación de Ingress a {{site.data.keyword.loganalysisshort_notm}} o a un servidor syslog externo.

<strong>Opciones del mandato</strong>:

<dl>
  <dt><code><em>CLUSTER</em></code></dt>
    <dd>El nombre o ID del clúster.</dd>
  <dt><code>--logsource <em>LOG_SOURCE</em></code></dt>
    <dd>El origen de registro para el que desea habilitar el reenvío de registros. Este argumento da soporte a una lista separada por comas de orígenes de registro a los que aplicar la configuración. Los valores aceptados son <code>container</code>, <code>application</code>, <code>worker</code>, <code>kubernetes</code> e <code>ingress</code>. Si no proporciona un origen de registro, las configuraciones de registro se crean para los orígenes de registro <code>container</code> e <code>ingress</code>.</dd>
  <dt><code>--namespace <em>KUBERNETES_NAMESPACE</em></code></dt>
    <dd>El espacio de Kubernetes desde el que desea reenviar registros. El reenvío de registros no recibe soporte para los espacios de nombres de Kubernetes <code>ibm-system</code> y <code>kube-system</code>. Este valor sólo es válido para el origen de registro de contenedor y es opcional. Si no especifica un espacio de nombres, todos los espacios de nombres del clúster utilizarán esta configuración.</dd>
  <dt><code>--hostname <em>LOG_SERVER_HOSTNAME</em></code></dt>
    <dd>Cuando el tipo de registro es <code>syslog</code>, el nombre de host o dirección IP del servidor del recopilador de registro. Este valor es obligatorio para <code>syslog</code>. Cuando el tipo de registro es <code>ibm</code>, el URL de ingestión de {{site.data.keyword.loganalysislong_notm}}. Puede encontrar la lista de URL de ingestión disponible [aquí](/docs/services/CloudLogAnalysis/log_ingestion.html#log_ingestion_urls). Si no especifica un URL de ingestión, se utiliza el punto final de la región en la que se ha creado el clúster.</dd>
  <dt><code>--port <em>LOG_SERVER_PORT</em></code></dt>
    <dd>El puerto del servidor del recopilador de registro. Este valor es opcional. Si no especifica un puerto, se utiliza el puerto estándar <code>514</code> para <code>syslog</code> y el puerto estándar <code>9091</code> para <code>ibm</code>.</dd>
  <dt><code>--space <em>CLUSTER_SPACE</em></code></dt>
    <dd>El nombre del espacio de Cloud Foundry al que desea enviar registros. Este valor sólo es válido para el registro de tipo <code>ibm</code> y es opcional. Si no especifica un espacio, los registros se envían al nivel de cuenta.</dd>
  <dt><code>--org <em>CLUSTER_ORG</em></code></dt>
    <dd>El nombre de la organización de Cloud Foundry en la que está el espacio. Este valor sólo es válido para el registro de tipo <code>ibm</code> y es necesario si ha especificado un espacio.</dd>
  <dt><code>--app-paths</code></dt>
    <dd>La vía de acceso al contenedor donde las apps realizan registros. Para reenviar registros con el tipo de origen <code>application</code>, debe proporcionar una vía de acceso. Para especificar más de una vía de acceso, utilice una lista separada por comas. Este valor es necesario para el origen de registro <code>application</code>. Ejemplo: <code>/var/log/myApp1/&ast;,/var/log/myApp2/&ast;</code></dd>
  <dt><code>--type <em>LOG_TYPE</em></code></dt>
    <dd>El destino al que desea reenviar los registros. Las opciones son <code>ibm</code>, que reenvía los registros a {{site.data.keyword.loganalysisshort_notm}} y <code>syslog</code>, que reenvía los registros a un servidor externo.</dd>
  <dt><code>--app-containers</code></dt>
    <dd>Opcional: Para reenviar registros de apps, puede especificar el nombre del contenedor que contiene la app. Puede especificar más de un contenedor mediante una lista separada por comas. Si no se especifica ningún contenedor, se reenvían los registros de todos los contenedores que contienen las vías de acceso indicadas. Esta opción únicamente es válida para el origen de registro <code>application</code>. </dt>
  <dt><code>--json</code></dt>
    <dd>Imprime la salida del mandato en formato JSON. Este valor es opcional.</dd>
  <dt><code>--skip-validation</code></dt>
    <dd>Omite la validación de los nombres de espacio y organización cuando se especifican. Al omitir la validación, disminuye el tiempo de proceso, pero si la configuración de registro no es válida, los registros no se reenviarán correctamente. Este valor es opcional.</dd>
</dl>

**Ejemplos**:

Ejemplo de registro de tipo `ibm` que reenvía desde un origen de registro de `contenedor` en el puerto predeterminado 9091:

  ```
  bx cs logging-config-create my_cluster --logsource container --namespace my_namespace --hostname ingest.logging.ng.bluemix.net --type ibm
  ```
  {: pre}

Ejemplo de registro de tipo `syslog` que reenvía desde un origen de registro de `contenedor` en el puerto predeterminado 514:

  ```
  bx cs logging-config-create my_cluster --logsource container --namespace my_namespace  --hostname 169.xx.xxx.xxx --type syslog
  ```
  {: pre}

Ejemplo de registro de tipo `syslog` que reenvía registros desde un origen de `ingress` en un puerto distinto al predeterminado:

  ```
  bx cs logging-config-create my_cluster --logsource container --hostname 169.xx.xxx.xxx --port 5514 --type syslog
  ```
  {: pre}

### bx cs logging-config-get CLUSTER [--logsource LOG_SOURCE][--json]
{: #cs_logging_get}

Vea todas las configuraciones de reenvío de registro para un clúster, o filtre las configuraciones de registro en función del origen del registro.

<strong>Opciones del mandato</strong>:

 <dl>
  <dt><code><em>CLUSTER</em></code></dt>
    <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>
  <dt><code>--logsource <em>LOG_SOURCE</em></code></dt>
    <dd>El tipo de origen de registro que desea filtrar. Sólo se devolverán las configuraciones de registro de este origen de registro en el clúster. Los valores aceptados son <code>container</code>, <code>application</code>, <code>worker</code>, <code>kubernetes</code> e <code>ingress</code>. Este valor es opcional.</dd>
  <dt><code>--json</code></dt>
    <dd>Opcionalmente, imprime la salida del mandato en formato JSON.</dd>
 </dl>

**Ejemplo**:

  ```
  bx cs logging-config-get my_cluster --logsource worker
  ```
  {: pre}


### bx cs logging-config-refresh CLUSTER
{: #cs_logging_refresh}

Renueve la configuración de registro para el clúster. Renueva la señal de registro para cualquier configuración de registro que se esté reenviando al nivel de espacio en el clúster.

<strong>Opciones del mandato</strong>:

<dl>
  <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>
</dl>

**Ejemplo**:

  ```
  bx cs logging-config-refresh my_cluster
  ```
  {: pre}


### bx cs logging-config-rm CLUSTER [--id LOG_CONFIG_ID][--all]
{: #cs_logging_rm}

Suprima una configuración de reenvío de registros o todas las configuraciones de registro de un clúster. Esto detiene el reenvío del registro a un servidor syslog remoto o a {{site.data.keyword.loganalysisshort_notm}}.

<strong>Opciones del mandato</strong>:

<dl>
  <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>
  <dt><code>--id <em>LOG_CONFIG_ID</em></code></dt>
   <dd>Si desea eliminar una única configuración de registro, el ID de la configuración de registro.</dd>
  <dt><code>--all</code></dt>
   <dd>El distintivo para eliminar todas las configuraciones de registro de un clúster.</dd>
</dl>

**Ejemplo**:

  ```
  bx cs logging-config-rm my_cluster --id f4bc77c0-ee7d-422d-aabf-a4e6b977264e
  ```
  {: pre}


### bx cs logging-config-update CLUSTER --id LOG_CONFIG_ID [--namespace NAMESPACE][--hostname LOG_SERVER_HOSTNAME_OR_IP] [--port LOG_SERVER_PORT][--space CLUSTER_SPACE] [--org CLUSTER_ORG] --type LOG_TYPE [--json][--skipValidation]
{: #cs_logging_update}

Actualizar los detalles de una configuración de reenvío de registros.

<strong>Opciones del mandato</strong>:

<dl>
  <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>
  <dt><code>--id <em>LOG_CONFIG_ID</em></code></dt>
   <dd>El ID de configuración de registro que desea actualizar. Este valor es obligatorio.</dd>
  <dt><code>--namespace <em>NAMESPACE</em></code>
    <dd>El espacio de Kubernetes desde el que desea reenviar registros. El reenvío de registros no recibe soporte para los espacios de nombres de Kubernetes <code>ibm-system</code> y <code>kube-system</code>. Este valor sólo es válido para el origen de registro <code>container</code>. Si no especifica un espacio de nombres, todos los espacios de nombres del clúster utilizarán esta configuración.</dd>
  <dt><code>--hostname <em>LOG_SERVER_HOSTNAME</em></code></dt>
   <dd>Cuando el tipo de registro es <code>syslog</code>, el nombre de host o dirección IP del servidor del recopilador de registro. Este valor es obligatorio para <code>syslog</code>. Cuando el tipo de registro es <code>ibm</code>, el URL de ingestión de {{site.data.keyword.loganalysislong_notm}}. Puede encontrar la lista de URL de ingestión disponible [aquí](/docs/services/CloudLogAnalysis/log_ingestion.html#log_ingestion_urls). Si no especifica un URL de ingestión, se utiliza el punto final de la región en la que se ha creado el clúster.</dd>
   <dt><code>--port <em>LOG_SERVER_PORT</em></code></dt>
   <dd>El puerto del servidor del recopilador de registro. Este valor es opcional cuando el tipo de registro es <code>syslog</code>. Si no especifica un puerto, se utiliza el puerto estándar <code>514</code> para <code>syslog</code> y el <code>9091</code> para <code>ibm</code>.</dd>
   <dt><code>--space <em>CLUSTER_SPACE</em></code></dt>
   <dd>El nombre del espacio al que desea enviar registros. Este valor sólo es válido para el registro de tipo <code>ibm</code> y es opcional. Si no especifica un espacio, los registros se envían al nivel de cuenta.</dd>
   <dt><code>--org <em>CLUSTER_ORG</em></code></dt>
   <dd>El nombre de la organización en la que está el espacio. Este valor sólo es válido para el registro de tipo <code>ibm</code> y es necesario si ha especificado un espacio.</dd>
   <dt><code>--app-paths</code></dt>
     <dd>Omite la validación de los nombres de espacio y organización cuando se especifican. Al omitir la validación, disminuye el tiempo de proceso, pero si la configuración de registro no es válida, los registros no se reenviarán correctamente. Este valor es opcional.</dd>
   <dt><code>--app-containers</code></dt>
     <dd>La vía de acceso de los contenedores en la que registran las apps. Para reenviar registros con el tipo de origen <code>application</code>, debe proporcionar una vía de acceso. Para especificar más de una vía de acceso, utilice una lista separada por comas. Ejemplo: <code>/var/log/myApp1/&ast;,/var/log/myApp2/&ast;</code></dd>
   <dt><code>--type <em>LOG_TYPE</em></code></dt>
   <dd>El protocolo de reenvío de registros que desea utilizar. Actualmente se da soporte a <code>syslog</code> e <code>ibm</code>. Este valor es obligatorio.</dd>
   <dt><code>--json</code></dt>
   <dd>Opcionalmente, imprime la salida del mandato en formato JSON.</dd>
   <dt><code>--skipValidation</code></dt>
   <dd>Omite la validación de los nombres de espacio y organización cuando se especifican. Al omitir la validación, disminuye el tiempo de proceso, pero si la configuración de registro no es válida, los registros no se reenviarán correctamente. Este valor es opcional.</dd>
   </dl>

**Ejemplo de registro de tipo `ibm`**:

  ```
  bx cs logging-config-update my_cluster --id f4bc77c0-ee7d-422d-aabf-a4e6b977264e --type ibm
  ```
  {: pre}

**Ejemplo de registro de tipo `syslog`**:

  ```
  bx cs logging-config-update my_cluster --id f4bc77c0-ee7d-422d-aabf-a4e6b977264e --hostname localhost --port 5514 --type syslog
  ```
  {: pre}


### bx cs logging-filter-create CLUSTER --type LOG_TYPE [--logging-configs CONFIGS][--namespace KUBERNETES_NAMESPACE] [--container CONTAINER_NAME][--level LOGGING_LEVEL] [--message MESSAGE][--s] [--json]
{: #cs_log_filter_create}

Crea un filtro de registro. Utilice este mandato para filtrar los registros que su configuración de registro reenvía. 

<strong>Opciones del mandato</strong>:

<dl>
  <dt><code><em>CLUSTER</em></code></dt>
    <dd>Obligatorio: Nombre o ID de clúster que desea para crear un filtro de registro. </dd>
  <dt><code>--type <em>LOG_TYPE</em></code></dt>
    <dd>Tipo de registro al que aplicar el filtro. Actualmente se da soporte a <code>all</code>, <code>container</code> y <code>host</code>. </dd>
  <dt><code>--logging-configs <em>CONFIGS</em></code></dt>
    <dd>Opcional: Una lista separada por comas de los ID de configuración de registro. Si no se proporciona, el filtro se aplica a todas las configuraciones de registro de clúster que se pasan al filtro. Puede ver las configuraciones de registro que coinciden con el filtro utilizando con el mandato el distintivo <code>--show-matching-configs</code>. </dd>
  <dt><code>--namespace <em>KUBERNETES_NAMESPACE</em></code></dt>
    <dd>Opcional: Espacio de nombres de Kubernetes para el que desea filtrar registros. </dd>
  <dt><code>--container <em>CONTAINER_NAME</em></code></dt>
    <dd>Opcional: Nombre del contenedor desde el que desea filtrar registros. Este distintivo sólo se aplica cuando se utiliza el tipo de registro de <code>container</code>. </dd>
  <dt><code>--level <em>LOGGING_LEVEL</em></code></dt>
    <dd>Opcional: Filtra los registros en el nivel especificado y en los inferiores. Valores aceptables en su orden canónico son <code>fatal</code>, <code>error</code>, <code>warn/warning</code>, <code>info</code>, <code>debug</code> y <code>trace</code>. Por ejemplo, si filtra registros al nivel <code>info</code>, también se filtran los niveles <code>debug</code> y <code>trace</code>. **Nota**: Puede utilizar este distintivo sólo cuando los mensajes de registro están en formato JSON y contienen un campo de nivel. Salida de ejemplo:
<code>{"log": "hello", "level": "info"}</code></dd>
  <dt><code>--message <em>MESSAGE</em></code></dt>
    <dd>Opcional: Filtra los registros que contienen un mensaje concreto en el registro. La coincidencia del mensaje se realiza de forma literal y no como una expresión. Ejemplo: Los mensajes "Hello", "!" y "Hello, World!", se aplicarían al registro "Hello, World!".</dd>
  <dt><code>--json</code></dt>
    <dd>Opcional: Imprime la salida del mandato en formato JSON.</dd>
</dl>

**Ejemplos**:

Este ejemplo filtra todos los registros reenviados desde contenedores con el nombre `test-container` en el espacio de nombres predeterminado que se encuentren en el nivel debug o inferior con un mensaje que contenga "GET request". 

  ```
  bx cs logging-filter-create example-cluster --type container --namespace default --container test-container --level debug --message "GET request"
  ```
  {: pre}

Este ejemplo filtra todos los registros que se reenvían, en un nivel info o inferior, desde un clúster específico. La salida se devuelve como JSON.

  ```
  bx cs logging-filter-create example-cluster --type all --level info --json
  ```
  {: pre}

### bx cs logging-filter-update CLUSTER --type LOG_TYPE [--logging-configs CONFIGS][--namespace KUBERNETES_NAMESPACE] [--container CONTAINER_NAME][--level LOGGING_LEVEL] [--message MESSAGE][--s] [--json]
{: #cs_log_filter_update}

Actualiza un filtro de registro. Utilice este mandato para actualizar un filtro de registro que haya creado.

<strong>Opciones del mandato</strong>:

<dl>
  <dt><code><em>CLUSTER</em></code></dt>
    <dd>Obligatorio: Nombre o ID de clúster que desea para actualizar un filtro de registro. </dd>
  <dt><code>--type <em>LOG_TYPE</em></code></dt>
    <dd>Tipo de registro al que aplicar el filtro. Actualmente se da soporte a <code>all</code>, <code>container</code> y <code>host</code>. </dd>
  <dt><code>--logging-configs <em>CONFIGS</em></code></dt>
    <dd>Opcional: Una lista separada por comas de los ID de configuración de registro. Si no se proporciona, el filtro se aplica a todas las configuraciones de registro de clúster que se pasan al filtro. Puede ver las configuraciones de registro que coinciden con el filtro utilizando con el mandato el distintivo <code>--show-matching-configs</code>. </dd>
  <dt><code>--namespace <em>KUBERNETES_NAMESPACE</em></code></dt>
    <dd>Opcional: Espacio de nombres de Kubernetes para el que desea filtrar registros. </dd>
  <dt><code>--container <em>CONTAINER_NAME</em></code></dt>
    <dd>Opcional: Nombre del contenedor desde el que desea filtrar registros. Este distintivo sólo se aplica cuando se utiliza el tipo de registro de <code>container</code>. </dd>
  <dt><code>--level <em>LOGGING_LEVEL</em></code></dt>
    <dd>Opcional: Filtra los registros en el nivel especificado y en los inferiores. Valores aceptables en su orden canónico son <code>fatal</code>, <code>error</code>, <code>warn/warning</code>, <code>info</code>, <code>debug</code> y <code>trace</code>. Por ejemplo, si filtra registros al nivel <code>info</code>, también se filtran los niveles <code>debug</code> y <code>trace</code>. **Nota**: Puede utilizar este distintivo sólo cuando los mensajes de registro están en formato JSON y contienen un campo de nivel. Salida de ejemplo:
<code>{"log": "hello", "level": "info"}</code></dd>
  <dt><code>--message <em>MESSAGE</em></code></dt>
    <dd>Opcional: Filtra los registros que contienen un mensaje concreto en el registro. La coincidencia del mensaje se realiza de forma literal y no como una expresión. Ejemplo: Los mensajes "Hello", "!" y "Hello, World!", se aplicarían al registro "Hello, World!".</dd>
  <dt><code>--json</code></dt>
    <dd>Opcional: Imprime la salida del mandato en formato JSON.</dd>
</dl>


### bx cs logging-filter-get CLUSTER [--id FILTER_ID][--show-matching-configs] [--json]
{: #cs_log_filter_view}

Visualiza una configuración de filtro de registro. Utilice este mandato para visualizar los filtros de registro que haya creado. 

<strong>Opciones del mandato</strong>:

<dl>
  <dt><code><em>CLUSTER</em></code></dt>
    <dd>Obligatorio: Nombre o ID de clúster del que desea visualizar los filtros. </dd>
  <dt><code>--id <em>FILTER_ID</em></code></dt>
    <dd>ID del filtro de registro que desea visualizar. </dd>
  <dt><code>--show-matching-configs</code></dt>
    <dd>Opcional: Muestra las configuraciones de registro que coincidan con la configuración que está visualizando. </dd>
  <dt><code>--json</code></dt>
    <dd>Opcional: Imprime la salida del mandato en formato JSON.</dd>
</dl>


### bx cs logging-filter-rm CLUSTER [--id FILTER_ID][--json] [--all]
{: #cs_log_filter_delete}

Suprime un filtro de registro. Utilice este mandato para eliminar un filtro de registro que haya creado.

<strong>Opciones del mandato</strong>:

<dl>
  <dt><code><em>CLUSTER</em></code></dt>
    <dd>Nombre o ID del clúster del que desea suprimir un filtro. </dd>
  <dt><code>--id <em>FILTER_ID</em></code></dt>
    <dd>ID del filtro de registro que desea suprimir. </dd>
  <dt><code>--all</code></dt>
    <dd>Opcional: Suprimir todos filtros de reenvío de registro. </dd>
  <dt><code>--json</code></dt>
    <dd>Opcional: Imprime la salida del mandato en formato JSON.</dd>
</dl>

<br />


## Mandatos de región
{: #region_commands}

### bx cs locations
{: #cs_datacenters}

Ver una lista de las ubicaciones disponibles en las que puede crear un clúster.

<strong>Opciones del mandato</strong>:

   Ninguno

**Ejemplo**:

  ```
  bx cs locations
  ```
  {: pre}


### bx cs region
{: #cs_region}

Busque la región de {{site.data.keyword.containershort_notm}} en la que está actualmente. Puede crear y gestionar clústeres específicos para la región. Utilice el mandato `bx cs region-set` para cambiar regiones.

**Ejemplo**:

```
bx cs region
```
{: pre}

**Salida**:
```
Region: us-south
```
{: screen}

### bx cs region-set [REGION]
{: #cs_region-set}

Establezca la región para {{site.data.keyword.containershort_notm}}. Puede crear y gestionar clústeres específicos para la región, y es posible que desee clústeres en varias regiones para tener una alta disponibilidad.

Por ejemplo, puede iniciar una sesión en {{site.data.keyword.Bluemix_notm}} en la Región EE.UU. sur y crear un clúster. A continuación, puede utilizar `bx cs region-set eu-central` para establecer la región UE Central como destino y crear otro clúster. Por último, puede utilizar `bx cs region-set us-south` para volver a EE.UU. sur para gestionar el clúster en esa región.

**Opciones del mandato**:

<dl>
<dt><code><em>REGION</em></code></dt>
<dd>Especifique la región que desea establecer como destino. Este valor es opcional. Si no indica ninguna región, puede seleccionarla de la lista en la salida.

Para obtener una lista de regiones disponibles, consulte [regiones y ubicaciones](cs_regions.html) o utilice el [mandato](#cs_regions) `bx cs regions`.</dd></dl>

**Ejemplo**:

```
bx cs region-set eu-central
```
{: pre}

```
bx cs region-set
```
{: pre}

**Salida**:
```
Choose a region:
1. ap-north
2. ap-south
3. eu-central
4. uk-south
5. us-east
6. us-south
Enter a number> 3
OK
```
{: screen}

### bx cs regions
{: #cs_regions}

Lista las regiones disponibles. `Region Name` es el nombre de {{site.data.keyword.containershort_notm}} y `Region Alias` es el nombre de {{site.data.keyword.Bluemix_notm}} general para la región.

**Ejemplo**:

```
bx cs regions
```
{: pre}

**Salida**:
```
Region Name   Region Alias
ap-north      jp-tok
ap-south      au-syd
eu-central    eu-de
uk-south      eu-gb
us-east       us-east
us-south      us-south
```
{: screen}


<br />


## Mandatos de nodo trabajador
{: worker_node_commands}



### bx cs worker-add --cluster CLUSTER [--file FILE_LOCATION][--hardware HARDWARE] --machine-type MACHINE_TYPE --number NUMBER --private-vlan PRIVATE_VLAN --public-vlan PUBLIC_VLAN [--disable-disk-encrypt]
{: #cs_worker_add}

Añadir nodos trabajadores al clúster estándar.

<strong>Opciones del mandato</strong>:

<dl>
<dt><code>--cluster <em>CLUSTER</em></code></dt>
<dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

<dt><code>--file <em>FILE_LOCATION</em></code></dt>
<dd>La vía de acceso al archivo YAML para añadir nodos trabajadores a su clúster. En lugar de definir los nodos trabajadores adicionales mediante las opciones que se proporcionan en este mandato, puede utilizar un archivo YAML. Este valor es opcional.

<p><strong>Nota:</strong> Si especifica la misma opción en el mandato y como parámetro en el archivo YAML, el valor en el mandato prevalece sobre el valor del archivo YAML. Por ejemplo, supongamos que define un tipo de máquina en el archivo YAML y utiliza la opción --machine-type en el mandato; el valor que especifique en la opción del mandato prevalece sobre el valor del archivo YAML.

<pre class="codeblock">
<code>name: <em>&lt;cluster_name_or_ID&gt;</em>
location: <em>&lt;location&gt;</em>
machine-type: <em>&lt;machine_type&gt;</em>
private-vlan: <em>&lt;private_VLAN&gt;</em>
public-vlan: <em>&lt;public_VLAN&gt;</em>
hardware: <em>&lt;shared_or_dedicated&gt;</em>
workerNum: <em>&lt;number_workers&gt;</em>
diskEncryption: <em>false</em></code></pre>

<table>
<caption>Tabla 2. Visión general de los componentes del archivo YAML</caption>
<thead>
<th colspan=2><img src="images/idea.png" alt="Icono Idea"/> Visión general de los componentes del archivo YAML</th>
</thead>
<tbody>
<tr>
<td><code><em>name</em></code></td>
<td>Sustituya <code><em>&lt;cluster_name_or_ID&gt;</em></code> por el nombre o ID del clúster donde desea añadir nodos trabajadores.</td>
</tr>
<tr>
<td><code><em>location</em></code></td>
<td>Sustituya <code><em>&lt;location&gt;</em></code> por la ubicación de despliegue de los nodos trabajadores. Las ubicaciones disponibles dependen de la región en la que ha iniciado la sesión. Para ver una lista de las ubicaciones disponibles, ejecute <code>cs bx ubicaciones</code>.</td>
</tr>
<tr>
<td><code><em>machine-type</em></code></td>
<td>Sustituya <code><em>&lt;machine_type&gt;</em></code> por el tipo de máquina en el que desea desplegar los nodos trabajadores. Puede desplegar los nodos trabajadores como máquinas virtuales en hardware dedicado o compartido, o como máquinas físicas en servidores nativos. Los tipos de máquinas físicas y virtuales varían según la ubicación en la que se despliega el clúster. Para obtener más información, consulte el [mandato](cs_cli_reference.html#cs_machine_types) `bx cs machine-types`. </td>
</tr>
<tr>
<td><code><em>private-vlan</em></code></td>
<td>Sustituya <code><em>&lt;private_VLAN&gt;</em></code> por el ID de la VLAN privada que desea utilizar para sus nodos trabajadores. Para ver una lista de las VLAN disponibles, ejecute <code>bx cs vlans <em>&lt;location&gt;</em></code> y busque direccionadores de VLAN que empiecen por <code>bcr</code> ("back-end router", direccionador de fondo).</td>
</tr>
<tr>
<td><code>public-vlan</code></td>
<td>Sustituya <code>&lt;public_VLAN&gt;</code> por el ID de la VLAN pública que desea utilizar para sus nodos trabajadores. Para ver una lista de las VLAN disponibles, ejecute <code>bx cs vlans &lt;location&gt;</code> y busque direccionadores de VLAN que empiecen por <code>fcr</code> ("front-end router", direccionador frontal). <br><strong>Nota</strong>: {[private_VLAN_vyatta]}</td>
</tr>
<tr>
<td><code>hardware</code></td>
<td>Para tipos de máquina virtual: El nivel de aislamiento del hardware del nodo trabajador. Utilice el valor dedicated si desea tener recursos físicos disponibles dedicados solo a usted, o el valor shared para permitir que los recursos físicos se compartan con otros clientes de IBM. El valor predeterminado es shared.</td>
</tr>
<tr>
<td><code>workerNum</code></td>
<td>Sustituya <code><em>&lt;number_workers&gt;</em></code> por el número de nodos trabajadores que desea desplegar.</td>
</tr>
<tr>
<td><code>diskEncryption: <em>false</em></code></td>
<td>Los nodos trabajadores tienen cifrado de disco de forma predeterminada; [más información](cs_secure.html#worker). Para inhabilitar el cifrado, incluya esta opción y establezca el valor en <code>false</code>.</td></tr>
</tbody></table></p></dd>

<dt><code>--hardware <em>HARDWARE</em></code></dt>
<dd>El nivel de aislamiento del hardware del nodo trabajador. Utilice el valor dedicated si desea tener recursos físicos disponibles dedicados solo a usted, o el valor shared para permitir que los recursos físicos se compartan con otros clientes de IBM. El valor predeterminado es shared. Este valor es opcional.</dd>

<dt><code>--machine-type <em>MACHINE_TYPE</em></code></dt>
<dd>Elija un tipo de máquina. Puede desplegar los nodos trabajadores como máquinas virtuales en hardware dedicado o compartido, o como máquinas físicas en servidores nativos. Los tipos de máquinas físicas y virtuales varían según la ubicación en la que se despliega el clúster. Para obtener más información, consulte la documentación del [mandato](cs_cli_reference.html#cs_machine_types) `bx cs machine-types`. Este valor es obligatorio para clústeres estándares y no está disponible para clústeres gratuitos.</dd>

<dt><code>--number <em>NUMBER</em></code></dt>
<dd>Un entero que representa el número de nodos trabajadores que desea crear en el clúster. El valor predeterminado es 1. Este valor es opcional.</dd>

<dt><code>--private-vlan <em>PRIVATE_VLAN</em></code></dt>
<dd>La VLAN privada que se ha especificado al crear el clúster. Este valor es obligatorio.

<p><strong>Nota:</strong> {[matching_VLANs]}</p></dd>

<dt><code>--public-vlan <em>PUBLIC_VLAN</em></code></dt>
<dd>La VLAN pública que se ha especificado al crear el clúster. Este valor es opcional. Si desea que los nodos trabajadores existan solo en una VLAN privada, no proporcione ningún ID de VLAN pública. <strong>Nota</strong>: {[private_VLAN_vyatta]}

<p><strong>Nota:</strong> {[matching_VLANs]}</p></dd>

<dt><code>--disable-disk-encrypt</code></dt>
<dd>Los nodos trabajadores tienen cifrado de disco de forma predeterminada; [más información](cs_secure.html#worker). Para inhabilitar el cifrado, incluya esta opción.</dd>
</dl>

**Ejemplos**:

  ```
  bx cs worker-add --cluster my_cluster --number 3 --public-vlan my_public_VLAN_ID --private-vlan my_private_VLAN_ID --machine-type u2c.2x4 --hardware shared
  ```
  {: pre}

  Ejemplo para {{site.data.keyword.Bluemix_dedicated_notm}}:

  ```
  bx cs worker-add --cluster my_cluster --number 3 --machine-type u2c.2x4
  ```
  {: pre}




### bx cs worker-get [CLUSTER_NAME_OR_ID] WORKER_NODE_ID
{: #cs_worker_get}

Visualiza los detalles de un nodo trabajador.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER_NAME_OR_ID</em></code></dt>
   <dd>El nombre o ID del clúster del nodo trabajador. Este valor es opcional.</dd>
   <dt><code><em>WORKER_NODE_ID</em></code></dt>
   <dd>El nombre del nodo trabajador. Ejecute <code>bx cs workers <em>CLUSTER</em></code> para ver los ID de los nodos
trabajadores de un clúster. Este valor es obligatorio.</dd>
   </dl>

**Mandato de ejemplo**:

  ```
  bx cs worker-get my_cluster kube-dal10-cr18a61a63a6a94b658596aa93d087aaa9-w1
  ```
  {: pre}

**Salida de ejemplo**:

  ```
  ID:           kube-dal10-123456789-w1
  State:        normal
  Status:       Ready
  Trust:        disabled
  Private VLAN: 223xxxx
  Public VLAN:  223xxxx
  Private IP:   10.xxx.xx.xxx
  Public IP:    169.xx.xxx.xxx
  Hardware:     shared
  Zone:         dal10
  Version:      1.8.11_1509
  ```
  {: screen}

### bx cs worker-reboot [-f][--hard] CLUSTER WORKER [WORKER]
{: #cs_worker_reboot}

Rearrancar un nodo trabajador de un clúster. Durante el rearranque, el estado del nodo trabajador no cambia.

**Atención:** Rearrancar un nodo trabajador puede provocar que se corrompan los datos en el nodo trabajador. Utilice este mandato con precaución y cuando sepa que el rearranque puede ayudar a recuperar el nodo trabajador. En todos los demás casos, [recargue el nodo trabajador](#cs_worker_reload) en su lugar.

Antes de rearrancar el nodo trabajador, asegúrese de que los pods se vuelven a programar en otros nodos trabajadores para evitar el tiempo de inactividad de la app o la corrupción de los datos en el nodo trabajador.

1. Liste todos los nodos trabajadores del clúster y anote el **nombre** del nodo trabajador que desea rearrancar.
   ```
   kubectl get nodes
   ```
   El **nombre** que se devuelve en este mandato es la dirección IP privada que se asigna al nodo trabajador. Puede encontrar más información sobre el nodo trabajador ejecutando el mandato `bx cs workers <cluster_name_or_ID>` y buscando el nodo trabajador con la misma dirección **IP privada**.
2. Marque el nodo trabajador como no programable en un proceso que se conoce como acordonamiento. Cuando se acordona un nodo trabajador, deja de estar disponible para programar pods en el futuro. Utilice el **nombre** del nodo trabajador que ha recuperado en el paso anterior.
   ```
   kubectl cordon <worker_name>
   ```
   {: pre}

3. Verifique que la programación de pods está inhabilitada en el nodo trabajador.
   ```
   kubectl get nodes
   ```
   {: pre}
   La programación de pods está inhabilitada en el nodo trabajador si el estado es **SchedulingDisabled**.
 4. Fuerce la eliminación de los pods del nodo trabajador y vuelva a programarlos en los demás nodos trabajadores del clúster.
    ```
    kubectl drain <worker_name>
    ```
    {: pre}
    Este proceso puede tardar unos minutos.
 5. Rearranque el nodo trabajador. Utilice el ID de trabajador que se devuelve del mandato `bx cs workers <cluster_name_or_ID>`.
    ```
    bx cs worker-reboot <cluster_name_or_ID> <worker_name_or_ID>
    ```
    {: pre}
 6. Espere unos 5 minutos antes de volver a permitir la programación de pods en el nodo de trabajador para asegurarse de que finalice el rearranque. Durante el rearranque, el estado del nodo trabajador no cambia. Por lo general, el rearranque de un nodo trabajador se realiza en pocos segundos.
 7. Permita la programación de pods en el nodo de trabajador. Utilice el **nombre** del nodo trabajador que se devuelve del mandato `kubectl get nodes`.
    ```
    kubectl uncordon <worker_name>
    ```
    {: pre}
    </br>

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code>-f</code></dt>
   <dd>Utilice esta opción para forzar el reinicio de un nodo trabajador sin solicitudes de usuario. Este valor es opcional.</dd>

   <dt><code>--hard</code></dt>
   <dd>Utilice esta opción para forzar un reinicio de un nodo trabajador, cortando el suministro eléctrico al nodo trabajador. Utilice esta opción si el nodo trabajador no responde o si tiene un bloqueo de Docker. Este valor es opcional.</dd>

   <dt><code><em>WORKER</em></code></dt>
   <dd>El nombre o ID de uno o varios nodos trabajadores. Utilice un espacio para ver una lista de varios nodos trabajadores. Este valor es obligatorio.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs worker-reboot my_cluster kube-dal10-cr18a61a63a6a94b658596aa93d087aaa9-w1 kube-dal10-cr18a61a63a6a94b658596aa93d087aaa9-w2
  ```
  {: pre}


### bx cs worker-reload [-f] CLUSTER WORKER [WORKER]
{: #cs_worker_reload}

Recargue todas las configuraciones necesarias para un nodo trabajador. Una recarga puede ser útil si el nodo trabajador tiene problemas, como un rendimiento lento, o si queda bloqueado en un estado incorrecto.

Al recargar un nodo trabajador no se aplican las últimas actualizaciones, parches de seguridad ni la [versión de Kubernetes](cs_versions.html#version_types). Cuando haya disponibles actualizaciones de parches o de versión, se le solicitará en la CLI y la consola al utilizar características relacionadas con los nodos trabajadores. Para mantener actualizados los nodos trabajadores, utilice de forma periódica el [mandato](cs_cli_reference.html#cs_worker_update) `bx cs worker-update`.
{: tip}

Antes de recargar el nodo trabajador, asegúrese de que los pods se vuelven a programar en otros nodos trabajadores para evitar el tiempo de inactividad de la app o la corrupción de los datos en el nodo trabajador.

1. Liste todos los nodos trabajadores del clúster y anote el **nombre** del nodo trabajador que desea recargar.
   ```
   kubectl get nodes
   ```
   El **nombre** que se devuelve en este mandato es la dirección IP privada que se asigna al nodo trabajador. Puede encontrar más información sobre el nodo trabajador ejecutando el mandato `bx cs workers <cluster_name_or_ID>` y buscando el nodo trabajador con la misma dirección **IP privada**.
2. Marque el nodo trabajador como no programable en un proceso que se conoce como acordonamiento. Cuando se acordona un nodo trabajador, deja de estar disponible para programar pods en el futuro. Utilice el **nombre** del nodo trabajador que ha recuperado en el paso anterior.
   ```
   kubectl cordon <worker_name>
   ```
   {: pre}

3. Verifique que la programación de pods está inhabilitada en el nodo trabajador.
   ```
   kubectl get nodes
   ```
   {: pre}
   La programación de pods está inhabilitada en el nodo trabajador si el estado es **SchedulingDisabled**.
 4. Fuerce la eliminación de los pods del nodo trabajador y vuelva a programarlos en los demás nodos trabajadores del clúster.
    ```
    kubectl drain <worker_name>
    ```
    {: pre}
    Este proceso puede tardar unos minutos.
 5. Recargue el nodo trabajador. Utilice el ID de trabajador que se devuelve del mandato `bx cs workers <cluster_name_or_ID>`.
    ```
    bx cs worker-reload <cluster_name_or_ID> <worker_name_or_ID>
    ```
    {: pre}
 6. Espere a que finalice la recarga.
 7. Permita la programación de pods en el nodo de trabajador. Utilice el **nombre** del nodo trabajador que se devuelve del mandato `kubectl get nodes`.
    ```
    kubectl uncordon <worker_name>
    ```
</br>
<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code>-f</code></dt>
   <dd>Utilice esta opción para forzar que se vuelva a cargar un nodo trabajador sin solicitudes de usuario. Este valor es opcional.</dd>

   <dt><code><em>WORKER</em></code></dt>
   <dd>El nombre o ID de uno o varios nodos trabajadores. Utilice un espacio para ver una lista de varios nodos trabajadores. Este valor es obligatorio.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs worker-reload my_cluster kube-dal10-cr18a61a63a6a94b658596aa93d087aaa9-w1 kube-dal10-cr18a61a63a6a94b658596aa93d087aaa9-w2
  ```
  {: pre}


### bx cs worker-rm [-f] CLUSTER WORKER [WORKER]
{: #cs_worker_rm}

Eliminar uno o varios nodos trabajadores de un clúster. Si elimina un nodo trabajador, el clúster se desequilibra. 

Antes de eliminar el nodo trabajador, asegúrese de que los pods se vuelven a programar en otros nodos trabajadores para evitar el tiempo de inactividad de la app o la corrupción de los datos en el nodo trabajador.
{: tip}

1. Liste todos los nodos trabajadores del clúster y anote el **nombre** del nodo trabajador que desea eliminar.
   ```
   kubectl get nodes
   ```
   El **nombre** que se devuelve en este mandato es la dirección IP privada que se asigna al nodo trabajador. Puede encontrar más información sobre el nodo trabajador ejecutando el mandato `bx cs workers <cluster_name_or_ID>` y buscando el nodo trabajador con la misma dirección **IP privada**.
2. Marque el nodo trabajador como no programable en un proceso que se conoce como acordonamiento. Cuando se acordona un nodo trabajador, deja de estar disponible para programar pods en el futuro. Utilice el **nombre** del nodo trabajador que ha recuperado en el paso anterior.
   ```
   kubectl cordon <worker_name>
   ```
   {: pre}

3. Verifique que la programación de pods está inhabilitada en el nodo trabajador.
   ```
   kubectl get nodes
   ```
   {: pre}
   La programación de pods está inhabilitada en el nodo trabajador si el estado es **SchedulingDisabled**.
4. Fuerce la eliminación de los pods del nodo trabajador y vuelva a programarlos en los demás nodos trabajadores del clúster.
   ```
   kubectl drain <worker_name>
   ```
   {: pre}
   Este proceso puede tardar unos minutos.
5. Elimine el nodo trabajador. Utilice el ID de trabajador que se devuelve del mandato `bx cs workers <cluster_name_or_ID>`.
   ```
   bx cs worker-rm <cluster_name_or_ID> <worker_name_or_ID>
   ```
   {: pre}

6. Verifique que se ha eliminado el nodo trabajador.
   ```
   bx cs workers <cluster_name_or_ID>
   ```
</br>
<strong>Opciones del mandato</strong>:

   <dl>
   <dt><code><em>CLUSTER</em></code></dt>
   <dd>El nombre o ID del clúster. Este valor es obligatorio.</dd>

   <dt><code>-f</code></dt>
   <dd>Utilice esta opción para forzar la eliminación de un nodo trabajador sin solicitudes de usuario. Este valor es opcional.</dd>

   <dt><code><em>WORKER</em></code></dt>
   <dd>El nombre o ID de uno o varios nodos trabajadores. Utilice un espacio para ver una lista de varios nodos trabajadores. Este valor es obligatorio.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs worker-rm my_cluster kube-dal10-cr18a61a63a6a94b658596aa93d087aaa9-w1 kube-dal10-cr18a61a63a6a94b658596aa93d087aaa9-w2
  ```
  {: pre}




### bx cs worker-update [-f] CLUSTER WORKER [WORKER][--kube-version MAJOR.MINOR.PATCH] [--force-update]
{: #cs_worker_update}

Actualiza los nodos trabajadores para aplicar las últimas actualizaciones y parches de seguridad para el sistema operativo, y para actualizar la versión de Kubernetes para que coincida con la versión del nodo maestro. Puede actualizar la versión de Kubernetes del nodo maestro con el [command](cs_cli_reference.html#cs_cluster_update) `bx cs cluster-update`.


**Importante**: La ejecución de `bx cs worker-update` puede causar un tiempo de inactividad para sus apps y servicios. Durante la actualización, todos los pods se vuelven a planificar en otros nodos trabajadores y los datos se suprimen si no se guardan fuera del pod. Para evitar el tiempo de inactividad, [asegúrese de tener suficientes nodos trabajadores para manejar la carga de trabajo mientras se estén actualizando los nodos trabajadores seleccionados](cs_cluster_update.html#worker_node).

Es posible que tenga que modificar los archivos YAML para futuros despliegues antes de la actualización. Revise esta [nota del release](cs_versions.html) para ver detalles.

<strong>Opciones del mandato</strong>:

   <dl>

   <dt><em>CLUSTER</em></dt>
   <dd>El nombre o ID del clúster en el que se listan los nodos trabajadores disponibles. Este valor es obligatorio.</dd>

   <dt><code>-f</code></dt>
   <dd>Utilice esta opción para forzar la actualización del maestro sin solicitudes de usuario. Este valor es opcional.</dd>

   <dt><code>--force-update</code></dt>
   <dd>Intente la actualización incluso si el cambio es superior a dos versiones anteriores. Este valor es opcional.</dd>

   <dt><code><em>WORKER</em></code></dt>
   <dd>El ID de uno o varios nodos trabajadores. Utilice un espacio para ver una lista de varios nodos trabajadores. Este valor es obligatorio.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs worker-update my_cluster kube-dal10-cr18a61a63a6a94b658596aa93d087aaa9-w1 kube-dal10-cr18a61a63a6a94b658596aa93d087aaa9-w2
  ```
  {: pre}



### bx cs workers CLUSTER [--show-deleted]
{: #cs_workers}

Ver una lista de los nodos trabajadores y el estado de cada uno de ellos en un clúster.

<strong>Opciones del mandato</strong>:

   <dl>
   <dt><em>CLUSTER</em></dt>
   <dd>El nombre o ID del clúster en el que se listan los nodos trabajadores disponibles. Este valor es obligatorio.</dd>
   <dt><em>--show-deleted</em></dt>
   <dd>Visualiza los nodos trabajadores que se han suprimido del clúster, incluido el motivo de la supresión. Este valor es opcional.</dd>
   </dl>

**Ejemplo**:

  ```
  bx cs workers my_cluster
  ```
  {: pre}

