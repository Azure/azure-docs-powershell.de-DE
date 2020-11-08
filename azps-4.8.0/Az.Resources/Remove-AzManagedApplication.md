---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 17a28da26aa26860b7fd4a28ec922932bb089da3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166645"
---
# <span data-ttu-id="881ce-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="881ce-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="881ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="881ce-102">SYNOPSIS</span></span>
<span data-ttu-id="881ce-103">Entfernt eine verwaltete Anwendung</span><span class="sxs-lookup"><span data-stu-id="881ce-103">Removes a managed application</span></span>

## <span data-ttu-id="881ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="881ce-104">SYNTAX</span></span>

### <span data-ttu-id="881ce-105">RemoveByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="881ce-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="881ce-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="881ce-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="881ce-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="881ce-107">DESCRIPTION</span></span>
<span data-ttu-id="881ce-108">Das Cmdlet " **Remove-AzManagedApplication** " entfernt eine verwaltete Anwendung.</span><span class="sxs-lookup"><span data-stu-id="881ce-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="881ce-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="881ce-109">EXAMPLES</span></span>

### <span data-ttu-id="881ce-110">Beispiel 1: Entfernen der verwalteten Anwendung nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="881ce-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="881ce-111">Der erste Befehl ruft eine verwaltete Anwendung mit dem Namen MyApp mithilfe des Get-AzManagedApplication-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="881ce-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="881ce-112">Der Befehl speichert Sie in der $Application-Variablen.</span><span class="sxs-lookup"><span data-stu-id="881ce-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="881ce-113">Mit dem zweiten Befehl wird die verwaltete Anwendung entfernt, die durch die **Resourcen** -Eigenschaft $Application identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="881ce-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="881ce-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="881ce-114">PARAMETERS</span></span>

### <span data-ttu-id="881ce-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="881ce-115">-ApiVersion</span></span>
<span data-ttu-id="881ce-116">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="881ce-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="881ce-117">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="881ce-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="881ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="881ce-118">-DefaultProfile</span></span>
<span data-ttu-id="881ce-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="881ce-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="881ce-120">-Force</span><span class="sxs-lookup"><span data-stu-id="881ce-120">-Force</span></span>
<span data-ttu-id="881ce-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="881ce-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="881ce-122">-ID</span><span class="sxs-lookup"><span data-stu-id="881ce-122">-Id</span></span>
<span data-ttu-id="881ce-123">Die vollqualifizierte verwaltete Anwendungs-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="881ce-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="881ce-124">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="881ce-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="881ce-125">-Name</span><span class="sxs-lookup"><span data-stu-id="881ce-125">-Name</span></span>
<span data-ttu-id="881ce-126">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="881ce-126">The managed application name.</span></span>

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

### <span data-ttu-id="881ce-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="881ce-127">-Pre</span></span>
<span data-ttu-id="881ce-128">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="881ce-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="881ce-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="881ce-129">-ResourceGroupName</span></span>
<span data-ttu-id="881ce-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="881ce-130">The resource group name.</span></span>

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

### <span data-ttu-id="881ce-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="881ce-131">-Confirm</span></span>
<span data-ttu-id="881ce-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="881ce-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="881ce-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="881ce-133">-WhatIf</span></span>
<span data-ttu-id="881ce-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="881ce-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="881ce-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="881ce-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="881ce-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="881ce-136">CommonParameters</span></span>
<span data-ttu-id="881ce-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="881ce-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="881ce-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="881ce-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="881ce-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="881ce-139">INPUTS</span></span>

### <span data-ttu-id="881ce-140">System. String</span><span class="sxs-lookup"><span data-stu-id="881ce-140">System.String</span></span>

## <span data-ttu-id="881ce-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="881ce-141">OUTPUTS</span></span>

### <span data-ttu-id="881ce-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="881ce-142">System.Boolean</span></span>

## <span data-ttu-id="881ce-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="881ce-143">NOTES</span></span>

## <span data-ttu-id="881ce-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="881ce-144">RELATED LINKS</span></span>
