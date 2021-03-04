---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 10acca5a89c4ea84d475e5eea2e89e18942116f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930344"
---
# <span data-ttu-id="c7008-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c7008-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="c7008-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7008-102">SYNOPSIS</span></span>
<span data-ttu-id="c7008-103">Erstellt einen Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="c7008-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="c7008-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7008-104">SYNTAX</span></span>

### <span data-ttu-id="c7008-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7008-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7008-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7008-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7008-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7008-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7008-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7008-108">DESCRIPTION</span></span>
<span data-ttu-id="c7008-109">Das New-AzContainerRegistryWebhook-Cmdlet erstellt einen Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="c7008-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="c7008-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c7008-110">EXAMPLES</span></span>

### <span data-ttu-id="c7008-111">Beispiel 1: Erstellen eines Containerregistrierungswebhooks.</span><span class="sxs-lookup"><span data-stu-id="c7008-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="c7008-112">Erstellen Sie einen Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="c7008-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="c7008-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c7008-113">PARAMETERS</span></span>

### <span data-ttu-id="c7008-114">-Aktion</span><span class="sxs-lookup"><span data-stu-id="c7008-114">-Action</span></span>
<span data-ttu-id="c7008-115">Leerraum getrennte Liste der Aktionen, die den Webhook auslösen, um Benachrichtigungen zu posten.</span><span class="sxs-lookup"><span data-stu-id="c7008-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7008-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7008-116">-DefaultProfile</span></span>
<span data-ttu-id="c7008-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7008-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7008-118">-Header</span><span class="sxs-lookup"><span data-stu-id="c7008-118">-Header</span></span>
<span data-ttu-id="c7008-119">Benutzerdefinierte Kopfzeilen, die den Webhookbenachrichtigungen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c7008-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="c7008-120">-Location</span><span class="sxs-lookup"><span data-stu-id="c7008-120">-Location</span></span>
<span data-ttu-id="c7008-121">Webhookspeicherort.</span><span class="sxs-lookup"><span data-stu-id="c7008-121">Webhook Location.</span></span>
<span data-ttu-id="c7008-122">Standardmäßig für den Speicherort der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="c7008-122">Default to the location of the registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7008-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c7008-123">-Name</span></span>
<span data-ttu-id="c7008-124">Webhookname.</span><span class="sxs-lookup"><span data-stu-id="c7008-124">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7008-125">-Registrierung</span><span class="sxs-lookup"><span data-stu-id="c7008-125">-Registry</span></span>
<span data-ttu-id="c7008-126">Containerregistrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c7008-126">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7008-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c7008-127">-RegistryName</span></span>
<span data-ttu-id="c7008-128">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="c7008-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="c7008-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7008-129">-ResourceGroupName</span></span>
<span data-ttu-id="c7008-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="c7008-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="c7008-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7008-131">-ResourceId</span></span>
<span data-ttu-id="c7008-132">Die Containerregistrierungsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c7008-132">The container registry resource id</span></span>

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

### <span data-ttu-id="c7008-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="c7008-133">-Scope</span></span>
<span data-ttu-id="c7008-134">Bereich "Webhook".</span><span class="sxs-lookup"><span data-stu-id="c7008-134">Webhook scope.</span></span>

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

### <span data-ttu-id="c7008-135">-Status</span><span class="sxs-lookup"><span data-stu-id="c7008-135">-Status</span></span>
<span data-ttu-id="c7008-136">Webhook-Status, Standardwert aktiviert</span><span class="sxs-lookup"><span data-stu-id="c7008-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="c7008-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="c7008-137">-Tag</span></span>
<span data-ttu-id="c7008-138">Webhook-Tags.</span><span class="sxs-lookup"><span data-stu-id="c7008-138">Webhook tags.</span></span>

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

### <span data-ttu-id="c7008-139">-URI</span><span class="sxs-lookup"><span data-stu-id="c7008-139">-Uri</span></span>
<span data-ttu-id="c7008-140">Der Dienst-URI für das Webhook zum Posten von Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="c7008-140">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7008-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c7008-141">-Confirm</span></span>
<span data-ttu-id="c7008-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7008-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7008-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7008-143">-WhatIf</span></span>
<span data-ttu-id="c7008-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7008-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7008-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7008-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7008-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7008-146">CommonParameters</span></span>
<span data-ttu-id="c7008-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7008-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7008-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7008-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7008-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c7008-149">INPUTS</span></span>

### <span data-ttu-id="c7008-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c7008-150">System.String</span></span>

## <span data-ttu-id="c7008-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c7008-151">OUTPUTS</span></span>

### <span data-ttu-id="c7008-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c7008-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="c7008-153">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c7008-153">NOTES</span></span>

## <span data-ttu-id="c7008-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c7008-154">RELATED LINKS</span></span>

[<span data-ttu-id="c7008-155">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c7008-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="c7008-156">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c7008-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="c7008-157">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c7008-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="c7008-158">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c7008-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)