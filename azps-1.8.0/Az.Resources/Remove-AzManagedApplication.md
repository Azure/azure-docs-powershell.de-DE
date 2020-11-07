---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 77cefc15467cc5fc553761457889aaf2ca770704
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659556"
---
# <span data-ttu-id="5f284-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="5f284-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="5f284-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f284-102">SYNOPSIS</span></span>
<span data-ttu-id="5f284-103">Entfernt eine verwaltete Anwendung</span><span class="sxs-lookup"><span data-stu-id="5f284-103">Removes a managed application</span></span>

## <span data-ttu-id="5f284-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f284-104">SYNTAX</span></span>

### <span data-ttu-id="5f284-105">RemoveByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f284-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f284-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="5f284-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f284-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f284-107">DESCRIPTION</span></span>
<span data-ttu-id="5f284-108">Das Cmdlet " **Remove-AzManagedApplication** " entfernt eine verwaltete Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5f284-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="5f284-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f284-109">EXAMPLES</span></span>

### <span data-ttu-id="5f284-110">Beispiel 1: Entfernen der verwalteten Anwendung nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="5f284-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="5f284-111">Der erste Befehl ruft eine verwaltete Anwendung mit dem Namen MyApp mithilfe des Get-AzManagedApplication-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="5f284-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="5f284-112">Der Befehl speichert Sie in der $Application-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5f284-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="5f284-113">Mit dem zweiten Befehl wird die verwaltete Anwendung entfernt, die durch die **Resourcen** -Eigenschaft $Application identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="5f284-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="5f284-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f284-114">PARAMETERS</span></span>

### <span data-ttu-id="5f284-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5f284-115">-ApiVersion</span></span>
<span data-ttu-id="5f284-116">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f284-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="5f284-117">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="5f284-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="5f284-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f284-118">-DefaultProfile</span></span>
<span data-ttu-id="5f284-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f284-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f284-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5f284-120">-Force</span></span>
<span data-ttu-id="5f284-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="5f284-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5f284-122">-ID</span><span class="sxs-lookup"><span data-stu-id="5f284-122">-Id</span></span>
<span data-ttu-id="5f284-123">Die vollqualifizierte verwaltete Anwendungs-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="5f284-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="5f284-124">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="5f284-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="5f284-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5f284-125">-Name</span></span>
<span data-ttu-id="5f284-126">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5f284-126">The managed application name.</span></span>

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

### <span data-ttu-id="5f284-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="5f284-127">-Pre</span></span>
<span data-ttu-id="5f284-128">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="5f284-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5f284-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f284-129">-ResourceGroupName</span></span>
<span data-ttu-id="5f284-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5f284-130">The resource group name.</span></span>

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

### <span data-ttu-id="5f284-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5f284-131">-Confirm</span></span>
<span data-ttu-id="5f284-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f284-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f284-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f284-133">-WhatIf</span></span>
<span data-ttu-id="5f284-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f284-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f284-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f284-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f284-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f284-136">CommonParameters</span></span>
<span data-ttu-id="5f284-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f284-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f284-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f284-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f284-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f284-139">INPUTS</span></span>

### <span data-ttu-id="5f284-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5f284-140">System.String</span></span>

## <span data-ttu-id="5f284-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f284-141">OUTPUTS</span></span>

### <span data-ttu-id="5f284-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5f284-142">System.Boolean</span></span>

## <span data-ttu-id="5f284-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f284-143">NOTES</span></span>

## <span data-ttu-id="5f284-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f284-144">RELATED LINKS</span></span>
