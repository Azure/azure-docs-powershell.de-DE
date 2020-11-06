---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: dec686838bd7826b57e7b158f4ed741608eaf782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478542"
---
# <span data-ttu-id="d7f33-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d7f33-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="d7f33-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7f33-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f33-103">Entfernt eine Pipeline aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d7f33-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7f33-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7f33-104">SYNTAX</span></span>

### <span data-ttu-id="d7f33-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d7f33-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7f33-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d7f33-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7f33-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7f33-107">DESCRIPTION</span></span>
<span data-ttu-id="d7f33-108">Das Cmdlet **Remove-AzureRmDataFactoryPipeline** entfernt eine Pipeline aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d7f33-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="d7f33-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7f33-109">EXAMPLES</span></span>

### <span data-ttu-id="d7f33-110">Beispiel 1: Entfernen einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="d7f33-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="d7f33-111">Dieses Cmdlet entfernt die Pipeline mit dem Namen DPWikisample aus der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d7f33-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="d7f33-112">Der Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="d7f33-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="d7f33-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7f33-113">PARAMETERS</span></span>

### <span data-ttu-id="d7f33-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d7f33-114">-DataFactory</span></span>
<span data-ttu-id="d7f33-115">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d7f33-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d7f33-116">Dieses Cmdlet entfernt eine Pipeline aus der Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d7f33-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f33-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d7f33-117">-DataFactoryName</span></span>
<span data-ttu-id="d7f33-118">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="d7f33-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d7f33-119">Dieses Cmdlet entfernt eine Pipeline aus der Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d7f33-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f33-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f33-120">-DefaultProfile</span></span>
<span data-ttu-id="d7f33-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d7f33-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7f33-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d7f33-122">-Force</span></span>
<span data-ttu-id="d7f33-123">Gibt an, dass dieses Cmdlet eine Pipeline entfernt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="d7f33-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f33-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d7f33-124">-Name</span></span>
<span data-ttu-id="d7f33-125">Gibt den Namen der zu entfernenden Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="d7f33-125">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f33-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7f33-126">-ResourceGroupName</span></span>
<span data-ttu-id="d7f33-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d7f33-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d7f33-128">Dieses Cmdlet entfernt eine Pipeline aus der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d7f33-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f33-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7f33-129">-Confirm</span></span>
<span data-ttu-id="d7f33-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7f33-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f33-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7f33-131">-WhatIf</span></span>
<span data-ttu-id="d7f33-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7f33-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7f33-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7f33-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f33-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f33-134">CommonParameters</span></span>
<span data-ttu-id="d7f33-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7f33-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f33-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7f33-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f33-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7f33-137">INPUTS</span></span>

### <span data-ttu-id="d7f33-138">Keine</span><span class="sxs-lookup"><span data-stu-id="d7f33-138">None</span></span>
<span data-ttu-id="d7f33-139">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d7f33-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7f33-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7f33-140">OUTPUTS</span></span>

### <span data-ttu-id="d7f33-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7f33-141">System.Boolean</span></span>

## <span data-ttu-id="d7f33-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7f33-142">NOTES</span></span>
* <span data-ttu-id="d7f33-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="d7f33-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d7f33-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7f33-144">RELATED LINKS</span></span>

[<span data-ttu-id="d7f33-145">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d7f33-145">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="d7f33-146">Neu – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d7f33-146">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="d7f33-147">Lebenslauf-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d7f33-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="d7f33-148">Satz-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="d7f33-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="d7f33-149">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d7f33-149">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


