---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 36bc713561c739804b358e4b778e17740bd9fb6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931352"
---
# <span data-ttu-id="5fc11-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="5fc11-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="5fc11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fc11-102">SYNOPSIS</span></span>
<span data-ttu-id="5fc11-103">Ruft einen Containerregistrierungswebhook ab.</span><span class="sxs-lookup"><span data-stu-id="5fc11-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="5fc11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fc11-104">SYNTAX</span></span>

### <span data-ttu-id="5fc11-105">ListWebhookByNameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5fc11-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fc11-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fc11-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fc11-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fc11-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fc11-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fc11-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fc11-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fc11-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fc11-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fc11-110">DESCRIPTION</span></span>
<span data-ttu-id="5fc11-111">Das Get-AzContainerRegistryWebhook-Cmdlet ruft einen angegebenen Webhook der Containerregistrierung oder alle Webhooks einer Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="5fc11-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="5fc11-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5fc11-112">EXAMPLES</span></span>

### <span data-ttu-id="5fc11-113">Beispiel 1: Erhalten eines angegebenen Webhooks einer Containerregistrierung</span><span class="sxs-lookup"><span data-stu-id="5fc11-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="5fc11-114">Einen angegebenen Webhook einer Containerregistrierung</span><span class="sxs-lookup"><span data-stu-id="5fc11-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="5fc11-115">Beispiel 2: Alle Webhooks einer Containerregistrierung</span><span class="sxs-lookup"><span data-stu-id="5fc11-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="5fc11-116">Alle Webhooks einer Containerregistrierung</span><span class="sxs-lookup"><span data-stu-id="5fc11-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="5fc11-117">Beispiel 3: Erhalten eines angegebenen Webhooks einer Containerregistrierung mit Konfigurationsdetails</span><span class="sxs-lookup"><span data-stu-id="5fc11-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="5fc11-118">Erhalten eines angegebenen Webhooks einer Containerregistrierung mit Konfigurationsdetails</span><span class="sxs-lookup"><span data-stu-id="5fc11-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="5fc11-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5fc11-119">PARAMETERS</span></span>

### <span data-ttu-id="5fc11-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fc11-120">-DefaultProfile</span></span>
<span data-ttu-id="5fc11-121">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fc11-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fc11-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="5fc11-122">-IncludeConfiguration</span></span>
<span data-ttu-id="5fc11-123">Hier erhalten Sie die Konfigurationsinformationen für einen Webhook.</span><span class="sxs-lookup"><span data-stu-id="5fc11-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="5fc11-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5fc11-124">-Name</span></span>
<span data-ttu-id="5fc11-125">Webhookname.</span><span class="sxs-lookup"><span data-stu-id="5fc11-125">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc11-126">-Registrierung</span><span class="sxs-lookup"><span data-stu-id="5fc11-126">-Registry</span></span>
<span data-ttu-id="5fc11-127">Containerregistrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="5fc11-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc11-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="5fc11-128">-RegistryName</span></span>
<span data-ttu-id="5fc11-129">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="5fc11-129">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc11-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fc11-130">-ResourceGroupName</span></span>
<span data-ttu-id="5fc11-131">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="5fc11-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc11-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fc11-132">-ResourceId</span></span>
<span data-ttu-id="5fc11-133">Die Containerregistrierungs-Webhook-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="5fc11-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="5fc11-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fc11-134">CommonParameters</span></span>
<span data-ttu-id="5fc11-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fc11-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fc11-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fc11-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fc11-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5fc11-137">INPUTS</span></span>

### <span data-ttu-id="5fc11-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5fc11-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="5fc11-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5fc11-139">System.String</span></span>

## <span data-ttu-id="5fc11-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5fc11-140">OUTPUTS</span></span>

### <span data-ttu-id="5fc11-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="5fc11-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="5fc11-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5fc11-142">NOTES</span></span>

## <span data-ttu-id="5fc11-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5fc11-143">RELATED LINKS</span></span>

[<span data-ttu-id="5fc11-144">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="5fc11-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="5fc11-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="5fc11-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="5fc11-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="5fc11-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="5fc11-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="5fc11-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)