---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: 2343b58891109d829a37131dff084b2b51e7f8ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299608"
---
# <span data-ttu-id="fce5a-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fce5a-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="fce5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fce5a-102">SYNOPSIS</span></span>
<span data-ttu-id="fce5a-103">Aktualisiert einen Container Registrierungs-webhook.</span><span class="sxs-lookup"><span data-stu-id="fce5a-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="fce5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fce5a-104">SYNTAX</span></span>

### <span data-ttu-id="fce5a-105">ResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fce5a-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fce5a-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="fce5a-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fce5a-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fce5a-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fce5a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fce5a-108">DESCRIPTION</span></span>
<span data-ttu-id="fce5a-109">Das Update-AzContainerRegistryWebhook-Cmdlet aktualisiert einen Container Registrierungs-webhook.</span><span class="sxs-lookup"><span data-stu-id="fce5a-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="fce5a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fce5a-110">EXAMPLES</span></span>

### <span data-ttu-id="fce5a-111">Beispiel 1: Aktualisieren eines vorhandenen Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="fce5a-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="fce5a-112">Aktualisieren eines vorhandenen Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="fce5a-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="fce5a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fce5a-113">PARAMETERS</span></span>

### <span data-ttu-id="fce5a-114">– Aktion</span><span class="sxs-lookup"><span data-stu-id="fce5a-114">-Action</span></span>
<span data-ttu-id="fce5a-115">Durch Leerzeichen getrennte Liste der Aktionen, die den webhook auslösen, um Benachrichtigungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="fce5a-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="fce5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fce5a-116">-DefaultProfile</span></span>
<span data-ttu-id="fce5a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fce5a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fce5a-118">-Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="fce5a-118">-Header</span></span>
<span data-ttu-id="fce5a-119">Durch Leerzeichen getrennte benutzerdefinierte Überschriften im Format "Schlüssel \[ = Wert \] ", das den webhook-Benachrichtigungen hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="fce5a-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="fce5a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fce5a-120">-Name</span></span>
<span data-ttu-id="fce5a-121">Webhook-Name.</span><span class="sxs-lookup"><span data-stu-id="fce5a-121">Webhook Name.</span></span>

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

### <span data-ttu-id="fce5a-122">-Registryname</span><span class="sxs-lookup"><span data-stu-id="fce5a-122">-RegistryName</span></span>
<span data-ttu-id="fce5a-123">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="fce5a-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="fce5a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fce5a-124">-ResourceGroupName</span></span>
<span data-ttu-id="fce5a-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fce5a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="fce5a-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fce5a-126">-ResourceId</span></span>
<span data-ttu-id="fce5a-127">Die Ressourcen-ID des Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="fce5a-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="fce5a-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="fce5a-128">-Scope</span></span>
<span data-ttu-id="fce5a-129">Webhook-Bereich.</span><span class="sxs-lookup"><span data-stu-id="fce5a-129">Webhook scope.</span></span>

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

### <span data-ttu-id="fce5a-130">-Status</span><span class="sxs-lookup"><span data-stu-id="fce5a-130">-Status</span></span>
<span data-ttu-id="fce5a-131">Webhook-Status</span><span class="sxs-lookup"><span data-stu-id="fce5a-131">Webhook status</span></span>

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

### <span data-ttu-id="fce5a-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="fce5a-132">-Tag</span></span>
<span data-ttu-id="fce5a-133">Leerzeichen getrennte Tags im Format "Schlüssel \[ = Wert \] ".</span><span class="sxs-lookup"><span data-stu-id="fce5a-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="fce5a-134">-URI</span><span class="sxs-lookup"><span data-stu-id="fce5a-134">-Uri</span></span>
<span data-ttu-id="fce5a-135">Der Dienst-URI für den webhook zum Veröffentlichen von Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="fce5a-135">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="fce5a-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="fce5a-136">-Webhook</span></span>
<span data-ttu-id="fce5a-137">Container Registrierungs webhook-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fce5a-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="fce5a-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fce5a-138">-Confirm</span></span>
<span data-ttu-id="fce5a-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fce5a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fce5a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fce5a-140">-WhatIf</span></span>
<span data-ttu-id="fce5a-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fce5a-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fce5a-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fce5a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fce5a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce5a-143">CommonParameters</span></span>
<span data-ttu-id="fce5a-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fce5a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce5a-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fce5a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce5a-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fce5a-146">INPUTS</span></span>

### <span data-ttu-id="fce5a-147">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fce5a-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="fce5a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="fce5a-148">System.String</span></span>

## <span data-ttu-id="fce5a-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fce5a-149">OUTPUTS</span></span>

### <span data-ttu-id="fce5a-150">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fce5a-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="fce5a-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="fce5a-151">NOTES</span></span>

## <span data-ttu-id="fce5a-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fce5a-152">RELATED LINKS</span></span>

[<span data-ttu-id="fce5a-153">Neu – AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fce5a-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fce5a-154">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fce5a-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fce5a-155">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fce5a-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fce5a-156">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fce5a-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)