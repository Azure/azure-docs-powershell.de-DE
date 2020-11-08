---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 3981d1fd0a921f467007afc85c00b726b6037fad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174426"
---
# <span data-ttu-id="9ee2b-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9ee2b-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="9ee2b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ee2b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee2b-103">Exportiert eine API in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-103">Exports an API to a file.</span></span>

## <span data-ttu-id="9ee2b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ee2b-104">SYNTAX</span></span>

### <span data-ttu-id="9ee2b-105">ExportToPipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ee2b-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ee2b-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="9ee2b-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ee2b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ee2b-107">DESCRIPTION</span></span>
<span data-ttu-id="9ee2b-108">Das Cmdlet **Export-AzApiManagementApi** exportiert eine Azure API-Verwaltungs-API in eine Datei in einem der unterstützten Formate.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="9ee2b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ee2b-109">EXAMPLES</span></span>

### <span data-ttu-id="9ee2b-110">Beispiel 1: Exportieren einer API im Web Application Description Language (WADL)-Format</span><span class="sxs-lookup"><span data-stu-id="9ee2b-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="9ee2b-111">Dieser Befehl exportiert eine API in eine WADL-Datei.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="9ee2b-112">Beispiel 2: Exportieren einer API im OpenApi 3,0-Spezifikations Format als JSON-Dokument</span><span class="sxs-lookup"><span data-stu-id="9ee2b-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="9ee2b-113">Dieser Befehl exportiert eine API-Definition im Open-API-Format als JSON-Dokument.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="9ee2b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ee2b-114">PARAMETERS</span></span>

### <span data-ttu-id="9ee2b-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9ee2b-115">-ApiId</span></span>
<span data-ttu-id="9ee2b-116">Gibt die ID der API an, die exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-116">Specifies the ID of the API to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee2b-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="9ee2b-117">-ApiRevision</span></span>
<span data-ttu-id="9ee2b-118">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-118">Identifier of API Revision.</span></span> <span data-ttu-id="9ee2b-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-119">This parameter is optional.</span></span> <span data-ttu-id="9ee2b-120">Wenn nicht angegeben, wird der Export für die derzeit aktive API-Revision durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="9ee2b-121">-Context</span><span class="sxs-lookup"><span data-stu-id="9ee2b-121">-Context</span></span>
<span data-ttu-id="9ee2b-122">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9ee2b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee2b-123">-DefaultProfile</span></span>
<span data-ttu-id="9ee2b-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ee2b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9ee2b-125">-Force</span></span>
<span data-ttu-id="9ee2b-126">Gibt an, dass diese Operation die Datei mit dem gleichen Namen überschreibt, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee2b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ee2b-127">-PassThru</span></span>
<span data-ttu-id="9ee2b-128">Gibt an, dass dieser Vorgang $true zurückgibt, wenn die API erfolgreich exportiert wird, oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee2b-129">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="9ee2b-129">-SaveAs</span></span>
<span data-ttu-id="9ee2b-130">Gibt den Dateipfad an, in dem die exportierte API gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-130">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee2b-131">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="9ee2b-131">-SpecificationFormat</span></span>
<span data-ttu-id="9ee2b-132">Gibt das API-Format an.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-132">Specifies the API format.</span></span>
<span data-ttu-id="9ee2b-133">psdx_paramvalues WADL, WSDL, Prahlerei, OpenApi und OpenApiJson</span><span class="sxs-lookup"><span data-stu-id="9ee2b-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee2b-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ee2b-134">-Confirm</span></span>
<span data-ttu-id="9ee2b-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee2b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ee2b-136">-WhatIf</span></span>
<span data-ttu-id="9ee2b-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ee2b-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee2b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee2b-139">CommonParameters</span></span>
<span data-ttu-id="9ee2b-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ee2b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee2b-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ee2b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee2b-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ee2b-142">INPUTS</span></span>

### <span data-ttu-id="9ee2b-143">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9ee2b-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9ee2b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9ee2b-144">System.String</span></span>

### <span data-ttu-id="9ee2b-145">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="9ee2b-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="9ee2b-146">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="9ee2b-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9ee2b-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ee2b-147">OUTPUTS</span></span>

### <span data-ttu-id="9ee2b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="9ee2b-148">System.String</span></span>

## <span data-ttu-id="9ee2b-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ee2b-149">NOTES</span></span>

## <span data-ttu-id="9ee2b-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ee2b-150">RELATED LINKS</span></span>

[<span data-ttu-id="9ee2b-151">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9ee2b-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="9ee2b-152">Importieren-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9ee2b-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="9ee2b-153">Neu – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9ee2b-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="9ee2b-154">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9ee2b-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="9ee2b-155">Satz-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9ee2b-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


