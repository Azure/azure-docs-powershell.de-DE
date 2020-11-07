---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 5fd06ad41e6fafe629ba50166650dd3d8766d29c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658285"
---
# <span data-ttu-id="50016-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="50016-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="50016-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50016-102">SYNOPSIS</span></span>
<span data-ttu-id="50016-103">Importiert eine API aus einer Datei oder einer URL.</span><span class="sxs-lookup"><span data-stu-id="50016-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="50016-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50016-104">SYNTAX</span></span>

### <span data-ttu-id="50016-105">ImportFromLocalFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="50016-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50016-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="50016-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50016-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50016-107">DESCRIPTION</span></span>
<span data-ttu-id="50016-108">Das Cmdlet " **Import-AzApiManagementApi** " importiert eine Azure API-Verwaltungs-API aus einer Datei oder einer URL in Web Application Description Language (WADL), Web Services Description Language (WSDL) oder Prahlerei-Format.</span><span class="sxs-lookup"><span data-stu-id="50016-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="50016-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50016-109">EXAMPLES</span></span>

### <span data-ttu-id="50016-110">Beispiel 1 Importieren einer API aus einer WADL-Datei</span><span class="sxs-lookup"><span data-stu-id="50016-110">Example 1 Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="50016-111">Dieser Befehl importiert eine API aus der angegebenen WADL-Datei.</span><span class="sxs-lookup"><span data-stu-id="50016-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="50016-112">Beispiel 2 Importieren einer API aus einer Prahlerei-Datei</span><span class="sxs-lookup"><span data-stu-id="50016-112">Example 2 Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="50016-113">Dieser Befehl importiert eine API aus der angegebenen Prahlerei-Datei.</span><span class="sxs-lookup"><span data-stu-id="50016-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="50016-114">Beispiel 3: Importieren einer API aus einem WADL-Link</span><span class="sxs-lookup"><span data-stu-id="50016-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="50016-115">Dieser Befehl importiert eine API aus dem angegebenen WADL-Link.</span><span class="sxs-lookup"><span data-stu-id="50016-115">This command imports an API from the specified WADL link.</span></span>

### <span data-ttu-id="50016-116">Beispiel 4: Importieren einer API aus einem geöffneten API-Link</span><span class="sxs-lookup"><span data-stu-id="50016-116">Example 4: Import an API from a Open Api Link</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationFormat OpenApi -SpecificationUrl https://raw.githubusercontent.com/OAI/OpenAPI-Specification/master/examples/v3.0/petstore.yaml -Path "petstore30"

ApiId                         : af3f57bab399455aa875d7050654e9d1
Name                          : Swagger Petstore
Description                   :
ServiceUrl                    : http://petstore.swagger.io/v1
Path                          : petstore30
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    :
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/af3f57bab399455aa875d7050654e9d1     
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="50016-117">Dieser Befehl importiert eine API aus dem angegebenen Open 3,0-Spezifikations Link.</span><span class="sxs-lookup"><span data-stu-id="50016-117">This command imports an API from the specified Open 3.0 specification link.</span></span>

### <span data-ttu-id="50016-118">Beispiel 5: Importieren einer API aus einem geöffneten API-Link in einen ApiVersion-Satz</span><span class="sxs-lookup"><span data-stu-id="50016-118">Example 5:  Import an API from a Open Api Link into a ApiVersion Set</span></span>

```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationPath "C:\contoso\specifications\uspto.yml" -SpecificationFormat OpenApi -Path uspostal -ApiVersionSetId 0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd -ApiVersion v2

ApiId                         : 6c3f20c66e5745b19229d06cd865948f
Name                          : USPTO Data Set API
Description                   : The Data Set API (DSAPI) allows the public users to discover and search USPTO exported data sets. This is a generic API that allows USPTO users to make any CSV based data files
                                searchable through API. With the help of GET call, it returns the list of data fields that are searchable. With the help of POST call, data can be fetched based on the filters on the    
                                field names. Please note that POST call is used to search the actual data. The reason for the POST call is that it allows users to specify any complex search criteria without worry      
                                about the GET size limitations as well as encoding of the input parameters.
ServiceUrl                    : https://developer.uspto.gov/ds-api
Path                          : uspostal
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v2
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd
Id                            : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis/6c3f20c66e5745b19229d06cd865948f    
ResourceGroupName             : Api-Default-East-US
ServiceName                   : contoso
```

<span data-ttu-id="50016-119">Dieser Befehl importiert eine API aus dem angegebenen geöffneten 3,0-Spezifikationsdokument und erstellt ein neues ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="50016-119">This command imports an API from the specified Open 3.0 specification document and create a new ApiVersion.</span></span>

## <span data-ttu-id="50016-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="50016-120">PARAMETERS</span></span>

