---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 30e3e7f7b6ace383a2c492f4dcc088f65dfea08b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943522"
---
# <span data-ttu-id="66912-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="66912-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="66912-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66912-102">SYNOPSIS</span></span>
<span data-ttu-id="66912-103">Erstellt eine von Azure verwaltete Anwendung.</span><span class="sxs-lookup"><span data-stu-id="66912-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="66912-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66912-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66912-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66912-105">DESCRIPTION</span></span>
<span data-ttu-id="66912-106">Das **Cmdlet New-AzManagedApplication** erstellt eine verwaltete Azure-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="66912-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="66912-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66912-107">EXAMPLES</span></span>

### <span data-ttu-id="66912-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66912-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="66912-109">Mit diesem Befehl wird eine verwaltete Anwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="66912-109">This command creates a managed application</span></span>

## <span data-ttu-id="66912-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="66912-110">PARAMETERS</span></span>

### <span data-ttu-id="66912-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="66912-111">-ApiVersion</span></span>
<span data-ttu-id="66912-112">Wenn festgelegt, gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="66912-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="66912-113">Wenn nicht angegeben, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="66912-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="66912-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66912-114">-DefaultProfile</span></span>
<span data-ttu-id="66912-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66912-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66912-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="66912-116">-Kind</span></span>
<span data-ttu-id="66912-117">Die art der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="66912-117">The managed application kind.</span></span>
<span data-ttu-id="66912-118">Eines der Marketplace- oder Servicecatalogs</span><span class="sxs-lookup"><span data-stu-id="66912-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66912-119">-Location</span><span class="sxs-lookup"><span data-stu-id="66912-119">-Location</span></span>
<span data-ttu-id="66912-120">Der Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="66912-120">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66912-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="66912-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="66912-122">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="66912-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="66912-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66912-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="66912-124">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="66912-124">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66912-125">-Name</span><span class="sxs-lookup"><span data-stu-id="66912-125">-Name</span></span>
<span data-ttu-id="66912-126">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="66912-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66912-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="66912-127">-Parameter</span></span>
<span data-ttu-id="66912-128">Die JSON formatierte Zeichenfolge mit Parametern für verwaltete Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="66912-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="66912-129">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameter enthält, oder die Parameter als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="66912-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="66912-130">-Plan</span><span class="sxs-lookup"><span data-stu-id="66912-130">-Plan</span></span>
<span data-ttu-id="66912-131">Eine Hashtabelle, die die Eigenschaften des Plans für verwaltete Anwendungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="66912-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="66912-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="66912-132">-Pre</span></span>
<span data-ttu-id="66912-133">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="66912-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="66912-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66912-134">-ResourceGroupName</span></span>
<span data-ttu-id="66912-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="66912-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66912-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="66912-136">-Tag</span></span>
<span data-ttu-id="66912-137">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="66912-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="66912-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66912-138">-Confirm</span></span>
<span data-ttu-id="66912-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66912-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66912-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66912-140">-WhatIf</span></span>
<span data-ttu-id="66912-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66912-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66912-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66912-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66912-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66912-143">CommonParameters</span></span>
<span data-ttu-id="66912-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66912-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66912-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66912-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66912-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66912-146">INPUTS</span></span>

### <span data-ttu-id="66912-147">System.String</span><span class="sxs-lookup"><span data-stu-id="66912-147">System.String</span></span>

### <span data-ttu-id="66912-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="66912-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="66912-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66912-149">OUTPUTS</span></span>

### <span data-ttu-id="66912-150">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="66912-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="66912-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="66912-151">NOTES</span></span>

## <span data-ttu-id="66912-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="66912-152">RELATED LINKS</span></span>
