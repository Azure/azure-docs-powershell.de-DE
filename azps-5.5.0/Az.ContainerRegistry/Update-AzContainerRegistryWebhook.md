---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: 2343b58891109d829a37131dff084b2b51e7f8ad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144556"
---
# <span data-ttu-id="a1d47-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1d47-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="a1d47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1d47-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d47-103">Aktualisiert einen Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="a1d47-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="a1d47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1d47-104">SYNTAX</span></span>

### <span data-ttu-id="a1d47-105">ResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1d47-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1d47-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1d47-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1d47-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1d47-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1d47-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1d47-108">DESCRIPTION</span></span>
<span data-ttu-id="a1d47-109">Das Update-AzContainerRegistryWebhook aktualisiert einen Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="a1d47-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="a1d47-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a1d47-110">EXAMPLES</span></span>

### <span data-ttu-id="a1d47-111">Beispiel 1: Aktualisieren eines vorhandenen Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="a1d47-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="a1d47-112">Aktualisieren Sie einen vorhandenen Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="a1d47-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="a1d47-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1d47-113">PARAMETERS</span></span>

### <span data-ttu-id="a1d47-114">-Aktion</span><span class="sxs-lookup"><span data-stu-id="a1d47-114">-Action</span></span>
<span data-ttu-id="a1d47-115">Liste mit getrennten Aktionen, die das Veröffentlichen von Benachrichtigungen durch den Webhook auslösen.</span><span class="sxs-lookup"><span data-stu-id="a1d47-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d47-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d47-116">-DefaultProfile</span></span>
<span data-ttu-id="a1d47-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1d47-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1d47-118">-Header</span><span class="sxs-lookup"><span data-stu-id="a1d47-118">-Header</span></span>
<span data-ttu-id="a1d47-119">Getrennter Speicherplatz für benutzerdefinierte Header im "key \[ =value"-Format, \] das den Webhookbenachrichtigungen hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a1d47-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d47-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a1d47-120">-Name</span></span>
<span data-ttu-id="a1d47-121">Name des Webhook.</span><span class="sxs-lookup"><span data-stu-id="a1d47-121">Webhook Name.</span></span>

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

### <span data-ttu-id="a1d47-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="a1d47-122">-RegistryName</span></span>
<span data-ttu-id="a1d47-123">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="a1d47-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="a1d47-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d47-124">-ResourceGroupName</span></span>
<span data-ttu-id="a1d47-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="a1d47-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a1d47-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1d47-126">-ResourceId</span></span>
<span data-ttu-id="a1d47-127">Die Containerregistrierungs-Webhook-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a1d47-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="a1d47-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="a1d47-128">-Scope</span></span>
<span data-ttu-id="a1d47-129">Bereich "Webhook".</span><span class="sxs-lookup"><span data-stu-id="a1d47-129">Webhook scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d47-130">-Status</span><span class="sxs-lookup"><span data-stu-id="a1d47-130">-Status</span></span>
<span data-ttu-id="a1d47-131">Webhookstatus</span><span class="sxs-lookup"><span data-stu-id="a1d47-131">Webhook status</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d47-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="a1d47-132">-Tag</span></span>
<span data-ttu-id="a1d47-133">Leerzeichen getrennte Tags im Format "key \[ \] =value".</span><span class="sxs-lookup"><span data-stu-id="a1d47-133">Space separated tags in 'key\[=value\]' format.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d47-134">-URI</span><span class="sxs-lookup"><span data-stu-id="a1d47-134">-Uri</span></span>
<span data-ttu-id="a1d47-135">Der Dienst-URI für das Webhook zum Posten von Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="a1d47-135">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d47-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="a1d47-136">-Webhook</span></span>
<span data-ttu-id="a1d47-137">Container Registry Webhook-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a1d47-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="a1d47-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1d47-138">-Confirm</span></span>
<span data-ttu-id="a1d47-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1d47-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1d47-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a1d47-140">-WhatIf</span></span>
<span data-ttu-id="a1d47-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1d47-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1d47-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1d47-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1d47-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d47-143">CommonParameters</span></span>
<span data-ttu-id="a1d47-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1d47-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d47-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1d47-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d47-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a1d47-146">INPUTS</span></span>

### <span data-ttu-id="a1d47-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1d47-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="a1d47-148">System.String</span><span class="sxs-lookup"><span data-stu-id="a1d47-148">System.String</span></span>

## <span data-ttu-id="a1d47-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a1d47-149">OUTPUTS</span></span>

### <span data-ttu-id="a1d47-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1d47-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="a1d47-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a1d47-151">NOTES</span></span>

## <span data-ttu-id="a1d47-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a1d47-152">RELATED LINKS</span></span>

[<span data-ttu-id="a1d47-153">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1d47-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="a1d47-154">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1d47-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="a1d47-155">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1d47-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="a1d47-156">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1d47-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)