---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 41f59b46595d45932010b1fcbedae07cdeca5f78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928504"
---
# <span data-ttu-id="b4b00-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="b4b00-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="b4b00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4b00-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b00-103">Entfernt eine verwaltete Anwendung</span><span class="sxs-lookup"><span data-stu-id="b4b00-103">Removes a managed application</span></span>

## <span data-ttu-id="b4b00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4b00-104">SYNTAX</span></span>

### <span data-ttu-id="b4b00-105">RemoveByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4b00-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4b00-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="b4b00-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4b00-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4b00-107">DESCRIPTION</span></span>
<span data-ttu-id="b4b00-108">Das **Cmdlet Remove-AzManagedApplication** entfernt eine verwaltete Anwendung</span><span class="sxs-lookup"><span data-stu-id="b4b00-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="b4b00-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b4b00-109">EXAMPLES</span></span>

### <span data-ttu-id="b4b00-110">Beispiel 1: Entfernen verwalteter Anwendungen nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b4b00-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="b4b00-111">Der erste Befehl ruft eine verwaltete Anwendung namens "myApp" mithilfe des cmdlets Get-AzManagedApplication ab.</span><span class="sxs-lookup"><span data-stu-id="b4b00-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="b4b00-112">Der Befehl speichert ihn in der $Application-Variable.</span><span class="sxs-lookup"><span data-stu-id="b4b00-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="b4b00-113">Mit dem zweiten Befehl wird die verwaltete Anwendung entfernt, die durch die **ResourceId-Eigenschaft** von $Application.</span><span class="sxs-lookup"><span data-stu-id="b4b00-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="b4b00-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b4b00-114">PARAMETERS</span></span>

### <span data-ttu-id="b4b00-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b4b00-115">-ApiVersion</span></span>
<span data-ttu-id="b4b00-116">Wenn festgelegt, gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="b4b00-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b4b00-117">Wenn nicht angegeben, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b4b00-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b4b00-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b00-118">-DefaultProfile</span></span>
<span data-ttu-id="b4b00-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4b00-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4b00-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="b4b00-120">-Force</span></span>
<span data-ttu-id="b4b00-121">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="b4b00-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b4b00-122">-ID</span><span class="sxs-lookup"><span data-stu-id="b4b00-122">-Id</span></span>
<span data-ttu-id="b4b00-123">Die vollqualifizierte verwaltete Anwendungs-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="b4b00-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="b4b00-124">z. B. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b4b00-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="b4b00-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b4b00-125">-Name</span></span>
<span data-ttu-id="b4b00-126">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b4b00-126">The managed application name.</span></span>

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

### <span data-ttu-id="b4b00-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="b4b00-127">-Pre</span></span>
<span data-ttu-id="b4b00-128">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4b00-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b4b00-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4b00-129">-ResourceGroupName</span></span>
<span data-ttu-id="b4b00-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b4b00-130">The resource group name.</span></span>

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

### <span data-ttu-id="b4b00-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4b00-131">-Confirm</span></span>
<span data-ttu-id="b4b00-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4b00-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4b00-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4b00-133">-WhatIf</span></span>
<span data-ttu-id="b4b00-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4b00-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4b00-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4b00-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4b00-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b00-136">CommonParameters</span></span>
<span data-ttu-id="b4b00-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4b00-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b00-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4b00-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b00-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b4b00-139">INPUTS</span></span>

### <span data-ttu-id="b4b00-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b4b00-140">System.String</span></span>

## <span data-ttu-id="b4b00-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b4b00-141">OUTPUTS</span></span>

### <span data-ttu-id="b4b00-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4b00-142">System.Boolean</span></span>

## <span data-ttu-id="b4b00-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b4b00-143">NOTES</span></span>

## <span data-ttu-id="b4b00-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b4b00-144">RELATED LINKS</span></span>
