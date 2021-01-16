---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 8ea10f2acbe69e31bf80e35f0a8ea1577ffac6f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308635"
---
# <span data-ttu-id="6eeae-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6eeae-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="6eeae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eeae-102">SYNOPSIS</span></span>
<span data-ttu-id="6eeae-103">Erstellt einen Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="6eeae-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="6eeae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6eeae-104">SYNTAX</span></span>

### <span data-ttu-id="6eeae-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6eeae-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6eeae-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eeae-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eeae-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eeae-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eeae-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6eeae-108">DESCRIPTION</span></span>
<span data-ttu-id="6eeae-109">Das New-AzContainerRegistryWebhook erstellt einen Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="6eeae-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="6eeae-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6eeae-110">EXAMPLES</span></span>

### <span data-ttu-id="6eeae-111">Beispiel 1: Erstellen eines Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="6eeae-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="6eeae-112">Erstellen Sie einen Containerregistrierungswebhook.</span><span class="sxs-lookup"><span data-stu-id="6eeae-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="6eeae-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6eeae-113">PARAMETERS</span></span>

### <span data-ttu-id="6eeae-114">-Action</span><span class="sxs-lookup"><span data-stu-id="6eeae-114">-Action</span></span>
<span data-ttu-id="6eeae-115">Liste mit getrennten Aktionen, die den Webhook zum Veröffentlichen von Benachrichtigungen auslösen.</span><span class="sxs-lookup"><span data-stu-id="6eeae-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="6eeae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eeae-116">-DefaultProfile</span></span>
<span data-ttu-id="6eeae-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6eeae-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eeae-118">-Header</span><span class="sxs-lookup"><span data-stu-id="6eeae-118">-Header</span></span>
<span data-ttu-id="6eeae-119">Benutzerdefinierte Header, die den Webhookbenachrichtigungen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6eeae-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="6eeae-120">-Location</span><span class="sxs-lookup"><span data-stu-id="6eeae-120">-Location</span></span>
<span data-ttu-id="6eeae-121">Webhook-Standort.</span><span class="sxs-lookup"><span data-stu-id="6eeae-121">Webhook Location.</span></span>
<span data-ttu-id="6eeae-122">Standardeinstellung für den Speicherort der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="6eeae-122">Default to the location of the registry.</span></span>

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

### <span data-ttu-id="6eeae-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6eeae-123">-Name</span></span>
<span data-ttu-id="6eeae-124">Name des Webhook.</span><span class="sxs-lookup"><span data-stu-id="6eeae-124">Webhook Name.</span></span>

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

### <span data-ttu-id="6eeae-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="6eeae-125">-Registry</span></span>
<span data-ttu-id="6eeae-126">Containerregistrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="6eeae-126">Container Registry Object.</span></span>

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

### <span data-ttu-id="6eeae-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="6eeae-127">-RegistryName</span></span>
<span data-ttu-id="6eeae-128">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="6eeae-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="6eeae-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eeae-129">-ResourceGroupName</span></span>
<span data-ttu-id="6eeae-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="6eeae-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="6eeae-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6eeae-131">-ResourceId</span></span>
<span data-ttu-id="6eeae-132">Die Containerregistrierungsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6eeae-132">The container registry resource id</span></span>

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

### <span data-ttu-id="6eeae-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="6eeae-133">-Scope</span></span>
<span data-ttu-id="6eeae-134">Bereich "Webhook".</span><span class="sxs-lookup"><span data-stu-id="6eeae-134">Webhook scope.</span></span>

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

### <span data-ttu-id="6eeae-135">-Status</span><span class="sxs-lookup"><span data-stu-id="6eeae-135">-Status</span></span>
<span data-ttu-id="6eeae-136">Webhook-Status, Standardwert ist aktiviert</span><span class="sxs-lookup"><span data-stu-id="6eeae-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="6eeae-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="6eeae-137">-Tag</span></span>
<span data-ttu-id="6eeae-138">Webhook-Tags.</span><span class="sxs-lookup"><span data-stu-id="6eeae-138">Webhook tags.</span></span>

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

### <span data-ttu-id="6eeae-139">-URI</span><span class="sxs-lookup"><span data-stu-id="6eeae-139">-Uri</span></span>
<span data-ttu-id="6eeae-140">Der Dienst-URI für das Webhook zum Posten von Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="6eeae-140">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="6eeae-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6eeae-141">-Confirm</span></span>
<span data-ttu-id="6eeae-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6eeae-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eeae-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6eeae-143">-WhatIf</span></span>
<span data-ttu-id="6eeae-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6eeae-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eeae-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6eeae-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eeae-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eeae-146">CommonParameters</span></span>
<span data-ttu-id="6eeae-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eeae-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eeae-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6eeae-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eeae-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6eeae-149">INPUTS</span></span>

### <span data-ttu-id="6eeae-150">System.String</span><span class="sxs-lookup"><span data-stu-id="6eeae-150">System.String</span></span>

## <span data-ttu-id="6eeae-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6eeae-151">OUTPUTS</span></span>

### <span data-ttu-id="6eeae-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6eeae-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="6eeae-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6eeae-153">NOTES</span></span>

## <span data-ttu-id="6eeae-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6eeae-154">RELATED LINKS</span></span>

[<span data-ttu-id="6eeae-155">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6eeae-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="6eeae-156">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6eeae-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="6eeae-157">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6eeae-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="6eeae-158">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6eeae-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)