### <span data-ttu-id="50016-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="50016-121">-ApiId</span></span>
<span data-ttu-id="50016-122">Gibt eine ID für die zu importierende API an.</span><span class="sxs-lookup"><span data-stu-id="50016-122">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="50016-123">Wenn Sie diesen Parameter nicht angeben, wird eine ID für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="50016-123">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50016-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="50016-124">-ApiRevision</span></span>
<span data-ttu-id="50016-125">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="50016-125">Identifier of API Revision.</span></span> <span data-ttu-id="50016-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="50016-126">This parameter is optional.</span></span> <span data-ttu-id="50016-127">Wenn nicht angegeben, wird der Import auf die aktuell aktive Revision oder eine neue API durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="50016-127">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50016-128">-ApiType</span><span class="sxs-lookup"><span data-stu-id="50016-128">-ApiType</span></span>
<span data-ttu-id="50016-129">Dieser Parameter ist optional mit dem Standardwert http.</span><span class="sxs-lookup"><span data-stu-id="50016-129">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="50016-130">Die SOAP-Option ist nur beim Importieren von WSDL anwendbar und erstellt eine SOAP-Passthrough-API.</span><span class="sxs-lookup"><span data-stu-id="50016-130">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50016-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="50016-131">-ApiVersion</span></span>
<span data-ttu-id="50016-132">API-Version der zu erstellende API.</span><span class="sxs-lookup"><span data-stu-id="50016-132">Api Version of the Api to create.</span></span> <span data-ttu-id="50016-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="50016-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50016-134">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="50016-134">-ApiVersionSetId</span></span>
<span data-ttu-id="50016-135">Ein Ressourcenbezeichner für den verknüpften API-Versions Satz.</span><span class="sxs-lookup"><span data-stu-id="50016-135">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="50016-136">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="50016-136">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50016-137">-Context</span><span class="sxs-lookup"><span data-stu-id="50016-137">-Context</span></span>
<span data-ttu-id="50016-138">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="50016-138">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50016-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50016-139">-DefaultProfile</span></span>
<span data-ttu-id="50016-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50016-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50016-141">-Path</span><span class="sxs-lookup"><span data-stu-id="50016-141">-Path</span></span>
<span data-ttu-id="50016-142">Gibt einen Web-API-Pfad als letzten Teil der öffentlichen URL der API an.</span><span class="sxs-lookup"><span data-stu-id="50016-142">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="50016-143">Diese URL wird von API-Consumern zum Senden von Anforderungen an den Webdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="50016-143">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="50016-144">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="50016-144">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="50016-145">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="50016-145">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50016-146">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="50016-146">-Protocol</span></span>
<span data-ttu-id="50016-147">Web-API-Protokolle (http, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="50016-147">Web API protocols (http, https).</span></span> <span data-ttu-id="50016-148">Protokolle, über die API zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="50016-148">Protocols over which API is made available.</span></span> <span data-ttu-id="50016-149">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="50016-149">This parameter is optional.</span></span> <span data-ttu-id="50016-150">Falls vorhanden, werden die im Spezifikationen-Dokument angegebenen Protokolle außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="50016-150">If provided it will override the protocols specified in the specifications document.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50016-151">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="50016-151">-ServiceUrl</span></span>
<span data-ttu-id="50016-152">Eine URL des Webdiensts, der die API verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="50016-152">A URL of the web service exposing the API.</span></span> <span data-ttu-id="50016-153">Diese URL wird nur von der Azure-API-Verwaltung verwendet und wird nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="50016-153">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="50016-154">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="50016-154">This parameter is optional.</span></span> <span data-ttu-id="50016-155">Wenn dies der Fall ist, wird die im Spezifikationen-Dokument angegebene serviceUrl außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="50016-155">If provided it will override the ServiceUrl specified in the Specifications document.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50016-156">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="50016-156">-SpecificationFormat</span></span>
<span data-ttu-id="50016-157">Gibt das Spezifikations Format an.</span><span class="sxs-lookup"><span data-stu-id="50016-157">Specifies the specification format.</span></span>
<span data-ttu-id="50016-158">psdx_paramvalues WADL, WSDL und Prahlerei.</span><span class="sxs-lookup"><span data-stu-id="50016-158">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50016-159">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="50016-159">-SpecificationPath</span></span>
<span data-ttu-id="50016-160">Gibt den Pfad der Spezifikationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="50016-160">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromLocalFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50016-161">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="50016-161">-SpecificationUrl</span></span>
<span data-ttu-id="50016-162">Gibt die Spezifikations-URL an.</span><span class="sxs-lookup"><span data-stu-id="50016-162">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50016-163">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="50016-163">-WsdlEndpointName</span></span>
<span data-ttu-id="50016-164">Lokaler Name des WSDL-Endpunkts (Port), der importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="50016-164">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="50016-165">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="50016-165">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="50016-166">Dieser Parameter ist optional und nur für den Import von WSDL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="50016-166">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="50016-167">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="50016-167">Default value is $null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50016-168">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="50016-168">-WsdlServiceName</span></span>
<span data-ttu-id="50016-169">Lokaler Name des zu importierenden WSDL-Diensts.</span><span class="sxs-lookup"><span data-stu-id="50016-169">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="50016-170">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="50016-170">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="50016-171">Dieser Parameter ist optional und nur für den Import von WSDL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="50016-171">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="50016-172">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="50016-172">Default value is $null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50016-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50016-173">CommonParameters</span></span>
<span data-ttu-id="50016-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50016-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50016-175">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50016-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50016-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50016-176">INPUTS</span></span>

### <span data-ttu-id="50016-177">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="50016-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="50016-178">System. String</span><span class="sxs-lookup"><span data-stu-id="50016-178">System.String</span></span>

### <span data-ttu-id="50016-179">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="50016-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="50016-180">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiType, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. Servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="50016-180">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="50016-181">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50016-181">OUTPUTS</span></span>

### <span data-ttu-id="50016-182">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="50016-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="50016-183">Notizen</span><span class="sxs-lookup"><span data-stu-id="50016-183">NOTES</span></span>

## <span data-ttu-id="50016-184">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50016-184">RELATED LINKS</span></span>

[<span data-ttu-id="50016-185">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="50016-185">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="50016-186">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="50016-186">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="50016-187">Neu – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="50016-187">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="50016-188">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="50016-188">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="50016-189">Satz-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="50016-189">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


