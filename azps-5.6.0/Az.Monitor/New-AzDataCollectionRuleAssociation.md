---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 1086f67bcec4adeef74fe7bf591e61d9d08a90e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934907"
---
# <span data-ttu-id="b1fc8-101">New-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="b1fc8-101">New-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="b1fc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="b1fc8-103">Erstellen sie die Zuordnung von Datensammlungsregel.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-103">Create data collection rule association.</span></span>

## <span data-ttu-id="b1fc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1fc8-104">SYNTAX</span></span>

### <span data-ttu-id="b1fc8-105">ByDataCollectionRuleId (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1fc8-105">ByDataCollectionRuleId (Default)</span></span>
```
New-AzDataCollectionRuleAssociation
   -TargetResourceId <string>
   -AssociationName <string>
   -RuleId <string>
   [-Description <string>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="b1fc8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b1fc8-106">ByInputObject</span></span>
```
New-AzDataCollectionRuleAssociation
   -TargetResourceId <string>
   -AssociationName <string>
   -InputObject <PSDataCollectionRuleResource>
   [-Description <string>]
   [-DefaultProfile <IAzureContextContainer>]  
   [-WhatIf]   
   [-Confirm]   
   [<CommonParameters>]
```


## <span data-ttu-id="b1fc8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1fc8-107">DESCRIPTION</span></span>
<span data-ttu-id="b1fc8-108">Das **Cmdlet New-AzDataCollectionRuleAssociation** erstellt eine Datensammlungsregeln-Zuordnung (Data Collection Rules Association, DCRA).</span><span class="sxs-lookup"><span data-stu-id="b1fc8-108">The **New-AzDataCollectionRuleAssociation** cmdlet creates a data collection rules association (DCRA).</span></span>

<span data-ttu-id="b1fc8-109">Um eine DCR auf einen virtuellen Computer anzuwenden, erstellen Sie eine Zuordnung für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-109">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="b1fc8-110">Ein virtueller Computer kann eine Zuordnung zu mehreren DCRs haben, und einem DCR sind möglicherweise mehrere virtuelle Computer zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-110">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="b1fc8-111">Auf diese Weise können Sie eine Gruppe von DCRs definieren, die jeweils einer bestimmten Anforderung gerecht werden, und sie nur auf die virtuellen Computer anwenden, auf denen sie angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-111">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="b1fc8-112">Hier ist der [Artikel "Konfigurieren der Datensammlung für den Azure Monitor-Agent"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) mit DCRA.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-112">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="b1fc8-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b1fc8-113">EXAMPLES</span></span>

### <span data-ttu-id="b1fc8-114">Beispiel 1: Erstellen der Zuordnung von Datensammlungsregel</span><span class="sxs-lookup"><span data-stu-id="b1fc8-114">Example 1: Create data collection rule association</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$vmId = '/subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}'
PS C:\>New-AzDataCollectionRuleAssociation -TargetResourceId $vmId -AssociationName "dcrAssoc" -RuleId $dcr.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Insights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/dcrAssoc
Name                 : dcrAssoc
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="b1fc8-115">Mit diesem Befehl wird eine Datensammlungsregelzuordnung für eine bestimmte Regel und Zielressourcen-ID erstellt.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-115">This command creates a data collection rule association for given rule and target resource ID.</span></span>

### <span data-ttu-id="b1fc8-116">Beispiel 2: Erstellen der Zuordnung von Datensammlungsregel aus einem DCR-Objekt</span><span class="sxs-lookup"><span data-stu-id="b1fc8-116">Example 2: Create data collection rule association from a DCR object</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$vmId = '/subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}'
PS C:\>$dcr | New-AzDataCollectionRuleAssociation -TargetResourceId $vmId -AssociationName "dcrAssocInput"

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Insights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/dcrAssocInput
Name                 : dcrAssocInput
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="b1fc8-117">Mit diesem Befehl wird eine Datensammlungsregelzuordnung für eine bestimmte Regel und Zielressourcen-ID erstellt.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-117">This command creates a data collection rule association for given rule and target resource ID.</span></span>

## <span data-ttu-id="b1fc8-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b1fc8-118">PARAMETERS</span></span>

### <span data-ttu-id="b1fc8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1fc8-119">-DefaultProfile</span></span>
<span data-ttu-id="b1fc8-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b1fc8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1fc8-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b1fc8-121">-TargetResourceId</span></span>
<span data-ttu-id="b1fc8-122">Die zu zuordnende Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b1fc8-122">The resource ID to associate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc8-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="b1fc8-123">-AssociationName</span></span>
<span data-ttu-id="b1fc8-124">Der Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="b1fc8-124">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc8-125">-RuleId</span><span class="sxs-lookup"><span data-stu-id="b1fc8-125">-RuleId</span></span>
<span data-ttu-id="b1fc8-126">Die Datensammlungsregel-ID</span><span class="sxs-lookup"><span data-stu-id="b1fc8-126">The data collection rule ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByDataCollectionRuleId
Aliases: DataCollectionRuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1fc8-127">-InputObject</span></span>
<span data-ttu-id="b1fc8-128">PSDataCollectionRuleResource-Objekt</span><span class="sxs-lookup"><span data-stu-id="b1fc8-128">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc8-129">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1fc8-129">-Description</span></span>
<span data-ttu-id="b1fc8-130">Ressourcenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="b1fc8-130">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc8-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1fc8-131">-Confirm</span></span>
<span data-ttu-id="b1fc8-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1fc8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1fc8-133">-WhatIf</span></span>
<span data-ttu-id="b1fc8-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1fc8-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1fc8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1fc8-136">CommonParameters</span></span>
<span data-ttu-id="b1fc8-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1fc8-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1fc8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1fc8-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b1fc8-139">INPUTS</span></span>

### <span data-ttu-id="b1fc8-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b1fc8-140">System.String</span></span>

## <span data-ttu-id="b1fc8-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b1fc8-141">OUTPUTS</span></span>

### <span data-ttu-id="b1fc8-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="b1fc8-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="b1fc8-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b1fc8-143">NOTES</span></span>

## <span data-ttu-id="b1fc8-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b1fc8-144">RELATED LINKS</span></span>

<span data-ttu-id="b1fc8-145">[Set-AzDataCollectionRuleAssociation](./Set-AzDataCollectionRuleAssociation.md) 
 [Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [Get-AzDataCollectionRuleAssociation](./Get-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="b1fc8-145">[Set-AzDataCollectionRuleAssociation](./Set-AzDataCollectionRuleAssociation.md)
[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[Get-AzDataCollectionRuleAssociation](./Get-AzDataCollectionRuleAssociation.md)</span></span>
