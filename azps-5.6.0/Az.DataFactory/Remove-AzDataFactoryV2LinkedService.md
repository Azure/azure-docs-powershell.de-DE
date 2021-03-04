---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: 87a50c69449437401ff26b76b87cf0f334ab8d71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930560"
---
# <span data-ttu-id="0b3bf-101">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0b3bf-101">Remove-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="0b3bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b3bf-102">SYNOPSIS</span></span>
<span data-ttu-id="0b3bf-103">Entfernt einen verknüpften Dienst aus Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-103">Removes a linked service from Data Factory.</span></span>

## <span data-ttu-id="0b3bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b3bf-104">SYNTAX</span></span>

### <span data-ttu-id="0b3bf-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b3bf-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b3bf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0b3bf-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b3bf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0b3bf-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b3bf-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b3bf-108">DESCRIPTION</span></span>
<span data-ttu-id="0b3bf-109">Das Remove-AzDataFactoryV2LinkedService cmdlet entfernt einen verknüpften Dienst aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-109">The Remove-AzDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="0b3bf-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b3bf-110">EXAMPLES</span></span>

### <span data-ttu-id="0b3bf-111">Beispiel 1: Entfernen eines verknüpften Diensts</span><span class="sxs-lookup"><span data-stu-id="0b3bf-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="0b3bf-112">Mit diesem Befehl wird der verknüpfte Dienst mit dem Namen LinkedServiceTest aus der Daten factory mit dem Namen WikiADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="0b3bf-113">Dieser Befehl gibt einen Wert von $True.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="0b3bf-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0b3bf-114">PARAMETERS</span></span>

### <span data-ttu-id="0b3bf-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0b3bf-115">-DataFactoryName</span></span>
<span data-ttu-id="0b3bf-116">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0b3bf-117">Dieses Cmdlet entfernt einen verknüpften Dienst aus der daten factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0b3bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b3bf-118">-DefaultProfile</span></span>
<span data-ttu-id="0b3bf-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b3bf-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="0b3bf-120">-Force</span></span>
<span data-ttu-id="0b3bf-121">Führt das Cmdlet aus, ohne zur Bestätigung aufgefordert zu werden.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0b3bf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b3bf-122">-InputObject</span></span>
<span data-ttu-id="0b3bf-123">Gibt das zu entfernende LinkedService-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3bf-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0b3bf-124">-Name</span></span>
<span data-ttu-id="0b3bf-125">Gibt den Namen des verknüpften Diensts an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="0b3bf-126">Name des verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3bf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b3bf-127">-ResourceGroupName</span></span>
<span data-ttu-id="0b3bf-128">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0b3bf-129">Dieses Cmdlet entfernt einen verknüpften Dienst aus der Gruppe, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0b3bf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b3bf-130">-ResourceId</span></span>
<span data-ttu-id="0b3bf-131">Die Azure-Ressourcen-ID des verknüpften Diensts, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-131">The Azure resource ID of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3bf-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b3bf-132">-Confirm</span></span>
<span data-ttu-id="0b3bf-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3bf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b3bf-134">-WhatIf</span></span>
<span data-ttu-id="0b3bf-135">Zeigt, was geschieht, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3bf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b3bf-136">CommonParameters</span></span>
<span data-ttu-id="0b3bf-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b3bf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b3bf-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b3bf-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b3bf-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b3bf-139">INPUTS</span></span>

### <span data-ttu-id="0b3bf-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="0b3bf-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

### <span data-ttu-id="0b3bf-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0b3bf-141">System.String</span></span>

## <span data-ttu-id="0b3bf-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b3bf-142">OUTPUTS</span></span>

### <span data-ttu-id="0b3bf-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="0b3bf-143">System.Void</span></span>

## <span data-ttu-id="0b3bf-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0b3bf-144">NOTES</span></span>
<span data-ttu-id="0b3bf-145">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="0b3bf-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0b3bf-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0b3bf-146">RELATED LINKS</span></span>

[<span data-ttu-id="0b3bf-147">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0b3bf-147">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="0b3bf-148">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0b3bf-148">Set-AzDataFactoryV2LinkedService</span></span>]()

