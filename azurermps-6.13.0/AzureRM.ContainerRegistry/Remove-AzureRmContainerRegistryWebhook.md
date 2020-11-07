---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: c1ba245f83db386e39f9fecf22f95d3681452d7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664361"
---
# <span data-ttu-id="b5050-101">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b5050-101">Remove-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="b5050-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b5050-102">SYNOPSIS</span></span>
<span data-ttu-id="b5050-103">Entfernt einen Container Registrierungs webhook.</span><span class="sxs-lookup"><span data-stu-id="b5050-103">Removes a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5050-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5050-104">SYNTAX</span></span>

### <span data-ttu-id="b5050-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b5050-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5050-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5050-106">WebhookObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5050-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5050-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5050-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5050-108">DESCRIPTION</span></span>
<span data-ttu-id="b5050-109">Das Remove-AzureRmContainerRegistryWebhook-Cmdlet entfernt einen Container Registrierungs-webhook.</span><span class="sxs-lookup"><span data-stu-id="b5050-109">The Remove-AzureRmContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="b5050-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b5050-110">EXAMPLES</span></span>

### <span data-ttu-id="b5050-111">Beispiel 1: Entfernen eines Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="b5050-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="b5050-112">Entfernt einen Container Registrierungs webhook.</span><span class="sxs-lookup"><span data-stu-id="b5050-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="b5050-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5050-113">PARAMETERS</span></span>

### <span data-ttu-id="b5050-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5050-114">-DefaultProfile</span></span>
<span data-ttu-id="b5050-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b5050-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5050-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b5050-116">-Name</span></span>
<span data-ttu-id="b5050-117">Webhook-Name.</span><span class="sxs-lookup"><span data-stu-id="b5050-117">Webhook Name.</span></span>

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

### <span data-ttu-id="b5050-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5050-118">-PassThru</span></span>
<span data-ttu-id="b5050-119">Gibt an, dass dieses Cmdlet "true" zurückgibt, wenn die Entfernung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b5050-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="b5050-120">-Registryname</span><span class="sxs-lookup"><span data-stu-id="b5050-120">-RegistryName</span></span>
<span data-ttu-id="b5050-121">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="b5050-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="b5050-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5050-122">-ResourceGroupName</span></span>
<span data-ttu-id="b5050-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b5050-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="b5050-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b5050-124">-ResourceId</span></span>
<span data-ttu-id="b5050-125">Die Ressourcen-ID des Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="b5050-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="b5050-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="b5050-126">-Webhook</span></span>
<span data-ttu-id="b5050-127">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="b5050-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="b5050-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b5050-128">-Confirm</span></span>
<span data-ttu-id="b5050-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5050-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5050-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5050-130">-WhatIf</span></span>
<span data-ttu-id="b5050-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5050-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5050-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5050-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5050-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5050-133">CommonParameters</span></span>
<span data-ttu-id="b5050-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5050-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5050-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5050-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5050-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b5050-136">INPUTS</span></span>

### <span data-ttu-id="b5050-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b5050-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="b5050-138">Parameter: webhook (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b5050-138">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="b5050-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b5050-139">System.String</span></span>

## <span data-ttu-id="b5050-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b5050-140">OUTPUTS</span></span>

### <span data-ttu-id="b5050-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b5050-141">System.Boolean</span></span>

## <span data-ttu-id="b5050-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="b5050-142">NOTES</span></span>

## <span data-ttu-id="b5050-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b5050-143">RELATED LINKS</span></span>

[<span data-ttu-id="b5050-144">Neu – AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b5050-144">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="b5050-145">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b5050-145">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="b5050-146">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b5050-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="b5050-147">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b5050-147">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
