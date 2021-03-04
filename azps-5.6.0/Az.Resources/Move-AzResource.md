---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: 16e43df2da9509d7fb222f3299a4c611d146026c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923944"
---
# <span data-ttu-id="8783e-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="8783e-101">Move-AzResource</span></span>

## <span data-ttu-id="8783e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8783e-102">SYNOPSIS</span></span>
<span data-ttu-id="8783e-103">Verschiebt eine Ressource in eine andere Ressourcengruppe oder ein anderes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8783e-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="8783e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8783e-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8783e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8783e-105">DESCRIPTION</span></span>
<span data-ttu-id="8783e-106">Das **Cmdlet Move-AzResource** verschiebt vorhandene Ressourcen in eine andere Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8783e-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="8783e-107">Diese Ressourcengruppe kann in einem anderen Abonnement enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="8783e-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="8783e-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8783e-108">EXAMPLES</span></span>

### <span data-ttu-id="8783e-109">Beispiel 1: Verschieben einer Ressource in eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8783e-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="8783e-110">Der erste Befehl ruft eine Ressource mit dem Namen ContosoStorageAccount mithilfe des cmdlets Get-AzResource ab und speichert diese Ressource dann in der $Resource Variablen.</span><span class="sxs-lookup"><span data-stu-id="8783e-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="8783e-111">Der zweite Befehl verschiebt diese Ressource in die Ressourcengruppe "ResourceGroup14".</span><span class="sxs-lookup"><span data-stu-id="8783e-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="8783e-112">Der Befehl identifiziert die zu verschiebende Ressource mithilfe der **ResourceId-Eigenschaft** $Resource.</span><span class="sxs-lookup"><span data-stu-id="8783e-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="8783e-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8783e-113">PARAMETERS</span></span>

### <span data-ttu-id="8783e-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8783e-114">-ApiVersion</span></span>
<span data-ttu-id="8783e-115">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="8783e-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8783e-116">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="8783e-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8783e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8783e-117">-DefaultProfile</span></span>
<span data-ttu-id="8783e-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8783e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8783e-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8783e-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="8783e-120">Gibt den Namen der Ressourcengruppe an, in die dieses Cmdlet Ressourcen verschiebt.</span><span class="sxs-lookup"><span data-stu-id="8783e-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8783e-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8783e-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="8783e-122">Gibt die ID des Abonnements an, in das dieses Cmdlet Ressourcen verschiebt.</span><span class="sxs-lookup"><span data-stu-id="8783e-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8783e-123">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="8783e-123">-Force</span></span>
<span data-ttu-id="8783e-124">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="8783e-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8783e-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="8783e-125">-Pre</span></span>
<span data-ttu-id="8783e-126">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8783e-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8783e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8783e-127">-ResourceId</span></span>
<span data-ttu-id="8783e-128">Gibt ein Array von IDs der Ressourcen an, die dieses Cmdlet verschiebt.</span><span class="sxs-lookup"><span data-stu-id="8783e-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8783e-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8783e-129">-Confirm</span></span>
<span data-ttu-id="8783e-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8783e-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8783e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8783e-131">-WhatIf</span></span>
<span data-ttu-id="8783e-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8783e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8783e-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8783e-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8783e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8783e-134">CommonParameters</span></span>
<span data-ttu-id="8783e-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8783e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8783e-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8783e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8783e-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8783e-137">INPUTS</span></span>

### <span data-ttu-id="8783e-138">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8783e-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8783e-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8783e-139">System.String[]</span></span>

## <span data-ttu-id="8783e-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8783e-140">OUTPUTS</span></span>

### <span data-ttu-id="8783e-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8783e-141">System.Boolean</span></span>

## <span data-ttu-id="8783e-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8783e-142">NOTES</span></span>

## <span data-ttu-id="8783e-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8783e-143">RELATED LINKS</span></span>

[<span data-ttu-id="8783e-144">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8783e-144">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="8783e-145">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="8783e-145">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="8783e-146">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="8783e-146">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="8783e-147">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="8783e-147">Set-AzResource</span></span>](./Set-AzResource.md)


