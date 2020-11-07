---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 09400d3111ffb3fda232e1cbb71fd0aac063a74c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663620"
---
# <span data-ttu-id="a86e3-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a86e3-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="a86e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a86e3-102">SYNOPSIS</span></span>
<span data-ttu-id="a86e3-103">Exportiert eine API in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="a86e3-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a86e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a86e3-104">SYNTAX</span></span>

### <span data-ttu-id="a86e3-105">In Pipeline exportieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="a86e3-105">Export to pipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a86e3-106">In Datei exportieren</span><span class="sxs-lookup"><span data-stu-id="a86e3-106">Export to File</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a86e3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a86e3-107">DESCRIPTION</span></span>
<span data-ttu-id="a86e3-108">Das Cmdlet **Export-AzureRmApiManagementApi** exportiert eine Azure API-Verwaltungs-API in eine Datei in einem der unterstützten Formate.</span><span class="sxs-lookup"><span data-stu-id="a86e3-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="a86e3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a86e3-109">EXAMPLES</span></span>

### <span data-ttu-id="a86e3-110">Beispiel 1: Exportieren einer API im Web Application Description Language (WADL)-Format</span><span class="sxs-lookup"><span data-stu-id="a86e3-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="a86e3-111">Dieser Befehl exportiert eine API in eine WADL-Datei.</span><span class="sxs-lookup"><span data-stu-id="a86e3-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="a86e3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a86e3-112">PARAMETERS</span></span>

### <span data-ttu-id="a86e3-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a86e3-113">-ApiId</span></span>
<span data-ttu-id="a86e3-114">Gibt die ID der API an, die exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a86e3-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="a86e3-115">-Context</span><span class="sxs-lookup"><span data-stu-id="a86e3-115">-Context</span></span>
<span data-ttu-id="a86e3-116">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a86e3-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a86e3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a86e3-117">-Force</span></span>
<span data-ttu-id="a86e3-118">Gibt an, dass diese Operation die Datei mit dem gleichen Namen überschreibt, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a86e3-118">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to File
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a86e3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a86e3-119">-PassThru</span></span>
<span data-ttu-id="a86e3-120">Gibt an, dass dieser Vorgang $true zurückgibt, wenn die API erfolgreich exportiert wird, oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="a86e3-120">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to File
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a86e3-121">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="a86e3-121">-SaveAs</span></span>
<span data-ttu-id="a86e3-122">Gibt den Dateipfad an, in dem die exportierte API gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a86e3-122">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: Export to File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a86e3-123">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="a86e3-123">-SpecificationFormat</span></span>
<span data-ttu-id="a86e3-124">Gibt das API-Format an.</span><span class="sxs-lookup"><span data-stu-id="a86e3-124">Specifies the API format.</span></span>
<span data-ttu-id="a86e3-125">psdx_paramvalues WADL und Prahlerei.</span><span class="sxs-lookup"><span data-stu-id="a86e3-125">psdx_paramvalues Wadl and Swagger.</span></span>

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

### <span data-ttu-id="a86e3-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a86e3-126">-Confirm</span></span>
<span data-ttu-id="a86e3-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a86e3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a86e3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a86e3-128">-WhatIf</span></span>
<span data-ttu-id="a86e3-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a86e3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a86e3-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a86e3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a86e3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a86e3-131">-DefaultProfile</span></span>
<span data-ttu-id="a86e3-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a86e3-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a86e3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a86e3-133">CommonParameters</span></span>
<span data-ttu-id="a86e3-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a86e3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a86e3-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a86e3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a86e3-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a86e3-136">INPUTS</span></span>

## <span data-ttu-id="a86e3-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a86e3-137">OUTPUTS</span></span>

### <span data-ttu-id="a86e3-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a86e3-138">String</span></span>
<span data-ttu-id="a86e3-139">Dieses Cmdlet gibt den exportierten API-Inhalt als Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="a86e3-139">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="a86e3-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="a86e3-140">NOTES</span></span>

## <span data-ttu-id="a86e3-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a86e3-141">RELATED LINKS</span></span>

[<span data-ttu-id="a86e3-142">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a86e3-142">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="a86e3-143">Importieren-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a86e3-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="a86e3-144">Neu – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a86e3-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="a86e3-145">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a86e3-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="a86e3-146">Satz-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a86e3-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


