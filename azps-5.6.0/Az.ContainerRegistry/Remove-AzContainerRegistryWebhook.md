---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: e189be8f04081bbc51c5cc19b981c164ce4e9c2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920811"
---
# <span data-ttu-id="e3e59-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e3e59-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="e3e59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3e59-102">SYNOPSIS</span></span>
<span data-ttu-id="e3e59-103">Entfernt einen Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="e3e59-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="e3e59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3e59-104">SYNTAX</span></span>

### <span data-ttu-id="e3e59-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e3e59-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3e59-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3e59-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3e59-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3e59-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3e59-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3e59-108">DESCRIPTION</span></span>
<span data-ttu-id="e3e59-109">Das Remove-AzContainerRegistryWebhook cmdlet entfernt einen Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="e3e59-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="e3e59-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e3e59-110">EXAMPLES</span></span>

### <span data-ttu-id="e3e59-111">Beispiel 1: Entfernen eines Containerregistrierungswebhooks.</span><span class="sxs-lookup"><span data-stu-id="e3e59-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="e3e59-112">Entfernt einen Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="e3e59-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="e3e59-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e3e59-113">PARAMETERS</span></span>

### <span data-ttu-id="e3e59-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3e59-114">-DefaultProfile</span></span>
<span data-ttu-id="e3e59-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3e59-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3e59-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e3e59-116">-Name</span></span>
<span data-ttu-id="e3e59-117">Webhookname.</span><span class="sxs-lookup"><span data-stu-id="e3e59-117">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e59-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3e59-118">-PassThru</span></span>
<span data-ttu-id="e3e59-119">Gibt an, dass dieses Cmdlet "true" zurückgibt, wenn das Entfernen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="e3e59-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="e3e59-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="e3e59-120">-RegistryName</span></span>
<span data-ttu-id="e3e59-121">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="e3e59-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e59-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3e59-122">-ResourceGroupName</span></span>
<span data-ttu-id="e3e59-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="e3e59-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e59-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3e59-124">-ResourceId</span></span>
<span data-ttu-id="e3e59-125">Die Containerregistrierungs-Webhook-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e3e59-125">The container registry Webhook resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e59-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="e3e59-126">-Webhook</span></span>
<span data-ttu-id="e3e59-127">Containerregistrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="e3e59-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e59-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e3e59-128">-Confirm</span></span>
<span data-ttu-id="e3e59-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3e59-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3e59-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3e59-130">-WhatIf</span></span>
<span data-ttu-id="e3e59-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3e59-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3e59-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3e59-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3e59-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3e59-133">CommonParameters</span></span>
<span data-ttu-id="e3e59-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3e59-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3e59-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3e59-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3e59-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e3e59-136">INPUTS</span></span>

### <span data-ttu-id="e3e59-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e3e59-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="e3e59-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e3e59-138">System.String</span></span>

## <span data-ttu-id="e3e59-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e3e59-139">OUTPUTS</span></span>

### <span data-ttu-id="e3e59-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3e59-140">System.Boolean</span></span>

## <span data-ttu-id="e3e59-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e3e59-141">NOTES</span></span>

## <span data-ttu-id="e3e59-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e3e59-142">RELATED LINKS</span></span>

[<span data-ttu-id="e3e59-143">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e3e59-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="e3e59-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e3e59-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="e3e59-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e3e59-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="e3e59-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e3e59-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)