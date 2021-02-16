---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 798bb97b9e84121894341dd807bbaa9b3658a039
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170202"
---
# <span data-ttu-id="896fa-101">Remove-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="896fa-101">Remove-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="896fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="896fa-102">SYNOPSIS</span></span>
<span data-ttu-id="896fa-103">Löschen sie eine Zuordnung von Datensammlungsregel.</span><span class="sxs-lookup"><span data-stu-id="896fa-103">Delete a data collection rule association.</span></span>

## <span data-ttu-id="896fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="896fa-104">SYNTAX</span></span>

### <span data-ttu-id="896fa-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="896fa-105">ByName (Default)</span></span>
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

### <span data-ttu-id="896fa-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="896fa-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -InputObject <PSDataCollectionRuleAssociationProxyOnlyResource>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="896fa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="896fa-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -AssociationId <string>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="896fa-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="896fa-108">DESCRIPTION</span></span>
<span data-ttu-id="896fa-109">Das **Cmdlet "Remove-AzDataCollectionRuleAssociation"** löscht eine Datensammlungsregelassoziation (Data Collection Rule Association, DCRA).</span><span class="sxs-lookup"><span data-stu-id="896fa-109">The **Remove-AzDataCollectionRuleAssociation** cmdlet delete a data collection rule association (DCRA).</span></span>

<span data-ttu-id="896fa-110">Um eine DCR auf einen virtuellen Computer anzuwenden, erstellen Sie eine Zuordnung für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="896fa-110">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="896fa-111">Ein virtueller Computer kann eine Zuordnung zu mehreren DCRs haben, und einem DCR sind möglicherweise mehrere virtuelle Computer zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="896fa-111">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="896fa-112">Auf diese Weise können Sie eine Reihe von DCRs definieren, die jeweils einer bestimmten Anforderung gerecht werden, und sie nur auf die virtuellen Computer anwenden, auf die sie angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="896fa-112">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="896fa-113">Hier ist der [Artikel "Konfigurieren der Datensammlung für den Azure Monitor-Agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) mit DCRA.</span><span class="sxs-lookup"><span data-stu-id="896fa-113">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="896fa-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="896fa-114">EXAMPLES</span></span>

### <span data-ttu-id="896fa-115">Beispiel 1: Löschen der Zuordnung von Datensammlungsregel zu Parametern für Name und Zielressource (zugeordneter virtueller Computer)</span><span class="sxs-lookup"><span data-stu-id="896fa-115">Example 1: Delete data collection rule association with name and target resource ID (associated virtual machine) parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName
```

### <span data-ttu-id="896fa-116">Beispiel 2: Löschen einer Datensammlungsregel mit Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="896fa-116">Example 2: Delete data collection rule with Input Object</span></span>
```
PS C:\>$dcrAssoc | Remove-AzDataCollectionRule
```

### <span data-ttu-id="896fa-117">Beispiel 3: Löschen einer Datensammlungsregel mit der Eigenschaft "Zuordnungsressourcen-ID"</span><span class="sxs-lookup"><span data-stu-id="896fa-117">Example 3: Delete data collection rule with the association resource ID property</span></span>
```
PS C:\>Remove-AzDataCollectionRule -AssociationId $dcrAssoc.Id
```

## <span data-ttu-id="896fa-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="896fa-118">PARAMETERS</span></span>

### <span data-ttu-id="896fa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="896fa-119">-DefaultProfile</span></span>
<span data-ttu-id="896fa-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="896fa-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="896fa-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="896fa-121">-TargetResourceId</span></span>
<span data-ttu-id="896fa-122">Die zugeordnete Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="896fa-122">The associated resource ID.</span></span>

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

### <span data-ttu-id="896fa-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="896fa-123">-AssociationName</span></span>
<span data-ttu-id="896fa-124">Der Name der Zuordnungsressource.</span><span class="sxs-lookup"><span data-stu-id="896fa-124">The name of the association resource.</span></span>

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

### <span data-ttu-id="896fa-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="896fa-125">-InputObject</span></span>
<span data-ttu-id="896fa-126">PSDataCollectionRuleResource-Objekt</span><span class="sxs-lookup"><span data-stu-id="896fa-126">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="896fa-127">-AssociationId</span><span class="sxs-lookup"><span data-stu-id="896fa-127">-AssociationId</span></span>
<span data-ttu-id="896fa-128">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="896fa-128">The resource identifier.</span></span>

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

### <span data-ttu-id="896fa-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="896fa-129">-Confirm</span></span>
<span data-ttu-id="896fa-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="896fa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="896fa-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="896fa-131">-WhatIf</span></span>
<span data-ttu-id="896fa-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="896fa-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="896fa-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="896fa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="896fa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="896fa-134">CommonParameters</span></span>
<span data-ttu-id="896fa-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="896fa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="896fa-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="896fa-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="896fa-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="896fa-137">INPUTS</span></span>

### <span data-ttu-id="896fa-138">System.String</span><span class="sxs-lookup"><span data-stu-id="896fa-138">System.String</span></span>
###<span data-ttu-id="896fa-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="896fa-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="896fa-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="896fa-140">OUTPUTS</span></span>

### <span data-ttu-id="896fa-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="896fa-141">System.Boolean</span></span>

## <span data-ttu-id="896fa-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="896fa-142">NOTES</span></span>

## <span data-ttu-id="896fa-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="896fa-143">RELATED LINKS</span></span>

<span data-ttu-id="896fa-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="896fa-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span></span>
