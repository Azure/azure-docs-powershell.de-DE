---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 87830eb9cb4321bf9af1476d3fa5a0db41796351
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936768"
---
# <span data-ttu-id="d5356-101">Remove-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="d5356-101">Remove-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="d5356-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5356-102">SYNOPSIS</span></span>
<span data-ttu-id="d5356-103">Löschen sie eine Zuordnung einer Datensammlungsregel.</span><span class="sxs-lookup"><span data-stu-id="d5356-103">Delete a data collection rule association.</span></span>

## <span data-ttu-id="d5356-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5356-104">SYNTAX</span></span>

### <span data-ttu-id="d5356-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5356-105">ByName (Default)</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -TargetResourceId <string> 
      -AssociationName <string> 
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="d5356-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d5356-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -InputObject <PSDataCollectionRuleAssociationProxyOnlyResource>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="d5356-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d5356-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -AssociationId <string>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="d5356-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5356-108">DESCRIPTION</span></span>
<span data-ttu-id="d5356-109">Das **Cmdlet Remove-AzDataCollectionRuleAssociation** löscht eine Datensammlungsregel-Zuordnung (Data Collection Rule Association, DCRA).</span><span class="sxs-lookup"><span data-stu-id="d5356-109">The **Remove-AzDataCollectionRuleAssociation** cmdlet delete a data collection rule association (DCRA).</span></span>

<span data-ttu-id="d5356-110">Um eine DCR auf einen virtuellen Computer anzuwenden, erstellen Sie eine Zuordnung für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d5356-110">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="d5356-111">Ein virtueller Computer kann eine Zuordnung zu mehreren DCRs haben, und einem DCR sind möglicherweise mehrere virtuelle Computer zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d5356-111">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="d5356-112">Auf diese Weise können Sie eine Gruppe von DCRs definieren, die jeweils einer bestimmten Anforderung gerecht werden, und sie nur auf die virtuellen Computer anwenden, auf denen sie angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5356-112">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="d5356-113">Hier ist der [Artikel "Konfigurieren der Datensammlung für den Azure Monitor-Agent"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) mit DCRA.</span><span class="sxs-lookup"><span data-stu-id="d5356-113">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="d5356-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5356-114">EXAMPLES</span></span>

### <span data-ttu-id="d5356-115">Beispiel 1: Löschen der Datensammlungsregelzuordnung mit Parametern für Name und Zielressourcen-ID (zugeordneter virtueller Computer)</span><span class="sxs-lookup"><span data-stu-id="d5356-115">Example 1: Delete data collection rule association with name and target resource ID (associated virtual machine) parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName
```

### <span data-ttu-id="d5356-116">Beispiel 2: Löschen der Datensammlungsregel mit Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="d5356-116">Example 2: Delete data collection rule with Input Object</span></span>
```
PS C:\>$dcrAssoc | Remove-AzDataCollectionRule
```

### <span data-ttu-id="d5356-117">Beispiel 3: Löschen der Datensammlungsregel mit der Eigenschaft "Zuordnungsressourcen-ID"</span><span class="sxs-lookup"><span data-stu-id="d5356-117">Example 3: Delete data collection rule with the association resource ID property</span></span>
```
PS C:\>Remove-AzDataCollectionRule -AssociationId $dcrAssoc.Id
```

## <span data-ttu-id="d5356-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d5356-118">PARAMETERS</span></span>

### <span data-ttu-id="d5356-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5356-119">-DefaultProfile</span></span>
<span data-ttu-id="d5356-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d5356-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5356-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d5356-121">-TargetResourceId</span></span>
<span data-ttu-id="d5356-122">Die zugeordnete Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d5356-122">The associated resource ID.</span></span>

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

### <span data-ttu-id="d5356-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="d5356-123">-AssociationName</span></span>
<span data-ttu-id="d5356-124">Der Name der Zuordnungsressource.</span><span class="sxs-lookup"><span data-stu-id="d5356-124">The name of the association resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName (Default)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5356-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5356-125">-InputObject</span></span>
<span data-ttu-id="d5356-126">PSDataCollectionRuleResource-Objekt</span><span class="sxs-lookup"><span data-stu-id="d5356-126">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="d5356-127">-AssociationId</span><span class="sxs-lookup"><span data-stu-id="d5356-127">-AssociationId</span></span>
<span data-ttu-id="d5356-128">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="d5356-128">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5356-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d5356-129">-Confirm</span></span>
<span data-ttu-id="d5356-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5356-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5356-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5356-131">-WhatIf</span></span>
<span data-ttu-id="d5356-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5356-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5356-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5356-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5356-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5356-134">CommonParameters</span></span>
<span data-ttu-id="d5356-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5356-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5356-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5356-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5356-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5356-137">INPUTS</span></span>

### <span data-ttu-id="d5356-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d5356-138">System.String</span></span>
###<span data-ttu-id="d5356-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="d5356-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="d5356-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5356-140">OUTPUTS</span></span>

### <span data-ttu-id="d5356-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d5356-141">System.Boolean</span></span>

## <span data-ttu-id="d5356-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d5356-142">NOTES</span></span>

## <span data-ttu-id="d5356-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d5356-143">RELATED LINKS</span></span>

<span data-ttu-id="d5356-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="d5356-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span></span>
