---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: a2acea388b34b23d4977fa65ae6e6e6d4702525b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932304"
---
# <span data-ttu-id="e7a47-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="e7a47-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="e7a47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7a47-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a47-103">Aktualisiert verwaltete Anwendung</span><span class="sxs-lookup"><span data-stu-id="e7a47-103">Updates managed application</span></span>

## <span data-ttu-id="e7a47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7a47-104">SYNTAX</span></span>

### <span data-ttu-id="e7a47-105">SetByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="e7a47-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7a47-106">SetById</span><span class="sxs-lookup"><span data-stu-id="e7a47-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7a47-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7a47-107">DESCRIPTION</span></span>
<span data-ttu-id="e7a47-108">Das **Cmdlet Set-AzManagedApplication** aktualisiert verwaltete Anwendungen</span><span class="sxs-lookup"><span data-stu-id="e7a47-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="e7a47-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e7a47-109">EXAMPLES</span></span>

### <span data-ttu-id="e7a47-110">Beispiel 1: Beschreibung der Definition verwalteter Anwendungen aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e7a47-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="e7a47-111">Mit diesem Befehl wird die Beschreibung der verwalteten Anwendung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e7a47-111">This command updates the managed application description</span></span>

## <span data-ttu-id="e7a47-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e7a47-112">PARAMETERS</span></span>

### <span data-ttu-id="e7a47-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e7a47-113">-ApiVersion</span></span>
<span data-ttu-id="e7a47-114">Wenn festgelegt, gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="e7a47-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e7a47-115">Wenn nicht angegeben, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e7a47-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e7a47-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a47-116">-DefaultProfile</span></span>
<span data-ttu-id="e7a47-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7a47-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7a47-118">-ID</span><span class="sxs-lookup"><span data-stu-id="e7a47-118">-Id</span></span>
<span data-ttu-id="e7a47-119">Die vollqualifizierte verwaltete Anwendungs-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="e7a47-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="e7a47-120">z. B. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a47-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a47-121">-Kind</span><span class="sxs-lookup"><span data-stu-id="e7a47-121">-Kind</span></span>
<span data-ttu-id="e7a47-122">Die art der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e7a47-122">The managed application kind.</span></span>
<span data-ttu-id="e7a47-123">Eines der Marketplace- oder Servicecatalogs</span><span class="sxs-lookup"><span data-stu-id="e7a47-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="e7a47-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e7a47-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="e7a47-125">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e7a47-125">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a47-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a47-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="e7a47-127">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e7a47-127">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a47-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e7a47-128">-Name</span></span>
<span data-ttu-id="e7a47-129">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e7a47-129">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a47-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="e7a47-130">-Parameter</span></span>
<span data-ttu-id="e7a47-131">Die JSON formatierte Zeichenfolge mit Parametern für verwaltete Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="e7a47-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="e7a47-132">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameter enthält, oder die Parameter als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e7a47-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a47-133">-Plan</span><span class="sxs-lookup"><span data-stu-id="e7a47-133">-Plan</span></span>
<span data-ttu-id="e7a47-134">Eine Hashtabelle, die die Eigenschaften des Plans für verwaltete Anwendungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="e7a47-134">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a47-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="e7a47-135">-Pre</span></span>
<span data-ttu-id="e7a47-136">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7a47-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e7a47-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a47-137">-ResourceGroupName</span></span>
<span data-ttu-id="e7a47-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e7a47-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a47-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="e7a47-139">-Tag</span></span>
<span data-ttu-id="e7a47-140">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="e7a47-140">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a47-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e7a47-141">-Confirm</span></span>
<span data-ttu-id="e7a47-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7a47-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7a47-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7a47-143">-WhatIf</span></span>
<span data-ttu-id="e7a47-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7a47-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7a47-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7a47-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7a47-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a47-146">CommonParameters</span></span>
<span data-ttu-id="e7a47-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7a47-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a47-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7a47-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a47-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e7a47-149">INPUTS</span></span>

### <span data-ttu-id="e7a47-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e7a47-150">System.String</span></span>

### <span data-ttu-id="e7a47-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e7a47-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e7a47-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e7a47-152">OUTPUTS</span></span>

### <span data-ttu-id="e7a47-153">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="e7a47-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e7a47-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e7a47-154">NOTES</span></span>

## <span data-ttu-id="e7a47-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e7a47-155">RELATED LINKS</span></span>
