---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: 3d8445c78ae2f11fef734db0b24319b524f55704
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996440"
---
# <span data-ttu-id="bdc57-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="bdc57-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="bdc57-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bdc57-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc57-103">Verwaltete Anwendung für Updates</span><span class="sxs-lookup"><span data-stu-id="bdc57-103">Updates managed application</span></span>

## <span data-ttu-id="bdc57-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdc57-104">SYNTAX</span></span>

### <span data-ttu-id="bdc57-105">SetByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="bdc57-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdc57-106">SetById</span><span class="sxs-lookup"><span data-stu-id="bdc57-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdc57-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bdc57-107">DESCRIPTION</span></span>
<span data-ttu-id="bdc57-108">Das Cmdlet " **Satz-AzManagedApplication** " aktualisiert verwaltete Anwendungen</span><span class="sxs-lookup"><span data-stu-id="bdc57-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="bdc57-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdc57-109">EXAMPLES</span></span>

### <span data-ttu-id="bdc57-110">Beispiel 1: Aktualisieren der Definitionsbeschreibung für verwaltete Anwendungen</span><span class="sxs-lookup"><span data-stu-id="bdc57-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="bdc57-111">Mit diesem Befehl wird die Beschreibung der verwalteten Anwendung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bdc57-111">This command updates the managed application description</span></span>

## <span data-ttu-id="bdc57-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdc57-112">PARAMETERS</span></span>

### <span data-ttu-id="bdc57-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bdc57-113">-ApiVersion</span></span>
<span data-ttu-id="bdc57-114">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bdc57-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="bdc57-115">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="bdc57-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="bdc57-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc57-116">-DefaultProfile</span></span>
<span data-ttu-id="bdc57-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bdc57-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdc57-118">-ID</span><span class="sxs-lookup"><span data-stu-id="bdc57-118">-Id</span></span>
<span data-ttu-id="bdc57-119">Die vollqualifizierte verwaltete Anwendungs-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="bdc57-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="bdc57-120">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc57-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="bdc57-121">-Art</span><span class="sxs-lookup"><span data-stu-id="bdc57-121">-Kind</span></span>
<span data-ttu-id="bdc57-122">Die Art der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="bdc57-122">The managed application kind.</span></span>
<span data-ttu-id="bdc57-123">Eine der Marketplace-oder servicecatalog</span><span class="sxs-lookup"><span data-stu-id="bdc57-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="bdc57-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="bdc57-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="bdc57-125">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bdc57-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="bdc57-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc57-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="bdc57-127">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bdc57-127">The managed resource group name.</span></span>

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

### <span data-ttu-id="bdc57-128">-Name</span><span class="sxs-lookup"><span data-stu-id="bdc57-128">-Name</span></span>
<span data-ttu-id="bdc57-129">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="bdc57-129">The managed application name.</span></span>

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

### <span data-ttu-id="bdc57-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="bdc57-130">-Parameter</span></span>
<span data-ttu-id="bdc57-131">Die JSON-formatierte Zeichenfolge von Parametern für verwaltete Anwendung.</span><span class="sxs-lookup"><span data-stu-id="bdc57-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="bdc57-132">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameter enthält, oder die Parameter als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="bdc57-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="bdc57-133">-Plan</span><span class="sxs-lookup"><span data-stu-id="bdc57-133">-Plan</span></span>
<span data-ttu-id="bdc57-134">Eine Hashtabelle, die verwaltete Anwendungsplan Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="bdc57-134">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="bdc57-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="bdc57-135">-Pre</span></span>
<span data-ttu-id="bdc57-136">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="bdc57-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="bdc57-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc57-137">-ResourceGroupName</span></span>
<span data-ttu-id="bdc57-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bdc57-138">The resource group name.</span></span>

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

### <span data-ttu-id="bdc57-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="bdc57-139">-Tag</span></span>
<span data-ttu-id="bdc57-140">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="bdc57-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="bdc57-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bdc57-141">-Confirm</span></span>
<span data-ttu-id="bdc57-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bdc57-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdc57-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdc57-143">-WhatIf</span></span>
<span data-ttu-id="bdc57-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bdc57-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdc57-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdc57-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdc57-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc57-146">CommonParameters</span></span>
<span data-ttu-id="bdc57-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdc57-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc57-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdc57-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc57-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bdc57-149">INPUTS</span></span>

### <span data-ttu-id="bdc57-150">System. String</span><span class="sxs-lookup"><span data-stu-id="bdc57-150">System.String</span></span>

### <span data-ttu-id="bdc57-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bdc57-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bdc57-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bdc57-152">OUTPUTS</span></span>

### <span data-ttu-id="bdc57-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="bdc57-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="bdc57-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="bdc57-154">NOTES</span></span>

## <span data-ttu-id="bdc57-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bdc57-155">RELATED LINKS</span></span>
