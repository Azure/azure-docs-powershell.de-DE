---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
ms.openlocfilehash: 5e00f3718b093f3112839ebb331fc96984a03038
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664703"
---
# <span data-ttu-id="18300-101">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="18300-101">Import-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="18300-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18300-102">SYNOPSIS</span></span>
<span data-ttu-id="18300-103">Importiert eine API aus einer Datei oder einer URL.</span><span class="sxs-lookup"><span data-stu-id="18300-103">Imports an API from a file or a URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18300-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18300-104">SYNTAX</span></span>

### <span data-ttu-id="18300-105">ImportFromLocalFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="18300-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18300-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="18300-106">ImportFromUrl</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18300-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18300-107">DESCRIPTION</span></span>
<span data-ttu-id="18300-108">Das Cmdlet " **Import-AzureRmApiManagementApi** " importiert eine Azure API-Verwaltungs-API aus einer Datei oder einer URL in Web Application Description Language (WADL), Web Services Description Language (WSDL) oder Prahlerei-Format.</span><span class="sxs-lookup"><span data-stu-id="18300-108">The **Import-AzureRmApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="18300-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18300-109">EXAMPLES</span></span>

### <span data-ttu-id="18300-110">Beispiel 1 Importieren einer API aus einer WADL-Datei</span><span class="sxs-lookup"><span data-stu-id="18300-110">Example 1 Import an API from a WADL file</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="18300-111">Dieser Befehl importiert eine API aus der angegebenen WADL-Datei.</span><span class="sxs-lookup"><span data-stu-id="18300-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="18300-112">Beispiel 2 Importieren einer API aus einer Prahlerei-Datei</span><span class="sxs-lookup"><span data-stu-id="18300-112">Example 2 Import an API from a Swagger file</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="18300-113">Dieser Befehl importiert eine API aus der angegebenen Prahlerei-Datei.</span><span class="sxs-lookup"><span data-stu-id="18300-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="18300-114">Beispiel 3: Importieren einer API aus einem WADL-Link</span><span class="sxs-lookup"><span data-stu-id="18300-114">Example 3: Import an API from a WADL link</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="18300-115">Dieser Befehl importiert eine API aus dem angegebenen WADL-Link.</span><span class="sxs-lookup"><span data-stu-id="18300-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="18300-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="18300-116">PARAMETERS</span></span>

### <span data-ttu-id="18300-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="18300-117">-ApiId</span></span>
<span data-ttu-id="18300-118">Gibt eine ID für die zu importierende API an.</span><span class="sxs-lookup"><span data-stu-id="18300-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="18300-119">Wenn Sie diesen Parameter nicht angeben, wird eine ID für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="18300-119">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18300-120">-ApiType</span><span class="sxs-lookup"><span data-stu-id="18300-120">-ApiType</span></span>
<span data-ttu-id="18300-121">Dieser Parameter ist optional mit dem Standardwert http.</span><span class="sxs-lookup"><span data-stu-id="18300-121">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="18300-122">Die SOAP-Option ist nur beim Importieren von WSDL anwendbar und erstellt eine SOAP-Passthrough-API.</span><span class="sxs-lookup"><span data-stu-id="18300-122">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: PsApiManagementApiType
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18300-123">-Context</span><span class="sxs-lookup"><span data-stu-id="18300-123">-Context</span></span>
<span data-ttu-id="18300-124">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="18300-124">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18300-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18300-125">-DefaultProfile</span></span>
<span data-ttu-id="18300-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="18300-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18300-127">-Path</span><span class="sxs-lookup"><span data-stu-id="18300-127">-Path</span></span>
<span data-ttu-id="18300-128">Gibt einen Web-API-Pfad als letzten Teil der öffentlichen URL der API an.</span><span class="sxs-lookup"><span data-stu-id="18300-128">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="18300-129">Diese URL wird von API-Consumern zum Senden von Anforderungen an den Webdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="18300-129">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="18300-130">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="18300-130">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="18300-131">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="18300-131">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18300-132">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="18300-132">-SpecificationFormat</span></span>
<span data-ttu-id="18300-133">Gibt das Spezifikations Format an.</span><span class="sxs-lookup"><span data-stu-id="18300-133">Specifies the specification format.</span></span>
<span data-ttu-id="18300-134">psdx_paramvalues WADL, WSDL und Prahlerei.</span><span class="sxs-lookup"><span data-stu-id="18300-134">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: PsApiManagementApiFormat
Parameter Sets: (All)
Aliases: 
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18300-135">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="18300-135">-SpecificationPath</span></span>
<span data-ttu-id="18300-136">Gibt den Pfad der Spezifikationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="18300-136">Specifies the specification file path.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromLocalFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18300-137">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="18300-137">-SpecificationUrl</span></span>
<span data-ttu-id="18300-138">Gibt die Spezifikations-URL an.</span><span class="sxs-lookup"><span data-stu-id="18300-138">Specifies the specification URL.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromUrl
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18300-139">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="18300-139">-WsdlEndpointName</span></span>
<span data-ttu-id="18300-140">Lokaler Name des WSDL-Endpunkts (Port), der importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="18300-140">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="18300-141">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="18300-141">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="18300-142">Dieser Parameter ist optional und nur für den Import von WSDL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="18300-142">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="18300-143">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="18300-143">Default value is $null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18300-144">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="18300-144">-WsdlServiceName</span></span>
<span data-ttu-id="18300-145">Lokaler Name des zu importierenden WSDL-Diensts.</span><span class="sxs-lookup"><span data-stu-id="18300-145">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="18300-146">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="18300-146">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="18300-147">Dieser Parameter ist optional und nur für den Import von WSDL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="18300-147">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="18300-148">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="18300-148">Default value is $null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18300-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18300-149">CommonParameters</span></span>
<span data-ttu-id="18300-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18300-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18300-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18300-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18300-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18300-152">INPUTS</span></span>

### <span data-ttu-id="18300-153">Keine</span><span class="sxs-lookup"><span data-stu-id="18300-153">None</span></span>
<span data-ttu-id="18300-154">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="18300-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18300-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18300-155">OUTPUTS</span></span>

### <span data-ttu-id="18300-156">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="18300-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="18300-157">Dieses Cmdlet gibt die importierte API als **PsApiManagementApi** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="18300-157">This cmdlet returns the imported API as a **PsApiManagementApi** object.</span></span>

## <span data-ttu-id="18300-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="18300-158">NOTES</span></span>

## <span data-ttu-id="18300-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18300-159">RELATED LINKS</span></span>

[<span data-ttu-id="18300-160">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="18300-160">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="18300-161">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="18300-161">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="18300-162">Neu – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="18300-162">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="18300-163">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="18300-163">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="18300-164">Satz-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="18300-164">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


