---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 06ff54b8f5a247f3035d0eda0be5c474f9a9576b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153652"
---
# <span data-ttu-id="2cf2e-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="2cf2e-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="2cf2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cf2e-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf2e-103">Erstellt eine in Azure verwaltete Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="2cf2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2cf2e-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cf2e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2cf2e-105">DESCRIPTION</span></span>
<span data-ttu-id="2cf2e-106">Das **Cmdlet "New-AzManagedApplication"** erstellt eine verwaltete Azure-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="2cf2e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2cf2e-107">EXAMPLES</span></span>

### <span data-ttu-id="2cf2e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2cf2e-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="2cf2e-109">Mit diesem Befehl wird eine verwaltete Anwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-109">This command creates a managed application</span></span>

## <span data-ttu-id="2cf2e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cf2e-110">PARAMETERS</span></span>

### <span data-ttu-id="2cf2e-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2cf2e-111">-ApiVersion</span></span>
<span data-ttu-id="2cf2e-112">Gibt im festgelegten Satz die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2cf2e-113">Wenn keine Angabe erfolgt, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2cf2e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf2e-114">-DefaultProfile</span></span>
<span data-ttu-id="2cf2e-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cf2e-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="2cf2e-116">-Kind</span></span>
<span data-ttu-id="2cf2e-117">Die verwaltete Anwendungs art.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-117">The managed application kind.</span></span>
<span data-ttu-id="2cf2e-118">Eine von Marketplace oder Servicecatalog</span><span class="sxs-lookup"><span data-stu-id="2cf2e-118">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="2cf2e-119">-Location</span><span class="sxs-lookup"><span data-stu-id="2cf2e-119">-Location</span></span>
<span data-ttu-id="2cf2e-120">Der Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-120">The resource location.</span></span>

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

### <span data-ttu-id="2cf2e-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="2cf2e-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="2cf2e-122">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="2cf2e-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cf2e-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="2cf2e-124">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-124">The managed resource group name.</span></span>

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

### <span data-ttu-id="2cf2e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2cf2e-125">-Name</span></span>
<span data-ttu-id="2cf2e-126">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-126">The managed application name.</span></span>

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

### <span data-ttu-id="2cf2e-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="2cf2e-127">-Parameter</span></span>
<span data-ttu-id="2cf2e-128">Die in JSON formatierte Parameterzeichenfolge für verwaltete Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="2cf2e-129">Dabei kann es sich entweder um einen Pfad zu einem Dateinamen oder URI mit den Parametern oder um die Parameter als Zeichenfolge geben.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="2cf2e-130">-Planen</span><span class="sxs-lookup"><span data-stu-id="2cf2e-130">-Plan</span></span>
<span data-ttu-id="2cf2e-131">Eine Hashtabelle, die verwaltete Anwendungsplaneigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="2cf2e-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="2cf2e-132">-Pre</span></span>
<span data-ttu-id="2cf2e-133">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2cf2e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cf2e-134">-ResourceGroupName</span></span>
<span data-ttu-id="2cf2e-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-135">The resource group name.</span></span>

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

### <span data-ttu-id="2cf2e-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="2cf2e-136">-Tag</span></span>
<span data-ttu-id="2cf2e-137">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="2cf2e-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cf2e-138">-Confirm</span></span>
<span data-ttu-id="2cf2e-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cf2e-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2cf2e-140">-WhatIf</span></span>
<span data-ttu-id="2cf2e-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cf2e-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cf2e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf2e-143">CommonParameters</span></span>
<span data-ttu-id="2cf2e-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cf2e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf2e-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cf2e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf2e-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2cf2e-146">INPUTS</span></span>

### <span data-ttu-id="2cf2e-147">System.String</span><span class="sxs-lookup"><span data-stu-id="2cf2e-147">System.String</span></span>

### <span data-ttu-id="2cf2e-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2cf2e-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2cf2e-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2cf2e-149">OUTPUTS</span></span>

### <span data-ttu-id="2cf2e-150">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="2cf2e-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2cf2e-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2cf2e-151">NOTES</span></span>

## <span data-ttu-id="2cf2e-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2cf2e-152">RELATED LINKS</span></span>
