---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 7b4dd01a689e1ac7b87e1c83a1e19bbd0c8a86db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663186"
---
# <span data-ttu-id="14afb-101">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="14afb-101">Remove-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="14afb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14afb-102">SYNOPSIS</span></span>
<span data-ttu-id="14afb-103">Entfernt einen verknüpften Dienst aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="14afb-103">Removes a linked service from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14afb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14afb-104">SYNTAX</span></span>

### <span data-ttu-id="14afb-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="14afb-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14afb-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="14afb-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14afb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14afb-107">DESCRIPTION</span></span>
<span data-ttu-id="14afb-108">Das Cmdlet **Remove-AzureRmDataFactoryLinkedService** entfernt einen verknüpften Dienst aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="14afb-108">The **Remove-AzureRmDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="14afb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14afb-109">EXAMPLES</span></span>

### <span data-ttu-id="14afb-110">Beispiel 1: Entfernen eines verknüpften Diensts</span><span class="sxs-lookup"><span data-stu-id="14afb-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="14afb-111">Mit diesem Befehl wird der verknüpfte Dienst mit dem Namen LinkedServiceTest aus der Data Factory mit dem Namen WikiADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="14afb-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="14afb-112">Dieser Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="14afb-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="14afb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="14afb-113">PARAMETERS</span></span>

### <span data-ttu-id="14afb-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="14afb-114">-DataFactory</span></span>
<span data-ttu-id="14afb-115">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="14afb-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="14afb-116">Mit diesem Cmdlet wird ein verknüpfter Dienst aus der Data Factory entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="14afb-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="14afb-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="14afb-117">-DataFactoryName</span></span>
<span data-ttu-id="14afb-118">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="14afb-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="14afb-119">Mit diesem Cmdlet wird ein verknüpfter Dienst aus der Data Factory entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="14afb-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="14afb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14afb-120">-DefaultProfile</span></span>
<span data-ttu-id="14afb-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="14afb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14afb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="14afb-122">-Force</span></span>
<span data-ttu-id="14afb-123">Gibt an, dass mit diesem Cmdlet ein verknüpfter Dienst entfernt wird, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="14afb-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="14afb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="14afb-124">-Name</span></span>
<span data-ttu-id="14afb-125">Gibt den Namen des zu entfernenden verknüpften Diensts an.</span><span class="sxs-lookup"><span data-stu-id="14afb-125">Specifies the name of the linked service to remove.</span></span>

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

### <span data-ttu-id="14afb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14afb-126">-ResourceGroupName</span></span>
<span data-ttu-id="14afb-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="14afb-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="14afb-128">Mit diesem Cmdlet wird ein verknüpfter Dienst aus der Gruppe entfernt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="14afb-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="14afb-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="14afb-129">-Confirm</span></span>
<span data-ttu-id="14afb-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="14afb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14afb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14afb-131">-WhatIf</span></span>
<span data-ttu-id="14afb-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14afb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14afb-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14afb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14afb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14afb-134">CommonParameters</span></span>
<span data-ttu-id="14afb-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14afb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14afb-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14afb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14afb-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14afb-137">INPUTS</span></span>

### <span data-ttu-id="14afb-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="14afb-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="14afb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="14afb-139">System.String</span></span>

## <span data-ttu-id="14afb-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14afb-140">OUTPUTS</span></span>

### <span data-ttu-id="14afb-141">System. void</span><span class="sxs-lookup"><span data-stu-id="14afb-141">System.Void</span></span>

## <span data-ttu-id="14afb-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="14afb-142">NOTES</span></span>
* <span data-ttu-id="14afb-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="14afb-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="14afb-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14afb-144">RELATED LINKS</span></span>

[<span data-ttu-id="14afb-145">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="14afb-145">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="14afb-146">Neu – AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="14afb-146">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)


