---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 3981d1fd0a921f467007afc85c00b726b6037fad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471520"
---
# <span data-ttu-id="23998-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="23998-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="23998-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23998-102">SYNOPSIS</span></span>
<span data-ttu-id="23998-103">Exportiert eine API in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="23998-103">Exports an API to a file.</span></span>

## <span data-ttu-id="23998-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23998-104">SYNTAX</span></span>

### <span data-ttu-id="23998-105">ExportToPipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="23998-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23998-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="23998-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23998-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23998-107">DESCRIPTION</span></span>
<span data-ttu-id="23998-108">Das **Cmdlet "Export-AzApiManagementApi"** exportiert eine Azure API Management API in eine Datei in einem der unterstützten Formate.</span><span class="sxs-lookup"><span data-stu-id="23998-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="23998-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="23998-109">EXAMPLES</span></span>

### <span data-ttu-id="23998-110">Beispiel 1: Exportieren einer API im Format WADL (Web Application Description Language)</span><span class="sxs-lookup"><span data-stu-id="23998-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="23998-111">Mit diesem Befehl wird eine API in eine WADL-Datei exportiert.</span><span class="sxs-lookup"><span data-stu-id="23998-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="23998-112">Beispiel 2: Exportieren einer API im OpenApi 3.0-Spezifikationsformat als Json-Dokument</span><span class="sxs-lookup"><span data-stu-id="23998-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="23998-113">Dieser Befehl exportiert eine API-Definition im Open -API-Format als Json-Dokument.</span><span class="sxs-lookup"><span data-stu-id="23998-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="23998-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23998-114">PARAMETERS</span></span>

### <span data-ttu-id="23998-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="23998-115">-ApiId</span></span>
<span data-ttu-id="23998-116">Gibt die ID der zu exportierenden API an.</span><span class="sxs-lookup"><span data-stu-id="23998-116">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="23998-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="23998-117">-ApiRevision</span></span>
<span data-ttu-id="23998-118">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="23998-118">Identifier of API Revision.</span></span> <span data-ttu-id="23998-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="23998-119">This parameter is optional.</span></span> <span data-ttu-id="23998-120">Wenn keine Angabe erfolgt, erfolgt der Export für die derzeit aktive API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="23998-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="23998-121">-Context</span><span class="sxs-lookup"><span data-stu-id="23998-121">-Context</span></span>
<span data-ttu-id="23998-122">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="23998-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="23998-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23998-123">-DefaultProfile</span></span>
<span data-ttu-id="23998-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23998-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23998-125">-Force</span><span class="sxs-lookup"><span data-stu-id="23998-125">-Force</span></span>
<span data-ttu-id="23998-126">Gibt an, dass durch diesen Vorgang die Datei mit demselben Namen überschrieben wird, wenn sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="23998-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="23998-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23998-127">-PassThru</span></span>
<span data-ttu-id="23998-128">Gibt an, dass dieser Vorgang $True, wenn die API erfolgreich exportiert wurde, oder $False zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="23998-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="23998-129">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="23998-129">-SaveAs</span></span>
<span data-ttu-id="23998-130">Gibt den Dateipfad an, unter dem die exportierte API gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="23998-130">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="23998-131">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="23998-131">-SpecificationFormat</span></span>
<span data-ttu-id="23998-132">Gibt das API-Format an.</span><span class="sxs-lookup"><span data-stu-id="23998-132">Specifies the API format.</span></span>
<span data-ttu-id="23998-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi und OpenApiJson</span><span class="sxs-lookup"><span data-stu-id="23998-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

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

### <span data-ttu-id="23998-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23998-134">-Confirm</span></span>
<span data-ttu-id="23998-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23998-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23998-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="23998-136">-WhatIf</span></span>
<span data-ttu-id="23998-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23998-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23998-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23998-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23998-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23998-139">CommonParameters</span></span>
<span data-ttu-id="23998-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23998-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23998-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23998-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23998-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="23998-142">INPUTS</span></span>

### <span data-ttu-id="23998-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="23998-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="23998-144">System.String</span><span class="sxs-lookup"><span data-stu-id="23998-144">System.String</span></span>

### <span data-ttu-id="23998-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="23998-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="23998-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="23998-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="23998-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="23998-147">OUTPUTS</span></span>

### <span data-ttu-id="23998-148">System.String</span><span class="sxs-lookup"><span data-stu-id="23998-148">System.String</span></span>

## <span data-ttu-id="23998-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="23998-149">NOTES</span></span>

## <span data-ttu-id="23998-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="23998-150">RELATED LINKS</span></span>

[<span data-ttu-id="23998-151">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="23998-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="23998-152">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="23998-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="23998-153">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="23998-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="23998-154">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="23998-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="23998-155">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="23998-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


