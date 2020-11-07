---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: a0e8a131b0a66c3887ecea7054a2f13b75e7f598
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820367"
---
# <span data-ttu-id="7fdf5-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="7fdf5-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="7fdf5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7fdf5-102">SYNOPSIS</span></span>
<span data-ttu-id="7fdf5-103">Entfernt einen verknüpften Dienst aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="7fdf5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fdf5-104">SYNTAX</span></span>

### <span data-ttu-id="7fdf5-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7fdf5-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fdf5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7fdf5-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fdf5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7fdf5-107">DESCRIPTION</span></span>
<span data-ttu-id="7fdf5-108">Das Cmdlet **Remove-AzDataFactoryLinkedService** entfernt einen verknüpften Dienst aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="7fdf5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7fdf5-109">EXAMPLES</span></span>

### <span data-ttu-id="7fdf5-110">Beispiel 1: Entfernen eines verknüpften Diensts</span><span class="sxs-lookup"><span data-stu-id="7fdf5-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="7fdf5-111">Mit diesem Befehl wird der verknüpfte Dienst mit dem Namen LinkedServiceTest aus der Data Factory mit dem Namen WikiADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="7fdf5-112">Dieser Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="7fdf5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fdf5-113">PARAMETERS</span></span>

### <span data-ttu-id="7fdf5-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fdf5-114">-DataFactory</span></span>
<span data-ttu-id="7fdf5-115">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="7fdf5-116">Mit diesem Cmdlet wird ein verknüpfter Dienst aus der Data Factory entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7fdf5-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="7fdf5-117">-DataFactoryName</span></span>
<span data-ttu-id="7fdf5-118">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7fdf5-119">Mit diesem Cmdlet wird ein verknüpfter Dienst aus der Data Factory entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7fdf5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fdf5-120">-DefaultProfile</span></span>
<span data-ttu-id="7fdf5-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7fdf5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fdf5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="7fdf5-122">-Force</span></span>
<span data-ttu-id="7fdf5-123">Gibt an, dass mit diesem Cmdlet ein verknüpfter Dienst entfernt wird, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="7fdf5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7fdf5-124">-Name</span></span>
<span data-ttu-id="7fdf5-125">Gibt den Namen des zu entfernenden verknüpften Diensts an.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fdf5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fdf5-126">-ResourceGroupName</span></span>
<span data-ttu-id="7fdf5-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7fdf5-128">Mit diesem Cmdlet wird ein verknüpfter Dienst aus der Gruppe entfernt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7fdf5-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7fdf5-129">-Confirm</span></span>
<span data-ttu-id="7fdf5-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fdf5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fdf5-131">-WhatIf</span></span>
<span data-ttu-id="7fdf5-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fdf5-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fdf5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fdf5-134">CommonParameters</span></span>
<span data-ttu-id="7fdf5-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fdf5-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fdf5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fdf5-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7fdf5-137">INPUTS</span></span>

### <span data-ttu-id="7fdf5-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7fdf5-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="7fdf5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7fdf5-139">System.String</span></span>

## <span data-ttu-id="7fdf5-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7fdf5-140">OUTPUTS</span></span>

### <span data-ttu-id="7fdf5-141">System. void</span><span class="sxs-lookup"><span data-stu-id="7fdf5-141">System.Void</span></span>

## <span data-ttu-id="7fdf5-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="7fdf5-142">NOTES</span></span>
* <span data-ttu-id="7fdf5-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="7fdf5-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7fdf5-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7fdf5-144">RELATED LINKS</span></span>

[<span data-ttu-id="7fdf5-145">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="7fdf5-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="7fdf5-146">Neu – AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="7fdf5-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)


