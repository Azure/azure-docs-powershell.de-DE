---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 8b5b9e8cfd1909b0d91627a2c0600620f264da78
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174380"
---
# <span data-ttu-id="6716f-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="6716f-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="6716f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6716f-102">SYNOPSIS</span></span>
<span data-ttu-id="6716f-103">Entfernt einen Datenfluss aus Data Factory.</span><span class="sxs-lookup"><span data-stu-id="6716f-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="6716f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6716f-104">SYNTAX</span></span>

### <span data-ttu-id="6716f-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6716f-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6716f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6716f-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6716f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6716f-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6716f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6716f-108">DESCRIPTION</span></span>
<span data-ttu-id="6716f-109">Das Remove-AzDataFactoryV2DataFlow-Cmdlet entfernt einen Datenfluss aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="6716f-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="6716f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6716f-110">EXAMPLES</span></span>

### <span data-ttu-id="6716f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6716f-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="6716f-112">Dieser Befehl entfernt den Datenfluss mit dem Namen dataflow5 aus der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="6716f-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="6716f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6716f-113">PARAMETERS</span></span>

### <span data-ttu-id="6716f-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6716f-114">-DataFactoryName</span></span>
<span data-ttu-id="6716f-115">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="6716f-115">The data factory name.</span></span>

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

### <span data-ttu-id="6716f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6716f-116">-DefaultProfile</span></span>
<span data-ttu-id="6716f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6716f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6716f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6716f-118">-Force</span></span>
<span data-ttu-id="6716f-119">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="6716f-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6716f-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6716f-120">-InputObject</span></span>
<span data-ttu-id="6716f-121">Das Datenflussobjekt.</span><span class="sxs-lookup"><span data-stu-id="6716f-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6716f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6716f-122">-Name</span></span>
<span data-ttu-id="6716f-123">Der Name des Datenflusses.</span><span class="sxs-lookup"><span data-stu-id="6716f-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6716f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6716f-124">-ResourceGroupName</span></span>
<span data-ttu-id="6716f-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6716f-125">The resource group name.</span></span>

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

### <span data-ttu-id="6716f-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6716f-126">-ResourceId</span></span>
<span data-ttu-id="6716f-127">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6716f-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6716f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6716f-128">-PassThru</span></span>
<span data-ttu-id="6716f-129">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="6716f-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="6716f-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6716f-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="6716f-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6716f-131">-Confirm</span></span>
<span data-ttu-id="6716f-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6716f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6716f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6716f-133">-WhatIf</span></span>
<span data-ttu-id="6716f-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6716f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6716f-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6716f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6716f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6716f-136">CommonParameters</span></span>
<span data-ttu-id="6716f-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6716f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6716f-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6716f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6716f-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6716f-139">INPUTS</span></span>

### <span data-ttu-id="6716f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="6716f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="6716f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6716f-141">System.String</span></span>

## <span data-ttu-id="6716f-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6716f-142">OUTPUTS</span></span>

### <span data-ttu-id="6716f-143">System. void</span><span class="sxs-lookup"><span data-stu-id="6716f-143">System.Void</span></span>

### <span data-ttu-id="6716f-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6716f-144">System.Boolean</span></span>

## <span data-ttu-id="6716f-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="6716f-145">NOTES</span></span>
<span data-ttu-id="6716f-146">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="6716f-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6716f-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6716f-147">RELATED LINKS</span></span>

[<span data-ttu-id="6716f-148">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="6716f-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="6716f-149">Satz-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="6716f-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

