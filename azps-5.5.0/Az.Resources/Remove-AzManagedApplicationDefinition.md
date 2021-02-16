---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 88d89e819d97a42a797be81e5cb0b4b401401108
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153585"
---
# <span data-ttu-id="48644-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="48644-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="48644-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48644-102">SYNOPSIS</span></span>
<span data-ttu-id="48644-103">Entfernt eine Definition einer verwalteten Anwendung</span><span class="sxs-lookup"><span data-stu-id="48644-103">Removes a managed application definition</span></span>

## <span data-ttu-id="48644-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48644-104">SYNTAX</span></span>

### <span data-ttu-id="48644-105">RemoveByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="48644-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48644-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="48644-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48644-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48644-107">DESCRIPTION</span></span>
<span data-ttu-id="48644-108">Das **Cmdlet "Remove-AzManagedApplicationDefinition"** entfernt eine verwaltete Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="48644-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="48644-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="48644-109">EXAMPLES</span></span>

### <span data-ttu-id="48644-110">Beispiel 1: Entfernen der Definition einer verwalteten Anwendung nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="48644-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="48644-111">Der erste Befehl ruft mithilfe des cmdlets "Get-AzManagedApplicationDefinition eine verwaltete Anwendungsdefinition namens "myAppDef" ab.</span><span class="sxs-lookup"><span data-stu-id="48644-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="48644-112">Der Befehl speichert sie in der $ApplicationDefinition Variable.</span><span class="sxs-lookup"><span data-stu-id="48644-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="48644-113">Mit dem zweiten Befehl wird die definition der verwalteten Anwendung entfernt, die durch die **Eigenschaft "ResourceId"** der $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="48644-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="48644-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48644-114">PARAMETERS</span></span>

### <span data-ttu-id="48644-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="48644-115">-ApiVersion</span></span>
<span data-ttu-id="48644-116">Gibt im festgelegten Satz die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="48644-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="48644-117">Wenn keine Angabe erfolgt, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="48644-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="48644-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48644-118">-DefaultProfile</span></span>
<span data-ttu-id="48644-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48644-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48644-120">-Force</span><span class="sxs-lookup"><span data-stu-id="48644-120">-Force</span></span>
<span data-ttu-id="48644-121">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="48644-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="48644-122">-ID</span><span class="sxs-lookup"><span data-stu-id="48644-122">-Id</span></span>
<span data-ttu-id="48644-123">Die vollqualifizierte Definitions-ID der verwalteten Anwendung, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="48644-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="48644-124">z. B. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="48644-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48644-125">-Name</span><span class="sxs-lookup"><span data-stu-id="48644-125">-Name</span></span>
<span data-ttu-id="48644-126">Der Name der verwalteten Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="48644-126">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48644-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="48644-127">-Pre</span></span>
<span data-ttu-id="48644-128">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="48644-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="48644-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48644-129">-ResourceGroupName</span></span>
<span data-ttu-id="48644-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="48644-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48644-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48644-131">-Confirm</span></span>
<span data-ttu-id="48644-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="48644-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48644-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="48644-133">-WhatIf</span></span>
<span data-ttu-id="48644-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="48644-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48644-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="48644-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48644-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48644-136">CommonParameters</span></span>
<span data-ttu-id="48644-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48644-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48644-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48644-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48644-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="48644-139">INPUTS</span></span>

### <span data-ttu-id="48644-140">System.String</span><span class="sxs-lookup"><span data-stu-id="48644-140">System.String</span></span>

## <span data-ttu-id="48644-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="48644-141">OUTPUTS</span></span>

### <span data-ttu-id="48644-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="48644-142">System.Boolean</span></span>

## <span data-ttu-id="48644-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="48644-143">NOTES</span></span>

## <span data-ttu-id="48644-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="48644-144">RELATED LINKS</span></span>
