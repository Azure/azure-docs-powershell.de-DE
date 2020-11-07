---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4064728aeffb53fe9f6065d295455738b6a0f046
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845676"
---
# <span data-ttu-id="57a3b-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="57a3b-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="57a3b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57a3b-102">SYNOPSIS</span></span>
<span data-ttu-id="57a3b-103">Entfernt einen Container Registrierungs webhook.</span><span class="sxs-lookup"><span data-stu-id="57a3b-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="57a3b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57a3b-104">SYNTAX</span></span>

### <span data-ttu-id="57a3b-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="57a3b-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57a3b-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57a3b-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57a3b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57a3b-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57a3b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57a3b-108">DESCRIPTION</span></span>
<span data-ttu-id="57a3b-109">Das Remove-AzContainerRegistryWebhook-Cmdlet entfernt einen Container Registrierungs-webhook.</span><span class="sxs-lookup"><span data-stu-id="57a3b-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="57a3b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57a3b-110">EXAMPLES</span></span>

### <span data-ttu-id="57a3b-111">Beispiel 1: Entfernen eines Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="57a3b-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="57a3b-112">Entfernt einen Container Registrierungs webhook.</span><span class="sxs-lookup"><span data-stu-id="57a3b-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="57a3b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="57a3b-113">PARAMETERS</span></span>

### <span data-ttu-id="57a3b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57a3b-114">-DefaultProfile</span></span>
<span data-ttu-id="57a3b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="57a3b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57a3b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="57a3b-116">-Name</span></span>
<span data-ttu-id="57a3b-117">Webhook-Name.</span><span class="sxs-lookup"><span data-stu-id="57a3b-117">Webhook Name.</span></span>

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

### <span data-ttu-id="57a3b-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57a3b-118">-PassThru</span></span>
<span data-ttu-id="57a3b-119">Gibt an, dass dieses Cmdlet "true" zurückgibt, wenn die Entfernung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="57a3b-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="57a3b-120">-Registryname</span><span class="sxs-lookup"><span data-stu-id="57a3b-120">-RegistryName</span></span>
<span data-ttu-id="57a3b-121">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="57a3b-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="57a3b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57a3b-122">-ResourceGroupName</span></span>
<span data-ttu-id="57a3b-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="57a3b-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="57a3b-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="57a3b-124">-ResourceId</span></span>
<span data-ttu-id="57a3b-125">Die Ressourcen-ID des Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="57a3b-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="57a3b-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="57a3b-126">-Webhook</span></span>
<span data-ttu-id="57a3b-127">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="57a3b-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="57a3b-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="57a3b-128">-Confirm</span></span>
<span data-ttu-id="57a3b-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="57a3b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57a3b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57a3b-130">-WhatIf</span></span>
<span data-ttu-id="57a3b-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57a3b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57a3b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="57a3b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57a3b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a3b-133">CommonParameters</span></span>
<span data-ttu-id="57a3b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57a3b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a3b-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57a3b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a3b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57a3b-136">INPUTS</span></span>

### <span data-ttu-id="57a3b-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="57a3b-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="57a3b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="57a3b-138">System.String</span></span>

## <span data-ttu-id="57a3b-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57a3b-139">OUTPUTS</span></span>

### <span data-ttu-id="57a3b-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="57a3b-140">System.Boolean</span></span>

## <span data-ttu-id="57a3b-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="57a3b-141">NOTES</span></span>

## <span data-ttu-id="57a3b-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57a3b-142">RELATED LINKS</span></span>

[<span data-ttu-id="57a3b-143">Neu – AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="57a3b-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="57a3b-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="57a3b-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="57a3b-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="57a3b-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="57a3b-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="57a3b-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)