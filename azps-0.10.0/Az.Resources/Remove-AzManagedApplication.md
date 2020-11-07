---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: a1dbab8cdb3416809a7200d91f718475334b2d9c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843267"
---
# <span data-ttu-id="90e74-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="90e74-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="90e74-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90e74-102">SYNOPSIS</span></span>
<span data-ttu-id="90e74-103">Entfernt eine verwaltete Anwendung</span><span class="sxs-lookup"><span data-stu-id="90e74-103">Removes a managed application</span></span>

## <span data-ttu-id="90e74-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90e74-104">SYNTAX</span></span>

### <span data-ttu-id="90e74-105">RemoveByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="90e74-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90e74-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="90e74-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90e74-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90e74-107">DESCRIPTION</span></span>
<span data-ttu-id="90e74-108">Das Cmdlet " **Remove-AzManagedApplication** " entfernt eine verwaltete Anwendung.</span><span class="sxs-lookup"><span data-stu-id="90e74-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="90e74-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90e74-109">EXAMPLES</span></span>

### <span data-ttu-id="90e74-110">Beispiel 1: Entfernen der verwalteten Anwendung nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="90e74-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="90e74-111">Der erste Befehl ruft eine verwaltete Anwendung mit dem Namen MyApp mithilfe des Get-AzManagedApplication-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="90e74-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="90e74-112">Der Befehl speichert Sie in der $Application-Variablen.</span><span class="sxs-lookup"><span data-stu-id="90e74-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="90e74-113">Mit dem zweiten Befehl wird die verwaltete Anwendung entfernt, die durch die **Resourcen** -Eigenschaft $Application identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="90e74-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="90e74-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="90e74-114">PARAMETERS</span></span>

### <span data-ttu-id="90e74-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="90e74-115">-ApiVersion</span></span>
<span data-ttu-id="90e74-116">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="90e74-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="90e74-117">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="90e74-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="90e74-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e74-118">-DefaultProfile</span></span>
<span data-ttu-id="90e74-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90e74-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e74-120">-Force</span><span class="sxs-lookup"><span data-stu-id="90e74-120">-Force</span></span>
<span data-ttu-id="90e74-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="90e74-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="90e74-122">-ID</span><span class="sxs-lookup"><span data-stu-id="90e74-122">-Id</span></span>
<span data-ttu-id="90e74-123">Die vollqualifizierte verwaltete Anwendungs-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="90e74-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="90e74-124">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="90e74-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="90e74-125">-Name</span><span class="sxs-lookup"><span data-stu-id="90e74-125">-Name</span></span>
<span data-ttu-id="90e74-126">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="90e74-126">The managed application name.</span></span>

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

### <span data-ttu-id="90e74-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="90e74-127">-Pre</span></span>
<span data-ttu-id="90e74-128">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="90e74-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="90e74-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e74-129">-ResourceGroupName</span></span>
<span data-ttu-id="90e74-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="90e74-130">The resource group name.</span></span>

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

### <span data-ttu-id="90e74-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90e74-131">-Confirm</span></span>
<span data-ttu-id="90e74-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90e74-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e74-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e74-133">-WhatIf</span></span>
<span data-ttu-id="90e74-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90e74-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90e74-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90e74-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e74-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e74-136">CommonParameters</span></span>
<span data-ttu-id="90e74-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90e74-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e74-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90e74-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e74-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90e74-139">INPUTS</span></span>

### <span data-ttu-id="90e74-140">System. String</span><span class="sxs-lookup"><span data-stu-id="90e74-140">System.String</span></span>

## <span data-ttu-id="90e74-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90e74-141">OUTPUTS</span></span>

### <span data-ttu-id="90e74-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90e74-142">System.Boolean</span></span>

## <span data-ttu-id="90e74-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="90e74-143">NOTES</span></span>

## <span data-ttu-id="90e74-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90e74-144">RELATED LINKS</span></span>
