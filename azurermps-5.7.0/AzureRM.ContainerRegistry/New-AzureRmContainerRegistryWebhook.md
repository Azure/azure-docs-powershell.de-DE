---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 0a23cfb79c341fb4fcee5b5688b0780ba178e978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497674"
---
# <span data-ttu-id="dd448-101">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="dd448-101">New-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="dd448-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd448-102">SYNOPSIS</span></span>
<span data-ttu-id="dd448-103">Erstellt einen Container Registrierungs webhook.</span><span class="sxs-lookup"><span data-stu-id="dd448-103">Creates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd448-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd448-104">SYNTAX</span></span>

### <span data-ttu-id="dd448-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd448-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd448-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd448-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd448-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd448-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd448-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd448-108">DESCRIPTION</span></span>
<span data-ttu-id="dd448-109">Das New-AzureRmContainerRegistryWebhook-Cmdlet erstellt einen Container Registrierungs-webhook.</span><span class="sxs-lookup"><span data-stu-id="dd448-109">The New-AzureRmContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="dd448-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd448-110">EXAMPLES</span></span>

### <span data-ttu-id="dd448-111">Beispiel 1: Erstellen eines Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="dd448-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="dd448-112">Erstellen Sie einen Container Registrierungs-webhook.</span><span class="sxs-lookup"><span data-stu-id="dd448-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="dd448-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd448-113">PARAMETERS</span></span>

### <span data-ttu-id="dd448-114">– Aktion</span><span class="sxs-lookup"><span data-stu-id="dd448-114">-Action</span></span>
<span data-ttu-id="dd448-115">Durch Leerzeichen getrennte Liste der Aktionen, die den webhook auslösen, um Benachrichtigungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="dd448-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd448-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd448-116">-Confirm</span></span>
<span data-ttu-id="dd448-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd448-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd448-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd448-118">-DefaultProfile</span></span>
<span data-ttu-id="dd448-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd448-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd448-120">-Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="dd448-120">-Header</span></span>
<span data-ttu-id="dd448-121">Benutzerdefinierte Header, die den webhook-Benachrichtigungen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="dd448-121">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd448-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="dd448-122">-Location</span></span>
<span data-ttu-id="dd448-123">Webhook-Position.</span><span class="sxs-lookup"><span data-stu-id="dd448-123">Webhook Location.</span></span>
<span data-ttu-id="dd448-124">Standardmäßig der Speicherort der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="dd448-124">Default to the location of the registry.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd448-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dd448-125">-Name</span></span>
<span data-ttu-id="dd448-126">Webhook-Name.</span><span class="sxs-lookup"><span data-stu-id="dd448-126">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd448-127">-Registry</span><span class="sxs-lookup"><span data-stu-id="dd448-127">-Registry</span></span>
<span data-ttu-id="dd448-128">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="dd448-128">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd448-129">-Registryname</span><span class="sxs-lookup"><span data-stu-id="dd448-129">-RegistryName</span></span>
<span data-ttu-id="dd448-130">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="dd448-130">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd448-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd448-131">-ResourceGroupName</span></span>
<span data-ttu-id="dd448-132">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dd448-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd448-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="dd448-133">-ResourceId</span></span>
<span data-ttu-id="dd448-134">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="dd448-134">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd448-135">-Scope</span><span class="sxs-lookup"><span data-stu-id="dd448-135">-Scope</span></span>
<span data-ttu-id="dd448-136">Webhook-Bereich.</span><span class="sxs-lookup"><span data-stu-id="dd448-136">Webhook scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd448-137">-Status</span><span class="sxs-lookup"><span data-stu-id="dd448-137">-Status</span></span>
<span data-ttu-id="dd448-138">Webhook-Status, Standardwert ist aktiviert</span><span class="sxs-lookup"><span data-stu-id="dd448-138">Webhook status, default value is enabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd448-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="dd448-139">-Tag</span></span>
<span data-ttu-id="dd448-140">Webhook-Tags.</span><span class="sxs-lookup"><span data-stu-id="dd448-140">Webhook tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd448-141">-URI</span><span class="sxs-lookup"><span data-stu-id="dd448-141">-Uri</span></span>
<span data-ttu-id="dd448-142">Der Dienst-URI für den webhook zum Veröffentlichen von Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="dd448-142">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd448-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd448-143">-WhatIf</span></span>
<span data-ttu-id="dd448-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd448-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd448-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd448-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd448-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd448-146">CommonParameters</span></span>
<span data-ttu-id="dd448-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd448-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd448-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd448-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd448-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd448-149">INPUTS</span></span>

### <span data-ttu-id="dd448-150">System. String</span><span class="sxs-lookup"><span data-stu-id="dd448-150">System.String</span></span>

## <span data-ttu-id="dd448-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd448-151">OUTPUTS</span></span>

### <span data-ttu-id="dd448-152">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="dd448-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="dd448-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd448-153">NOTES</span></span>

## <span data-ttu-id="dd448-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd448-154">RELATED LINKS</span></span>

[<span data-ttu-id="dd448-155">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="dd448-155">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="dd448-156">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="dd448-156">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="dd448-157">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="dd448-157">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="dd448-158">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="dd448-158">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
