---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 690ebbfb1bb3cca6de8feb1f199068510e41f1d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650360"
---
# <span data-ttu-id="696c7-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="696c7-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="696c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="696c7-102">SYNOPSIS</span></span>
<span data-ttu-id="696c7-103">Importiert eine API aus einer Datei oder einer URL.</span><span class="sxs-lookup"><span data-stu-id="696c7-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="696c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="696c7-104">SYNTAX</span></span>

### <span data-ttu-id="696c7-105">ImportFromLocalFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="696c7-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="696c7-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="696c7-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="696c7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="696c7-107">DESCRIPTION</span></span>
<span data-ttu-id="696c7-108">Das Cmdlet " **Import-AzApiManagementApi** " importiert eine Azure API-Verwaltungs-API aus einer Datei oder einer URL in Web Application Description Language (WADL), Web Services Description Language (WSDL) oder Prahlerei-Format.</span><span class="sxs-lookup"><span data-stu-id="696c7-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="696c7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="696c7-109">EXAMPLES</span></span>

### <span data-ttu-id="696c7-110">Beispiel 1 Importieren einer API aus einer WADL-Datei</span><span class="sxs-lookup"><span data-stu-id="696c7-110">Example 1 Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="696c7-111">Dieser Befehl importiert eine API aus der angegebenen WADL-Datei.</span><span class="sxs-lookup"><span data-stu-id="696c7-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="696c7-112">Beispiel 2 Importieren einer API aus einer Prahlerei-Datei</span><span class="sxs-lookup"><span data-stu-id="696c7-112">Example 2 Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="696c7-113">Dieser Befehl importiert eine API aus der angegebenen Prahlerei-Datei.</span><span class="sxs-lookup"><span data-stu-id="696c7-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="696c7-114">Beispiel 3: Importieren einer API aus einem WADL-Link</span><span class="sxs-lookup"><span data-stu-id="696c7-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="696c7-115">Dieser Befehl importiert eine API aus dem angegebenen WADL-Link.</span><span class="sxs-lookup"><span data-stu-id="696c7-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="696c7-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="696c7-116">PARAMETERS</span></span>

### <span data-ttu-id="696c7-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="696c7-117">-ApiId</span></span>
<span data-ttu-id="696c7-118">Gibt eine ID für die zu importierende API an.</span><span class="sxs-lookup"><span data-stu-id="696c7-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="696c7-119">Wenn Sie diesen Parameter nicht angeben, wird eine ID für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="696c7-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="696c7-120">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="696c7-120">-ApiRevision</span></span>
<span data-ttu-id="696c7-121">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="696c7-121">Identifier of API Revision.</span></span> <span data-ttu-id="696c7-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="696c7-122">This parameter is optional.</span></span> <span data-ttu-id="696c7-123">Wenn nicht angegeben, wird der Import auf die aktuell aktive Revision oder eine neue API durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="696c7-123">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="696c7-124">-ApiType</span><span class="sxs-lookup"><span data-stu-id="696c7-124">-ApiType</span></span>
<span data-ttu-id="696c7-125">Dieser Parameter ist optional mit dem Standardwert http.</span><span class="sxs-lookup"><span data-stu-id="696c7-125">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="696c7-126">Die SOAP-Option ist nur beim Importieren von WSDL anwendbar und erstellt eine SOAP-Passthrough-API.</span><span class="sxs-lookup"><span data-stu-id="696c7-126">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="696c7-127">-Context</span><span class="sxs-lookup"><span data-stu-id="696c7-127">-Context</span></span>
<span data-ttu-id="696c7-128">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="696c7-128">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696c7-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696c7-129">-DefaultProfile</span></span>
<span data-ttu-id="696c7-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="696c7-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="696c7-131">-Path</span><span class="sxs-lookup"><span data-stu-id="696c7-131">-Path</span></span>
<span data-ttu-id="696c7-132">Gibt einen Web-API-Pfad als letzten Teil der öffentlichen URL der API an.</span><span class="sxs-lookup"><span data-stu-id="696c7-132">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="696c7-133">Diese URL wird von API-Consumern zum Senden von Anforderungen an den Webdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="696c7-133">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="696c7-134">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="696c7-134">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="696c7-135">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="696c7-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="696c7-136">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="696c7-136">-SpecificationFormat</span></span>
<span data-ttu-id="696c7-137">Gibt das Spezifikations Format an.</span><span class="sxs-lookup"><span data-stu-id="696c7-137">Specifies the specification format.</span></span>
<span data-ttu-id="696c7-138">psdx_paramvalues WADL, WSDL und Prahlerei.</span><span class="sxs-lookup"><span data-stu-id="696c7-138">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696c7-139">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="696c7-139">-SpecificationPath</span></span>
<span data-ttu-id="696c7-140">Gibt den Pfad der Spezifikationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="696c7-140">Specifies the specification file path.</span></span>

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

### <span data-ttu-id="696c7-141">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="696c7-141">-SpecificationUrl</span></span>
<span data-ttu-id="696c7-142">Gibt die Spezifikations-URL an.</span><span class="sxs-lookup"><span data-stu-id="696c7-142">Specifies the specification URL.</span></span>

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

### <span data-ttu-id="696c7-143">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="696c7-143">-WsdlEndpointName</span></span>
<span data-ttu-id="696c7-144">Lokaler Name des WSDL-Endpunkts (Port), der importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="696c7-144">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="696c7-145">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="696c7-145">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="696c7-146">Dieser Parameter ist optional und nur für den Import von WSDL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="696c7-146">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="696c7-147">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="696c7-147">Default value is $null.</span></span>

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

### <span data-ttu-id="696c7-148">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="696c7-148">-WsdlServiceName</span></span>
<span data-ttu-id="696c7-149">Lokaler Name des zu importierenden WSDL-Diensts.</span><span class="sxs-lookup"><span data-stu-id="696c7-149">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="696c7-150">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="696c7-150">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="696c7-151">Dieser Parameter ist optional und nur für den Import von WSDL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="696c7-151">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="696c7-152">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="696c7-152">Default value is $null.</span></span>

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

### <span data-ttu-id="696c7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696c7-153">CommonParameters</span></span>
<span data-ttu-id="696c7-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="696c7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696c7-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="696c7-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696c7-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="696c7-156">INPUTS</span></span>

### <span data-ttu-id="696c7-157">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="696c7-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="696c7-158">System. String</span><span class="sxs-lookup"><span data-stu-id="696c7-158">System.String</span></span>

### <span data-ttu-id="696c7-159">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="696c7-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="696c7-160">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiType, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. Servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="696c7-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="696c7-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="696c7-161">OUTPUTS</span></span>

### <span data-ttu-id="696c7-162">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="696c7-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="696c7-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="696c7-163">NOTES</span></span>

## <span data-ttu-id="696c7-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="696c7-164">RELATED LINKS</span></span>

[<span data-ttu-id="696c7-165">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="696c7-165">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="696c7-166">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="696c7-166">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="696c7-167">Neu – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="696c7-167">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="696c7-168">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="696c7-168">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="696c7-169">Satz-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="696c7-169">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


