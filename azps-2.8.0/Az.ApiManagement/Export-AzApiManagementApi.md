---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 7b4163b18905fd0676543de1b0ead26d11c7096a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658342"
---
# <span data-ttu-id="b703d-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b703d-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="b703d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b703d-102">SYNOPSIS</span></span>
<span data-ttu-id="b703d-103">Exportiert eine API in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="b703d-103">Exports an API to a file.</span></span>

## <span data-ttu-id="b703d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b703d-104">SYNTAX</span></span>

### <span data-ttu-id="b703d-105">ExportToPipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="b703d-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b703d-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="b703d-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b703d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b703d-107">DESCRIPTION</span></span>
<span data-ttu-id="b703d-108">Das Cmdlet **Export-AzApiManagementApi** exportiert eine Azure API-Verwaltungs-API in eine Datei in einem der unterstützten Formate.</span><span class="sxs-lookup"><span data-stu-id="b703d-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="b703d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b703d-109">EXAMPLES</span></span>

### <span data-ttu-id="b703d-110">Beispiel 1: Exportieren einer API im Web Application Description Language (WADL)-Format</span><span class="sxs-lookup"><span data-stu-id="b703d-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="b703d-111">Dieser Befehl exportiert eine API in eine WADL-Datei.</span><span class="sxs-lookup"><span data-stu-id="b703d-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="b703d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b703d-112">PARAMETERS</span></span>

### <span data-ttu-id="b703d-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b703d-113">-ApiId</span></span>
<span data-ttu-id="b703d-114">Gibt die ID der API an, die exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b703d-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="b703d-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="b703d-115">-ApiRevision</span></span>
<span data-ttu-id="b703d-116">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="b703d-116">Identifier of API Revision.</span></span> <span data-ttu-id="b703d-117">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b703d-117">This parameter is optional.</span></span> <span data-ttu-id="b703d-118">Wenn nicht angegeben, wird der Export für die derzeit aktive API-Revision durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b703d-118">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="b703d-119">-Context</span><span class="sxs-lookup"><span data-stu-id="b703d-119">-Context</span></span>
<span data-ttu-id="b703d-120">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b703d-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b703d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b703d-121">-DefaultProfile</span></span>
<span data-ttu-id="b703d-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b703d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b703d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b703d-123">-Force</span></span>
<span data-ttu-id="b703d-124">Gibt an, dass diese Operation die Datei mit dem gleichen Namen überschreibt, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b703d-124">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="b703d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b703d-125">-PassThru</span></span>
<span data-ttu-id="b703d-126">Gibt an, dass dieser Vorgang $true zurückgibt, wenn die API erfolgreich exportiert wird, oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="b703d-126">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="b703d-127">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="b703d-127">-SaveAs</span></span>
<span data-ttu-id="b703d-128">Gibt den Dateipfad an, in dem die exportierte API gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b703d-128">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="b703d-129">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="b703d-129">-SpecificationFormat</span></span>
<span data-ttu-id="b703d-130">Gibt das API-Format an.</span><span class="sxs-lookup"><span data-stu-id="b703d-130">Specifies the API format.</span></span>
<span data-ttu-id="b703d-131">psdx_paramvalues WADL und Prahlerei.</span><span class="sxs-lookup"><span data-stu-id="b703d-131">psdx_paramvalues Wadl and Swagger.</span></span>

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

### <span data-ttu-id="b703d-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b703d-132">-Confirm</span></span>
<span data-ttu-id="b703d-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b703d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b703d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b703d-134">-WhatIf</span></span>
<span data-ttu-id="b703d-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b703d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b703d-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b703d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b703d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b703d-137">CommonParameters</span></span>
<span data-ttu-id="b703d-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b703d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b703d-139">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b703d-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b703d-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b703d-140">INPUTS</span></span>

### <span data-ttu-id="b703d-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b703d-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b703d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b703d-142">System.String</span></span>

### <span data-ttu-id="b703d-143">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="b703d-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="b703d-144">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="b703d-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b703d-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b703d-145">OUTPUTS</span></span>

### <span data-ttu-id="b703d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b703d-146">System.String</span></span>

## <span data-ttu-id="b703d-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="b703d-147">NOTES</span></span>

## <span data-ttu-id="b703d-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b703d-148">RELATED LINKS</span></span>

[<span data-ttu-id="b703d-149">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b703d-149">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="b703d-150">Importieren-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b703d-150">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="b703d-151">Neu – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b703d-151">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="b703d-152">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b703d-152">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="b703d-153">Satz-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b703d-153">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


