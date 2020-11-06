---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
ms.openlocfilehash: a95aa5cf5d78d2540fe2816cfa4b044502c69b0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498090"
---
# <span data-ttu-id="96374-101">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="96374-101">Import-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="96374-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96374-102">SYNOPSIS</span></span>
<span data-ttu-id="96374-103">Importiert eine API aus einer Datei oder einer URL.</span><span class="sxs-lookup"><span data-stu-id="96374-103">Imports an API from a file or a URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96374-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96374-104">SYNTAX</span></span>

### <span data-ttu-id="96374-105">Aus lokaler Datei (Standard)</span><span class="sxs-lookup"><span data-stu-id="96374-105">From Local File (Default)</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96374-106">Von URL</span><span class="sxs-lookup"><span data-stu-id="96374-106">From URL</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96374-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96374-107">DESCRIPTION</span></span>
<span data-ttu-id="96374-108">Das Cmdlet " **Import-AzureRmApiManagementApi** " importiert eine Azure API-Verwaltungs-API aus einer Datei oder einer URL in Web Application Description Language (WADL), Web Services Description Language (WSDL) oder Prahlerei-Format.</span><span class="sxs-lookup"><span data-stu-id="96374-108">The **Import-AzureRmApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="96374-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96374-109">EXAMPLES</span></span>

### <span data-ttu-id="96374-110">Beispiel 1 Importieren einer API aus einer WADL-Datei</span><span class="sxs-lookup"><span data-stu-id="96374-110">Example 1 Import an API from a WADL file</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="96374-111">Dieser Befehl importiert eine API aus der angegebenen WADL-Datei.</span><span class="sxs-lookup"><span data-stu-id="96374-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="96374-112">Beispiel 2 Importieren einer API aus einer Prahlerei-Datei</span><span class="sxs-lookup"><span data-stu-id="96374-112">Example 2 Import an API from a Swagger file</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="96374-113">Dieser Befehl importiert eine API aus der angegebenen Prahlerei-Datei.</span><span class="sxs-lookup"><span data-stu-id="96374-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="96374-114">Beispiel 3: Importieren einer API aus einem WADL-Link</span><span class="sxs-lookup"><span data-stu-id="96374-114">Example 3: Import an API from a WADL link</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="96374-115">Dieser Befehl importiert eine API aus dem angegebenen WADL-Link.</span><span class="sxs-lookup"><span data-stu-id="96374-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="96374-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="96374-116">PARAMETERS</span></span>

### <span data-ttu-id="96374-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="96374-117">-ApiId</span></span>
<span data-ttu-id="96374-118">Gibt eine ID für die zu importierende API an.</span><span class="sxs-lookup"><span data-stu-id="96374-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="96374-119">Wenn Sie diesen Parameter nicht angeben, wird eine ID für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="96374-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="96374-120">-ApiType</span><span class="sxs-lookup"><span data-stu-id="96374-120">-ApiType</span></span>
<span data-ttu-id="96374-121">Dieser Parameter ist optional mit dem Standardwert http.</span><span class="sxs-lookup"><span data-stu-id="96374-121">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="96374-122">Die SOAP-Option ist nur beim Importieren von WSDL anwendbar und erstellt eine SOAP-Passthrough-API.</span><span class="sxs-lookup"><span data-stu-id="96374-122">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="96374-123">-Context</span><span class="sxs-lookup"><span data-stu-id="96374-123">-Context</span></span>
<span data-ttu-id="96374-124">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="96374-124">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="96374-125">-Path</span><span class="sxs-lookup"><span data-stu-id="96374-125">-Path</span></span>
<span data-ttu-id="96374-126">Gibt einen Web-API-Pfad als letzten Teil der öffentlichen URL der API an.</span><span class="sxs-lookup"><span data-stu-id="96374-126">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="96374-127">Diese URL wird von API-Consumern zum Senden von Anforderungen an den Webdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="96374-127">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="96374-128">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="96374-128">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="96374-129">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="96374-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="96374-130">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="96374-130">-SpecificationFormat</span></span>
<span data-ttu-id="96374-131">Gibt das Spezifikations Format an.</span><span class="sxs-lookup"><span data-stu-id="96374-131">Specifies the specification format.</span></span>
<span data-ttu-id="96374-132">psdx_paramvalues WADL, WSDL und Prahlerei.</span><span class="sxs-lookup"><span data-stu-id="96374-132">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

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

### <span data-ttu-id="96374-133">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="96374-133">-SpecificationPath</span></span>
<span data-ttu-id="96374-134">Gibt den Pfad der Spezifikationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="96374-134">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: From Local File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96374-135">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="96374-135">-SpecificationUrl</span></span>
<span data-ttu-id="96374-136">Gibt die Spezifikations-URL an.</span><span class="sxs-lookup"><span data-stu-id="96374-136">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: From URL
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96374-137">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="96374-137">-WsdlEndpointName</span></span>
<span data-ttu-id="96374-138">Lokaler Name des WSDL-Endpunkts (Port), der importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="96374-138">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="96374-139">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="96374-139">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="96374-140">Dieser Parameter ist optional und nur für den Import von WSDL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="96374-140">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="96374-141">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="96374-141">Default value is $null.</span></span>

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

### <span data-ttu-id="96374-142">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="96374-142">-WsdlServiceName</span></span>
<span data-ttu-id="96374-143">Lokaler Name des zu importierenden WSDL-Diensts.</span><span class="sxs-lookup"><span data-stu-id="96374-143">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="96374-144">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="96374-144">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="96374-145">Dieser Parameter ist optional und nur für den Import von WSDL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="96374-145">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="96374-146">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="96374-146">Default value is $null.</span></span>

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

### <span data-ttu-id="96374-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96374-147">-DefaultProfile</span></span>
<span data-ttu-id="96374-148">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="96374-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96374-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96374-149">CommonParameters</span></span>
<span data-ttu-id="96374-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96374-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96374-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96374-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96374-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96374-152">INPUTS</span></span>

## <span data-ttu-id="96374-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96374-153">OUTPUTS</span></span>

### <span data-ttu-id="96374-154">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="96374-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="96374-155">Dieses Cmdlet gibt die importierte API als **PsApiManagementApi** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="96374-155">This cmdlet returns the imported API as a **PsApiManagementApi** object.</span></span>

## <span data-ttu-id="96374-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="96374-156">NOTES</span></span>

## <span data-ttu-id="96374-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96374-157">RELATED LINKS</span></span>

[<span data-ttu-id="96374-158">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="96374-158">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="96374-159">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="96374-159">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="96374-160">Neu – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="96374-160">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="96374-161">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="96374-161">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="96374-162">Satz-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="96374-162">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


