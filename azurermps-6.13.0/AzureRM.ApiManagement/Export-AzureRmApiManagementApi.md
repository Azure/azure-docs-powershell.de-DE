---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/export-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 7dc06f280595551a9e054c251339e96163b798b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663017"
---
# <span data-ttu-id="26e5f-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="26e5f-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="26e5f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26e5f-102">SYNOPSIS</span></span>
<span data-ttu-id="26e5f-103">Exportiert eine API in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="26e5f-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26e5f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26e5f-104">SYNTAX</span></span>

### <span data-ttu-id="26e5f-105">ExportToPipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="26e5f-105">ExportToPipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e5f-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="26e5f-106">ExportToFile</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26e5f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26e5f-107">DESCRIPTION</span></span>
<span data-ttu-id="26e5f-108">Das Cmdlet **Export-AzureRmApiManagementApi** exportiert eine Azure API-Verwaltungs-API in eine Datei in einem der unterstützten Formate.</span><span class="sxs-lookup"><span data-stu-id="26e5f-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="26e5f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26e5f-109">EXAMPLES</span></span>

### <span data-ttu-id="26e5f-110">Beispiel 1: Exportieren einer API im Web Application Description Language (WADL)-Format</span><span class="sxs-lookup"><span data-stu-id="26e5f-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="26e5f-111">Dieser Befehl exportiert eine API in eine WADL-Datei.</span><span class="sxs-lookup"><span data-stu-id="26e5f-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="26e5f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="26e5f-112">PARAMETERS</span></span>

### <span data-ttu-id="26e5f-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="26e5f-113">-ApiId</span></span>
<span data-ttu-id="26e5f-114">Gibt die ID der API an, die exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="26e5f-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="26e5f-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="26e5f-115">-ApiRevision</span></span>
<span data-ttu-id="26e5f-116">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="26e5f-116">Identifier of API Revision.</span></span> <span data-ttu-id="26e5f-117">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="26e5f-117">This parameter is optional.</span></span> <span data-ttu-id="26e5f-118">Wenn nicht angegeben, wird der Export für die derzeit aktive API-Revision durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="26e5f-118">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="26e5f-119">-Context</span><span class="sxs-lookup"><span data-stu-id="26e5f-119">-Context</span></span>
<span data-ttu-id="26e5f-120">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="26e5f-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="26e5f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e5f-121">-DefaultProfile</span></span>
<span data-ttu-id="26e5f-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="26e5f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26e5f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="26e5f-123">-Force</span></span>
<span data-ttu-id="26e5f-124">Gibt an, dass diese Operation die Datei mit dem gleichen Namen überschreibt, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="26e5f-124">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="26e5f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26e5f-125">-PassThru</span></span>
<span data-ttu-id="26e5f-126">Gibt an, dass dieser Vorgang $true zurückgibt, wenn die API erfolgreich exportiert wird, oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="26e5f-126">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="26e5f-127">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="26e5f-127">-SaveAs</span></span>
<span data-ttu-id="26e5f-128">Gibt den Dateipfad an, in dem die exportierte API gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="26e5f-128">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="26e5f-129">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="26e5f-129">-SpecificationFormat</span></span>
<span data-ttu-id="26e5f-130">Gibt das API-Format an.</span><span class="sxs-lookup"><span data-stu-id="26e5f-130">Specifies the API format.</span></span>
<span data-ttu-id="26e5f-131">psdx_paramvalues WADL und Prahlerei.</span><span class="sxs-lookup"><span data-stu-id="26e5f-131">psdx_paramvalues Wadl and Swagger.</span></span>

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

### <span data-ttu-id="26e5f-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="26e5f-132">-Confirm</span></span>
<span data-ttu-id="26e5f-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26e5f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e5f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e5f-134">-WhatIf</span></span>
<span data-ttu-id="26e5f-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26e5f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26e5f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26e5f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26e5f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e5f-137">CommonParameters</span></span>
<span data-ttu-id="26e5f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e5f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e5f-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26e5f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e5f-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26e5f-140">INPUTS</span></span>

### <span data-ttu-id="26e5f-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="26e5f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="26e5f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="26e5f-142">System.String</span></span>

### <span data-ttu-id="26e5f-143">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="26e5f-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="26e5f-144">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="26e5f-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="26e5f-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26e5f-145">OUTPUTS</span></span>

### <span data-ttu-id="26e5f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="26e5f-146">System.String</span></span>
<span data-ttu-id="26e5f-147">Dieses Cmdlet gibt den exportierten API-Inhalt als Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="26e5f-147">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="26e5f-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="26e5f-148">NOTES</span></span>

## <span data-ttu-id="26e5f-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26e5f-149">RELATED LINKS</span></span>

[<span data-ttu-id="26e5f-150">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="26e5f-150">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="26e5f-151">Importieren-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="26e5f-151">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="26e5f-152">Neu – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="26e5f-152">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="26e5f-153">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="26e5f-153">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="26e5f-154">Satz-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="26e5f-154">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


