---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 144e67a2e58aeaa7fe7aa424ddc79bfca4aaa538
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147420"
---
# <span data-ttu-id="8da3f-101">Get-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="8da3f-101">Get-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="8da3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8da3f-102">SYNOPSIS</span></span>
<span data-ttu-id="8da3f-103">Ruft die Zuordnung(en) von Datensammlungsregel ab.</span><span class="sxs-lookup"><span data-stu-id="8da3f-103">Gets data collection rule association(s).</span></span>

## <span data-ttu-id="8da3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8da3f-104">SYNTAX</span></span>

### <span data-ttu-id="8da3f-105">ByAssociatedResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="8da3f-105">ByAssociatedResource (Default)</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="8da3f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8da3f-106">ByName</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   -AssociationName <string> 
   [-DefaultProfile <IAzureContextContainer>] 
   [<CommonParameters>]
```

### <span data-ttu-id="8da3f-107">ByRule</span><span class="sxs-lookup"><span data-stu-id="8da3f-107">ByRule</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="8da3f-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8da3f-108">ByInputObject</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="8da3f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8da3f-109">DESCRIPTION</span></span>
<span data-ttu-id="8da3f-110">Das **Cmdlet "Get-AzDataCollectionRuleAssociation"** ruft eine oder mehrere Datensammlungsregelnzuordnungen (Data Collection Rules Associations, DCRA) ab.</span><span class="sxs-lookup"><span data-stu-id="8da3f-110">The **Get-AzDataCollectionRuleAssociation** cmdlet gets one or more data collection rules associations (DCRA).</span></span>

<span data-ttu-id="8da3f-111">Um eine DCR auf einen virtuellen Computer anzuwenden, erstellen Sie eine Zuordnung für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="8da3f-111">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="8da3f-112">Ein virtueller Computer kann eine Zuordnung zu mehreren DCRs haben, und einem DCR sind möglicherweise mehrere virtuelle Computer zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8da3f-112">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="8da3f-113">Auf diese Weise können Sie eine Reihe von DCRs definieren, die jeweils einer bestimmten Anforderung gerecht werden, und sie nur auf die virtuellen Computer anwenden, auf die sie angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8da3f-113">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="8da3f-114">Hier ist der [Artikel "Konfigurieren der Datensammlung für den Azure Monitor-Agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) mit DCRA.</span><span class="sxs-lookup"><span data-stu-id="8da3f-114">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="8da3f-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8da3f-115">EXAMPLES</span></span>

### <span data-ttu-id="8da3f-116">Beispiel 1: Erhalten von Datensammlungsregelnzuordnungen nach Zielressourcen-ID (zugeordneter virtueller Computer)</span><span class="sxs-lookup"><span data-stu-id="8da3f-116">Example 1: Get data collection rules associations by target resource ID (associated virtual machine)</span></span>
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

<span data-ttu-id="8da3f-117">Dieser Befehl listet alle Datensammlungsregeln für die angegebene Zielressourcen-ID (virtueller Computer) auf.</span><span class="sxs-lookup"><span data-stu-id="8da3f-117">This command lists all the data collection rules for the given target resource ID (virtual machine).</span></span>

### <span data-ttu-id="8da3f-118">Beispiel 2: Erhalten von Zuordnungen von Datensammlungsregeln nach Regel (DCR)</span><span class="sxs-lookup"><span data-stu-id="8da3f-118">Example 2: Get data collection rules associations by rule (DCR)</span></span>
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

<span data-ttu-id="8da3f-119">Dieser Befehl listet Datensammlungsregelnzuordnungen für die angegebene Ressourcengruppe und -regel auf.</span><span class="sxs-lookup"><span data-stu-id="8da3f-119">This command lists data collection rules associations for the given resource group and rule (DCR).</span></span>

### <span data-ttu-id="8da3f-120">Beispiel 3: Rufen Sie Datensammlungsregelzuordnungen nach Eingabeobjekt ab (PSDataCollectionRuleResource)</span><span class="sxs-lookup"><span data-stu-id="8da3f-120">Example 3: Get data collection rule associations by input object (PSDataCollectionRuleResource)</span></span>
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

<span data-ttu-id="8da3f-121">Dieser Befehl listet die Zuordnungen von Datensammlungsregeln für das angegebene Eingabeobjekt auf.</span><span class="sxs-lookup"><span data-stu-id="8da3f-121">This command lists data collection rules associations for the given input object.</span></span>

### <span data-ttu-id="8da3f-122">Beispiel 4: Erhalten einer Datensammlungsregelzuordnung nach Zielressourcen-ID (zugeordneter virtueller Computer) und Zuordnungsname</span><span class="sxs-lookup"><span data-stu-id="8da3f-122">Example 4: Get a data collection rule association by target resource ID (associated virtual machine) and association name</span></span>
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

<span data-ttu-id="8da3f-123">Mit diesem Befehl wird eine Datensammlungsregel zuordnung (eine Liste mit einem einzelnen Element) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8da3f-123">This command lists one (a list with a single element) data collection rule association.</span></span>

## <span data-ttu-id="8da3f-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8da3f-124">PARAMETERS</span></span>

### <span data-ttu-id="8da3f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da3f-125">-DefaultProfile</span></span>
<span data-ttu-id="8da3f-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8da3f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8da3f-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8da3f-127">-TargetResourceId</span></span>
<span data-ttu-id="8da3f-128">Die zugeordnete Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="8da3f-128">The associated resource ID</span></span>

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

### <span data-ttu-id="8da3f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8da3f-129">-ResourceGroupName</span></span>
<span data-ttu-id="8da3f-130">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8da3f-130">The resource group name</span></span>

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

### <span data-ttu-id="8da3f-131">-RuleName</span><span class="sxs-lookup"><span data-stu-id="8da3f-131">-RuleName</span></span>
<span data-ttu-id="8da3f-132">Name der Datensammlungsregel</span><span class="sxs-lookup"><span data-stu-id="8da3f-132">The data collection rule name</span></span>

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

### <span data-ttu-id="8da3f-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8da3f-133">-InputObject</span></span>
<span data-ttu-id="8da3f-134">PSDataCollectionRuleResource-Objekt</span><span class="sxs-lookup"><span data-stu-id="8da3f-134">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="8da3f-135">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="8da3f-135">-AssociationName</span></span>
<span data-ttu-id="8da3f-136">Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="8da3f-136">The name of the association.</span></span>

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

### <span data-ttu-id="8da3f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da3f-137">CommonParameters</span></span>
<span data-ttu-id="8da3f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da3f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da3f-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8da3f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da3f-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8da3f-140">INPUTS</span></span>

### <span data-ttu-id="8da3f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8da3f-141">System.String</span></span>
### <span data-ttu-id="8da3f-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="8da3f-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="8da3f-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8da3f-143">OUTPUTS</span></span>

### <span data-ttu-id="8da3f-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="8da3f-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="8da3f-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8da3f-145">NOTES</span></span>

## <span data-ttu-id="8da3f-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8da3f-146">RELATED LINKS</span></span>

<span data-ttu-id="8da3f-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="8da3f-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span></span>
