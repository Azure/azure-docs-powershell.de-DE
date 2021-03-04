---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 1a63d28664eb8ade22c87cfad3a21db0764cbceb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932651"
---
# <span data-ttu-id="06d66-101">Get-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="06d66-101">Get-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="06d66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06d66-102">SYNOPSIS</span></span>
<span data-ttu-id="06d66-103">Ruft zuordnungen von Datensammlungsregel(en) ab.</span><span class="sxs-lookup"><span data-stu-id="06d66-103">Gets data collection rule association(s).</span></span>

## <span data-ttu-id="06d66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06d66-104">SYNTAX</span></span>

### <span data-ttu-id="06d66-105">ByAssociatedResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="06d66-105">ByAssociatedResource (Default)</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="06d66-106">ByName</span><span class="sxs-lookup"><span data-stu-id="06d66-106">ByName</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   -AssociationName <string> 
   [-DefaultProfile <IAzureContextContainer>] 
   [<CommonParameters>]
```

### <span data-ttu-id="06d66-107">ByRule</span><span class="sxs-lookup"><span data-stu-id="06d66-107">ByRule</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="06d66-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="06d66-108">ByInputObject</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="06d66-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06d66-109">DESCRIPTION</span></span>
<span data-ttu-id="06d66-110">Das **Cmdlet Get-AzDataCollectionRuleAssociation** ruft eine oder mehrere Datensammlungsregelnzuordnungen (Data Collection Rules Associations, DCRA) ab.</span><span class="sxs-lookup"><span data-stu-id="06d66-110">The **Get-AzDataCollectionRuleAssociation** cmdlet gets one or more data collection rules associations (DCRA).</span></span>

<span data-ttu-id="06d66-111">Um eine DCR auf einen virtuellen Computer anzuwenden, erstellen Sie eine Zuordnung für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="06d66-111">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="06d66-112">Ein virtueller Computer kann eine Zuordnung zu mehreren DCRs haben, und einem DCR sind möglicherweise mehrere virtuelle Computer zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="06d66-112">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="06d66-113">Auf diese Weise können Sie eine Gruppe von DCRs definieren, die jeweils einer bestimmten Anforderung gerecht werden, und sie nur auf die virtuellen Computer anwenden, auf denen sie angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="06d66-113">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="06d66-114">Hier ist der [Artikel "Konfigurieren der Datensammlung für den Azure Monitor-Agent"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) mit DCRA.</span><span class="sxs-lookup"><span data-stu-id="06d66-114">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="06d66-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="06d66-115">EXAMPLES</span></span>

### <span data-ttu-id="06d66-116">Beispiel 1: Erhalten von Zuordnungen zu Datensammlungsregeln nach Zielressourcen-ID (zugeordneter virtueller Computer)</span><span class="sxs-lookup"><span data-stu-id="06d66-116">Example 1: Get data collection rules associations by target resource ID (associated virtual machine)</span></span>
```
PS C:\>$vm = Get-AzVM -ResourceGroupName $rg -Name $vmName
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="06d66-117">Mit diesem Befehl werden alle Datensammlungsregeln für die angegebene Zielressourcen-ID (virtueller Computer) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="06d66-117">This command lists all the data collection rules for the given target resource ID (virtual machine).</span></span>

### <span data-ttu-id="06d66-118">Beispiel 2: Erhalten von Zuordnungen von Datensammlungsregeln nach Regel (DCR)</span><span class="sxs-lookup"><span data-stu-id="06d66-118">Example 2: Get data collection rules associations by rule (DCR)</span></span>
```
PS C:\>Get-AzDataCollectionRuleAssociation -ResourceGroup $rg -RuleName $dcrName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="06d66-119">Mit diesem Befehl werden Zuordnungen von Datensammlungsregeln für die angegebene Ressourcengruppe und -regel (DCR) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="06d66-119">This command lists data collection rules associations for the given resource group and rule (DCR).</span></span>

### <span data-ttu-id="06d66-120">Beispiel 3: Rufen Sie Datensammlungsregelzuordnungen nach Eingabeobjekt ab (PSDataCollectionRuleResource)</span><span class="sxs-lookup"><span data-stu-id="06d66-120">Example 3: Get data collection rule associations by input object (PSDataCollectionRuleResource)</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$dcr | Get-AzDataCollectionRuleAssociation

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="06d66-121">Mit diesem Befehl werden Zuordnungen von Datensammlungsregeln für das angegebene Eingabeobjekt aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="06d66-121">This command lists data collection rules associations for the given input object.</span></span>

### <span data-ttu-id="06d66-122">Beispiel 4: Erhalten einer Zuordnung einer Datensammlungsregel nach Zielressourcen-ID (zugeordneter virtueller Computer) und Zuordnungsname</span><span class="sxs-lookup"><span data-stu-id="06d66-122">Example 4: Get a data collection rule association by target resource ID (associated virtual machine) and association name</span></span>
```
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="06d66-123">Mit diesem Befehl wird eine (eine Liste mit einem einzelnen Element) der Datensammlungsregel-Zuordnung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="06d66-123">This command lists one (a list with a single element) data collection rule association.</span></span>

## <span data-ttu-id="06d66-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="06d66-124">PARAMETERS</span></span>

### <span data-ttu-id="06d66-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d66-125">-DefaultProfile</span></span>
<span data-ttu-id="06d66-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="06d66-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06d66-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="06d66-127">-TargetResourceId</span></span>
<span data-ttu-id="06d66-128">Die zugeordnete Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="06d66-128">The associated resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByAssociatedResource (Default)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d66-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d66-129">-ResourceGroupName</span></span>
<span data-ttu-id="06d66-130">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="06d66-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d66-131">-RuleName</span><span class="sxs-lookup"><span data-stu-id="06d66-131">-RuleName</span></span>
<span data-ttu-id="06d66-132">Name der Datensammlungsregel</span><span class="sxs-lookup"><span data-stu-id="06d66-132">The data collection rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases: DataCollectionRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d66-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06d66-133">-InputObject</span></span>
<span data-ttu-id="06d66-134">PSDataCollectionRuleResource-Objekt</span><span class="sxs-lookup"><span data-stu-id="06d66-134">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="06d66-135">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="06d66-135">-AssociationName</span></span>
<span data-ttu-id="06d66-136">Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="06d66-136">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d66-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d66-137">CommonParameters</span></span>
<span data-ttu-id="06d66-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d66-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d66-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06d66-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d66-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="06d66-140">INPUTS</span></span>

### <span data-ttu-id="06d66-141">System.String</span><span class="sxs-lookup"><span data-stu-id="06d66-141">System.String</span></span>
### <span data-ttu-id="06d66-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="06d66-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="06d66-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="06d66-143">OUTPUTS</span></span>

### <span data-ttu-id="06d66-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="06d66-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="06d66-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="06d66-145">NOTES</span></span>

## <span data-ttu-id="06d66-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="06d66-146">RELATED LINKS</span></span>

<span data-ttu-id="06d66-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="06d66-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span></span>
