---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
ms.openlocfilehash: 4dfa9417b2bce7473b3d2986f503c163cb6bf42f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930016"
---
# <span data-ttu-id="39be1-101">Remove-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="39be1-101">Remove-AzDataCollectionRule</span></span>

## <span data-ttu-id="39be1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39be1-102">SYNOPSIS</span></span>
<span data-ttu-id="39be1-103">Löschen sie eine Datensammlungsregel.</span><span class="sxs-lookup"><span data-stu-id="39be1-103">Delete a data collection rule.</span></span>

## <span data-ttu-id="39be1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39be1-104">SYNTAX</span></span>

### <span data-ttu-id="39be1-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="39be1-105">ByName (Default)</span></span>
```
Remove-AzDataCollectionRule
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="39be1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="39be1-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRule
   -InputObject <PSDataCollectionRuleResource>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="39be1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="39be1-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRule
   -RuleId <string>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="39be1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39be1-108">DESCRIPTION</span></span>
<span data-ttu-id="39be1-109">Das **Cmdlet Remove-AzDataCollectionRule** löscht eine Datensammlungsregel.</span><span class="sxs-lookup"><span data-stu-id="39be1-109">The **Remove-AzDataCollectionRule** cmdlet delete a data collection rule.</span></span>

<span data-ttu-id="39be1-110">Datensammlungsregeln (Data Collection Rules, DCR) definieren Daten, die in Azure Monitor übermittelt werden, und geben an, wo diese Daten gesendet oder gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="39be1-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="39be1-111">Hier finden Sie den vollständigen [DCR-Übersichtsartikel](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span><span class="sxs-lookup"><span data-stu-id="39be1-111">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="39be1-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39be1-112">EXAMPLES</span></span>

### <span data-ttu-id="39be1-113">Beispiel 1: Löschen der Datensammlungsregel mit Parametern für Name und Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="39be1-113">Example 1: Delete data collection rule with name and resource group parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr"             
```

### <span data-ttu-id="39be1-114">Beispiel 2: Löschen der Datensammlungsregel mit Rückgabe boolescher Namen und Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="39be1-114">Example 2: Delete data collection rule with name and resource group return bool</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr" -PassThru

True
```

### <span data-ttu-id="39be1-115">Beispiel 3: Löschen der Datensammlungsregel aus InputObject</span><span class="sxs-lookup"><span data-stu-id="39be1-115">Example 3: Delete data collection rule from InputObject</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroupName "testdcr" -RuleName "dcrFromPipe95" | Remove-AzDataCollectionRule
```

### <span data-ttu-id="39be1-116">Beispiel 4: Löschen der Datensammlungsregel aus der Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="39be1-116">Example 4: Delete data collection rule from resource id</span></span>
```
PS C:\>Remove-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/{dcrName}"
```

## <span data-ttu-id="39be1-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="39be1-117">PARAMETERS</span></span>

### <span data-ttu-id="39be1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39be1-118">-DefaultProfile</span></span>
<span data-ttu-id="39be1-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="39be1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39be1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39be1-120">-ResourceGroupName</span></span>
<span data-ttu-id="39be1-121">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="39be1-121">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39be1-122">-RuleName</span><span class="sxs-lookup"><span data-stu-id="39be1-122">-RuleName</span></span>
<span data-ttu-id="39be1-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="39be1-123">The resource name.</span></span>

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

### <span data-ttu-id="39be1-124">-RuleId</span><span class="sxs-lookup"><span data-stu-id="39be1-124">-RuleId</span></span>
<span data-ttu-id="39be1-125">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="39be1-125">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39be1-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39be1-126">-Confirm</span></span>
<span data-ttu-id="39be1-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39be1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39be1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39be1-128">-WhatIf</span></span>
<span data-ttu-id="39be1-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39be1-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39be1-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39be1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39be1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39be1-131">CommonParameters</span></span>
<span data-ttu-id="39be1-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39be1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39be1-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39be1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39be1-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39be1-134">INPUTS</span></span>

### <span data-ttu-id="39be1-135">System.String</span><span class="sxs-lookup"><span data-stu-id="39be1-135">System.String</span></span>

## <span data-ttu-id="39be1-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39be1-136">OUTPUTS</span></span>

### <span data-ttu-id="39be1-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="39be1-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="39be1-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="39be1-138">NOTES</span></span>

## <span data-ttu-id="39be1-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="39be1-139">RELATED LINKS</span></span>

<span data-ttu-id="39be1-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="39be1-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>