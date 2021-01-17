---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 88d89e819d97a42a797be81e5cb0b4b401401108
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308155"
---
# <span data-ttu-id="f1987-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="f1987-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="f1987-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1987-102">SYNOPSIS</span></span>
<span data-ttu-id="f1987-103">Entfernt eine Definition einer verwalteten Anwendung</span><span class="sxs-lookup"><span data-stu-id="f1987-103">Removes a managed application definition</span></span>

## <span data-ttu-id="f1987-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1987-104">SYNTAX</span></span>

### <span data-ttu-id="f1987-105">RemoveByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1987-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1987-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="f1987-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1987-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1987-107">DESCRIPTION</span></span>
<span data-ttu-id="f1987-108">Das **Cmdlet "Remove-AzManagedApplicationDefinition"** entfernt eine verwaltete Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="f1987-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="f1987-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1987-109">EXAMPLES</span></span>

### <span data-ttu-id="f1987-110">Beispiel 1: Entfernen der Definition einer verwalteten Anwendung nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f1987-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="f1987-111">Der erste Befehl ruft mithilfe des cmdlets "Get-AzManagedApplicationDefinition eine verwaltete Anwendungsdefinition namens "myAppDef" ab.</span><span class="sxs-lookup"><span data-stu-id="f1987-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="f1987-112">Der Befehl speichert sie in der $ApplicationDefinition Variable.</span><span class="sxs-lookup"><span data-stu-id="f1987-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="f1987-113">Mit dem zweiten Befehl wird die definition der verwalteten Anwendung entfernt, die durch die **Eigenschaft "ResourceId"** der $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="f1987-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="f1987-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1987-114">PARAMETERS</span></span>

### <span data-ttu-id="f1987-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f1987-115">-ApiVersion</span></span>
<span data-ttu-id="f1987-116">Wenn dies festgelegt ist, wird die Version der zu verwendenden Ressourcenanbieter-API angegeben.</span><span class="sxs-lookup"><span data-stu-id="f1987-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f1987-117">Wenn keine Angabe erfolgt, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f1987-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f1987-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1987-118">-DefaultProfile</span></span>
<span data-ttu-id="f1987-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1987-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1987-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f1987-120">-Force</span></span>
<span data-ttu-id="f1987-121">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="f1987-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f1987-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f1987-122">-Id</span></span>
<span data-ttu-id="f1987-123">Die vollqualifizierte Definitions-ID der verwalteten Anwendung, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="f1987-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="f1987-124">z. B. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="f1987-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="f1987-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f1987-125">-Name</span></span>
<span data-ttu-id="f1987-126">Der Name der verwalteten Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="f1987-126">The managed application definition name.</span></span>

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

### <span data-ttu-id="f1987-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="f1987-127">-Pre</span></span>
<span data-ttu-id="f1987-128">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1987-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f1987-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1987-129">-ResourceGroupName</span></span>
<span data-ttu-id="f1987-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f1987-130">The resource group name.</span></span>

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

### <span data-ttu-id="f1987-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1987-131">-Confirm</span></span>
<span data-ttu-id="f1987-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1987-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1987-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f1987-133">-WhatIf</span></span>
<span data-ttu-id="f1987-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1987-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1987-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1987-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1987-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1987-136">CommonParameters</span></span>
<span data-ttu-id="f1987-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1987-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1987-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1987-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1987-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1987-139">INPUTS</span></span>

### <span data-ttu-id="f1987-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f1987-140">System.String</span></span>

## <span data-ttu-id="f1987-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1987-141">OUTPUTS</span></span>

### <span data-ttu-id="f1987-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f1987-142">System.Boolean</span></span>

## <span data-ttu-id="f1987-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f1987-143">NOTES</span></span>

## <span data-ttu-id="f1987-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f1987-144">RELATED LINKS</span></span>
