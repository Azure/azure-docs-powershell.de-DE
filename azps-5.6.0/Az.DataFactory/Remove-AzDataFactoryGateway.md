---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: eb9100bf4843d7213d2fbb89ac1827ba7ee1e509
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921312"
---
# <span data-ttu-id="5619a-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="5619a-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="5619a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5619a-102">SYNOPSIS</span></span>
<span data-ttu-id="5619a-103">Entfernt ein Gateway aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="5619a-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="5619a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5619a-104">SYNTAX</span></span>

### <span data-ttu-id="5619a-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5619a-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5619a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5619a-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5619a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5619a-107">DESCRIPTION</span></span>
<span data-ttu-id="5619a-108">Das **Cmdlet Remove-AzDataFactoryGateway** entfernt das angegebene Gateway aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="5619a-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="5619a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5619a-109">EXAMPLES</span></span>

### <span data-ttu-id="5619a-110">Beispiel 1: Entfernen eines Gateways</span><span class="sxs-lookup"><span data-stu-id="5619a-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="5619a-111">Mit diesem Befehl wird das Gateway namens ContosoGateway aus der Daten factory mit dem Namen WikiADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="5619a-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="5619a-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5619a-112">PARAMETERS</span></span>

### <span data-ttu-id="5619a-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5619a-113">-DataFactory</span></span>
<span data-ttu-id="5619a-114">Gibt ein **PSDataFactory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="5619a-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="5619a-115">Dieses Cmdlet entfernt ein Gateway aus der Daten factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5619a-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5619a-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5619a-116">-DataFactoryName</span></span>
<span data-ttu-id="5619a-117">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="5619a-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5619a-118">Dieses Cmdlet entfernt ein Gateway aus der Daten factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5619a-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5619a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5619a-119">-DefaultProfile</span></span>
<span data-ttu-id="5619a-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5619a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5619a-121">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="5619a-121">-Force</span></span>
<span data-ttu-id="5619a-122">Gibt an, dass dieses Cmdlet ein Gateway entfernt, ohne Sie zur Bestätigung auffordern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="5619a-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5619a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5619a-123">-Name</span></span>
<span data-ttu-id="5619a-124">Gibt den Namen des zu entfernenden Gateways an.</span><span class="sxs-lookup"><span data-stu-id="5619a-124">Specifies the name of the gateway to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5619a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5619a-125">-ResourceGroupName</span></span>
<span data-ttu-id="5619a-126">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5619a-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5619a-127">Dieses Cmdlet entfernt ein Gateway, das zu der Gruppe gehört, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5619a-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5619a-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5619a-128">-Confirm</span></span>
<span data-ttu-id="5619a-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5619a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5619a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5619a-130">-WhatIf</span></span>
<span data-ttu-id="5619a-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5619a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5619a-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5619a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5619a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5619a-133">CommonParameters</span></span>
<span data-ttu-id="5619a-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5619a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5619a-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5619a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5619a-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5619a-136">INPUTS</span></span>

### <span data-ttu-id="5619a-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5619a-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="5619a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5619a-138">System.String</span></span>

## <span data-ttu-id="5619a-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5619a-139">OUTPUTS</span></span>

### <span data-ttu-id="5619a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5619a-140">System.Boolean</span></span>

## <span data-ttu-id="5619a-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5619a-141">NOTES</span></span>
* <span data-ttu-id="5619a-142">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="5619a-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5619a-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5619a-143">RELATED LINKS</span></span>

[<span data-ttu-id="5619a-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="5619a-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="5619a-145">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="5619a-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="5619a-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="5619a-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


