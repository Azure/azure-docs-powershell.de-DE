---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 061b712f0c9e2d77d4dab70a0e39051d5f92d7ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820460"
---
# <span data-ttu-id="cb5c6-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cb5c6-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="cb5c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb5c6-102">SYNOPSIS</span></span>
<span data-ttu-id="cb5c6-103">Erstellt einen Container Registrierungs webhook.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="cb5c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb5c6-104">SYNTAX</span></span>

### <span data-ttu-id="cb5c6-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cb5c6-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb5c6-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb5c6-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb5c6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb5c6-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb5c6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb5c6-108">DESCRIPTION</span></span>
<span data-ttu-id="cb5c6-109">Das New-AzContainerRegistryWebhook-Cmdlet erstellt einen Container Registrierungs-webhook.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="cb5c6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb5c6-110">EXAMPLES</span></span>

### <span data-ttu-id="cb5c6-111">Beispiel 1: Erstellen eines Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="cb5c6-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="cb5c6-112">Erstellen Sie einen Container Registrierungs-webhook.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="cb5c6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb5c6-113">PARAMETERS</span></span>

### <span data-ttu-id="cb5c6-114">– Aktion</span><span class="sxs-lookup"><span data-stu-id="cb5c6-114">-Action</span></span>
<span data-ttu-id="cb5c6-115">Durch Leerzeichen getrennte Liste der Aktionen, die den webhook auslösen, um Benachrichtigungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="cb5c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb5c6-116">-DefaultProfile</span></span>
<span data-ttu-id="cb5c6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb5c6-118">-Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="cb5c6-118">-Header</span></span>
<span data-ttu-id="cb5c6-119">Benutzerdefinierte Header, die den webhook-Benachrichtigungen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="cb5c6-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="cb5c6-120">-Location</span></span>
<span data-ttu-id="cb5c6-121">Webhook-Position.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-121">Webhook Location.</span></span>
<span data-ttu-id="cb5c6-122">Standardmäßig der Speicherort der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-122">Default to the location of the registry.</span></span>

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

### <span data-ttu-id="cb5c6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cb5c6-123">-Name</span></span>
<span data-ttu-id="cb5c6-124">Webhook-Name.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-124">Webhook Name.</span></span>

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

### <span data-ttu-id="cb5c6-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="cb5c6-125">-Registry</span></span>
<span data-ttu-id="cb5c6-126">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-126">Container Registry Object.</span></span>

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

### <span data-ttu-id="cb5c6-127">-Registryname</span><span class="sxs-lookup"><span data-stu-id="cb5c6-127">-RegistryName</span></span>
<span data-ttu-id="cb5c6-128">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="cb5c6-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="cb5c6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb5c6-129">-ResourceGroupName</span></span>
<span data-ttu-id="cb5c6-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="cb5c6-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cb5c6-131">-ResourceId</span></span>
<span data-ttu-id="cb5c6-132">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="cb5c6-132">The container registry resource id</span></span>

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

### <span data-ttu-id="cb5c6-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="cb5c6-133">-Scope</span></span>
<span data-ttu-id="cb5c6-134">Webhook-Bereich.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-134">Webhook scope.</span></span>

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

### <span data-ttu-id="cb5c6-135">-Status</span><span class="sxs-lookup"><span data-stu-id="cb5c6-135">-Status</span></span>
<span data-ttu-id="cb5c6-136">Webhook-Status, Standardwert ist aktiviert</span><span class="sxs-lookup"><span data-stu-id="cb5c6-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="cb5c6-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="cb5c6-137">-Tag</span></span>
<span data-ttu-id="cb5c6-138">Webhook-Tags.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-138">Webhook tags.</span></span>

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

### <span data-ttu-id="cb5c6-139">-URI</span><span class="sxs-lookup"><span data-stu-id="cb5c6-139">-Uri</span></span>
<span data-ttu-id="cb5c6-140">Der Dienst-URI für den webhook zum Veröffentlichen von Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-140">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="cb5c6-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cb5c6-141">-Confirm</span></span>
<span data-ttu-id="cb5c6-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb5c6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb5c6-143">-WhatIf</span></span>
<span data-ttu-id="cb5c6-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb5c6-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb5c6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb5c6-146">CommonParameters</span></span>
<span data-ttu-id="cb5c6-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb5c6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb5c6-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb5c6-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb5c6-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb5c6-149">INPUTS</span></span>

### <span data-ttu-id="cb5c6-150">System. String</span><span class="sxs-lookup"><span data-stu-id="cb5c6-150">System.String</span></span>

## <span data-ttu-id="cb5c6-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb5c6-151">OUTPUTS</span></span>

### <span data-ttu-id="cb5c6-152">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cb5c6-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="cb5c6-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb5c6-153">NOTES</span></span>

## <span data-ttu-id="cb5c6-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb5c6-154">RELATED LINKS</span></span>

[<span data-ttu-id="cb5c6-155">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cb5c6-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="cb5c6-156">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cb5c6-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="cb5c6-157">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cb5c6-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="cb5c6-158">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cb5c6-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)