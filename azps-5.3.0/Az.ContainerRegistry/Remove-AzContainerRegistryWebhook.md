---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4064728aeffb53fe9f6065d295455738b6a0f046
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472874"
---
# <span data-ttu-id="b59ce-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b59ce-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="b59ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b59ce-102">SYNOPSIS</span></span>
<span data-ttu-id="b59ce-103">Entfernt einen Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="b59ce-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="b59ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b59ce-104">SYNTAX</span></span>

### <span data-ttu-id="b59ce-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b59ce-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b59ce-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b59ce-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b59ce-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b59ce-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b59ce-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b59ce-108">DESCRIPTION</span></span>
<span data-ttu-id="b59ce-109">Das Remove-AzContainerRegistryWebhook cmdlet entfernt einen Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="b59ce-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="b59ce-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b59ce-110">EXAMPLES</span></span>

### <span data-ttu-id="b59ce-111">Beispiel 1: Entfernen eines Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="b59ce-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="b59ce-112">Entfernt einen Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="b59ce-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="b59ce-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b59ce-113">PARAMETERS</span></span>

### <span data-ttu-id="b59ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b59ce-114">-DefaultProfile</span></span>
<span data-ttu-id="b59ce-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b59ce-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b59ce-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b59ce-116">-Name</span></span>
<span data-ttu-id="b59ce-117">Name des Webhook.</span><span class="sxs-lookup"><span data-stu-id="b59ce-117">Webhook Name.</span></span>

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

### <span data-ttu-id="b59ce-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b59ce-118">-PassThru</span></span>
<span data-ttu-id="b59ce-119">Gibt an, dass dieses Cmdlet "true" zurückgibt, wenn das Entfernen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b59ce-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="b59ce-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b59ce-120">-RegistryName</span></span>
<span data-ttu-id="b59ce-121">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="b59ce-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="b59ce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b59ce-122">-ResourceGroupName</span></span>
<span data-ttu-id="b59ce-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="b59ce-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="b59ce-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b59ce-124">-ResourceId</span></span>
<span data-ttu-id="b59ce-125">Die Containerregistrierungs-Webhook-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b59ce-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="b59ce-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="b59ce-126">-Webhook</span></span>
<span data-ttu-id="b59ce-127">Containerregistrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="b59ce-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="b59ce-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b59ce-128">-Confirm</span></span>
<span data-ttu-id="b59ce-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b59ce-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b59ce-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b59ce-130">-WhatIf</span></span>
<span data-ttu-id="b59ce-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b59ce-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b59ce-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b59ce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b59ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b59ce-133">CommonParameters</span></span>
<span data-ttu-id="b59ce-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b59ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b59ce-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b59ce-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b59ce-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b59ce-136">INPUTS</span></span>

### <span data-ttu-id="b59ce-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b59ce-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="b59ce-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b59ce-138">System.String</span></span>

## <span data-ttu-id="b59ce-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b59ce-139">OUTPUTS</span></span>

### <span data-ttu-id="b59ce-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b59ce-140">System.Boolean</span></span>

## <span data-ttu-id="b59ce-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b59ce-141">NOTES</span></span>

## <span data-ttu-id="b59ce-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b59ce-142">RELATED LINKS</span></span>

[<span data-ttu-id="b59ce-143">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b59ce-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b59ce-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b59ce-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b59ce-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b59ce-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b59ce-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b59ce-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)