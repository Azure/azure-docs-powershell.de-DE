---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 17a28da26aa26860b7fd4a28ec922932bb089da3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459223"
---
# <span data-ttu-id="dbd0b-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="dbd0b-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="dbd0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbd0b-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd0b-103">Entfernt eine verwaltete Anwendung</span><span class="sxs-lookup"><span data-stu-id="dbd0b-103">Removes a managed application</span></span>

## <span data-ttu-id="dbd0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbd0b-104">SYNTAX</span></span>

### <span data-ttu-id="dbd0b-105">RemoveByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="dbd0b-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbd0b-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="dbd0b-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbd0b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbd0b-107">DESCRIPTION</span></span>
<span data-ttu-id="dbd0b-108">Das **Cmdlet "Remove-AzManagedApplication"** entfernt eine verwaltete Anwendung.</span><span class="sxs-lookup"><span data-stu-id="dbd0b-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="dbd0b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dbd0b-109">EXAMPLES</span></span>

### <span data-ttu-id="dbd0b-110">Beispiel 1: Entfernen einer verwalteten Anwendung nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="dbd0b-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="dbd0b-111">Der erste Befehl ruft mithilfe des Cmdlets "Get-AzManagedApplication" eine verwaltete Anwendung namens "myApp" ab.</span><span class="sxs-lookup"><span data-stu-id="dbd0b-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="dbd0b-112">Der Befehl speichert sie in der $Application Variable.</span><span class="sxs-lookup"><span data-stu-id="dbd0b-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="dbd0b-113">Mit dem zweiten Befehl wird die verwaltete Anwendung entfernt, die durch die **Eigenschaft "ResourceId"** von "$Application.</span><span class="sxs-lookup"><span data-stu-id="dbd0b-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="dbd0b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbd0b-114">PARAMETERS</span></span>

### <span data-ttu-id="dbd0b-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dbd0b-115">-ApiVersion</span></span>
<span data-ttu-id="dbd0b-116">Wenn dies festgelegt ist, wird die Version der zu verwendenden Ressourcenanbieter-API angegeben.</span><span class="sxs-lookup"><span data-stu-id="dbd0b-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="dbd0b-117">Wenn keine Angabe erfolgt, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="dbd0b-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="dbd0b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd0b-118">-DefaultProfile</span></span>
<span data-ttu-id="dbd0b-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbd0b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbd0b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="dbd0b-120">-Force</span></span>
<span data-ttu-id="dbd0b-121">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="dbd0b-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dbd0b-122">-ID</span><span class="sxs-lookup"><span data-stu-id="dbd0b-122">-Id</span></span>
<span data-ttu-id="dbd0b-123">Die vollqualifizierte verwaltete Anwendungs-ID einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="dbd0b-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="dbd0b-124">z. B. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="dbd0b-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="dbd0b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dbd0b-125">-Name</span></span>
<span data-ttu-id="dbd0b-126">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="dbd0b-126">The managed application name.</span></span>

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

### <span data-ttu-id="dbd0b-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="dbd0b-127">-Pre</span></span>
<span data-ttu-id="dbd0b-128">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dbd0b-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="dbd0b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbd0b-129">-ResourceGroupName</span></span>
<span data-ttu-id="dbd0b-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dbd0b-130">The resource group name.</span></span>

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

### <span data-ttu-id="dbd0b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbd0b-131">-Confirm</span></span>
<span data-ttu-id="dbd0b-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dbd0b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbd0b-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dbd0b-133">-WhatIf</span></span>
<span data-ttu-id="dbd0b-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbd0b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbd0b-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbd0b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbd0b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd0b-136">CommonParameters</span></span>
<span data-ttu-id="dbd0b-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbd0b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd0b-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbd0b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd0b-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dbd0b-139">INPUTS</span></span>

### <span data-ttu-id="dbd0b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="dbd0b-140">System.String</span></span>

## <span data-ttu-id="dbd0b-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dbd0b-141">OUTPUTS</span></span>

### <span data-ttu-id="dbd0b-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dbd0b-142">System.Boolean</span></span>

## <span data-ttu-id="dbd0b-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dbd0b-143">NOTES</span></span>

## <span data-ttu-id="dbd0b-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dbd0b-144">RELATED LINKS</span></span>
