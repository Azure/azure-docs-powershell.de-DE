---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 7515046ed6e9fd6ba5c64b8123f8113b28b53f9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662952"
---
# <span data-ttu-id="d5d11-101">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d5d11-101">Update-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="d5d11-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5d11-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d11-103">Aktualisiert einen Container Registrierungs-webhook.</span><span class="sxs-lookup"><span data-stu-id="d5d11-103">Updates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5d11-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5d11-104">SYNTAX</span></span>

### <span data-ttu-id="d5d11-105">ResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5d11-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5d11-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5d11-106">NameResourceGroupParameterSet</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5d11-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5d11-107">WebhookObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5d11-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5d11-108">DESCRIPTION</span></span>
<span data-ttu-id="d5d11-109">Das Update-AzureRmContainerRegistryWebhook-Cmdlet aktualisiert einen Container Registrierungs-webhook.</span><span class="sxs-lookup"><span data-stu-id="d5d11-109">The Update-AzureRmContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="d5d11-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5d11-110">EXAMPLES</span></span>

### <span data-ttu-id="d5d11-111">Beispiel 1: Aktualisieren eines vorhandenen Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="d5d11-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="d5d11-112">Aktualisieren eines vorhandenen Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="d5d11-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="d5d11-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5d11-113">PARAMETERS</span></span>

### <span data-ttu-id="d5d11-114">– Aktion</span><span class="sxs-lookup"><span data-stu-id="d5d11-114">-Action</span></span>
<span data-ttu-id="d5d11-115">Durch Leerzeichen getrennte Liste der Aktionen, die den webhook auslösen, um Benachrichtigungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="d5d11-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d11-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d11-116">-DefaultProfile</span></span>
<span data-ttu-id="d5d11-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5d11-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5d11-118">-Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="d5d11-118">-Header</span></span>
<span data-ttu-id="d5d11-119">Durch Leerzeichen getrennte benutzerdefinierte Überschriften im Format "Schlüssel \[ = Wert \] ", das den webhook-Benachrichtigungen hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d5d11-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="d5d11-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d5d11-120">-Name</span></span>
<span data-ttu-id="d5d11-121">Webhook-Name.</span><span class="sxs-lookup"><span data-stu-id="d5d11-121">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d11-122">-Registryname</span><span class="sxs-lookup"><span data-stu-id="d5d11-122">-RegistryName</span></span>
<span data-ttu-id="d5d11-123">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="d5d11-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="d5d11-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5d11-124">-ResourceGroupName</span></span>
<span data-ttu-id="d5d11-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d5d11-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="d5d11-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d5d11-126">-ResourceId</span></span>
<span data-ttu-id="d5d11-127">Die Ressourcen-ID des Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="d5d11-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="d5d11-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="d5d11-128">-Scope</span></span>
<span data-ttu-id="d5d11-129">Webhook-Bereich.</span><span class="sxs-lookup"><span data-stu-id="d5d11-129">Webhook scope.</span></span>

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

### <span data-ttu-id="d5d11-130">-Status</span><span class="sxs-lookup"><span data-stu-id="d5d11-130">-Status</span></span>
<span data-ttu-id="d5d11-131">Webhook-Status</span><span class="sxs-lookup"><span data-stu-id="d5d11-131">Webhook status</span></span>

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

### <span data-ttu-id="d5d11-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="d5d11-132">-Tag</span></span>
<span data-ttu-id="d5d11-133">Leerzeichen getrennte Tags im Format "Schlüssel \[ = Wert \] ".</span><span class="sxs-lookup"><span data-stu-id="d5d11-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="d5d11-134">-URI</span><span class="sxs-lookup"><span data-stu-id="d5d11-134">-Uri</span></span>
<span data-ttu-id="d5d11-135">Der Dienst-URI für den webhook zum Veröffentlichen von Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="d5d11-135">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d11-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="d5d11-136">-Webhook</span></span>
<span data-ttu-id="d5d11-137">Container Registrierungs webhook-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d5d11-137">Container Registry Webhook Object.</span></span>

```yaml
Type: PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5d11-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d5d11-138">-Confirm</span></span>
<span data-ttu-id="d5d11-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5d11-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5d11-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5d11-140">-WhatIf</span></span>
<span data-ttu-id="d5d11-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5d11-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5d11-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5d11-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5d11-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d11-143">CommonParameters</span></span>
<span data-ttu-id="d5d11-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5d11-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d11-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5d11-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d11-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5d11-146">INPUTS</span></span>

### <span data-ttu-id="d5d11-147">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d5d11-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="d5d11-148">System. String</span><span class="sxs-lookup"><span data-stu-id="d5d11-148">System.String</span></span>

## <span data-ttu-id="d5d11-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5d11-149">OUTPUTS</span></span>

### <span data-ttu-id="d5d11-150">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d5d11-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="d5d11-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5d11-151">NOTES</span></span>

## <span data-ttu-id="d5d11-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5d11-152">RELATED LINKS</span></span>

[<span data-ttu-id="d5d11-153">Neu – AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d5d11-153">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="d5d11-154">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d5d11-154">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="d5d11-155">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d5d11-155">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="d5d11-156">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d5d11-156">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
