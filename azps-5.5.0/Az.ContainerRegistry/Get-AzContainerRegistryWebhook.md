---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 231ff710e2c8c2945947ecf2d09845e635ee6244
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148700"
---
# <span data-ttu-id="a33d5-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a33d5-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="a33d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a33d5-102">SYNOPSIS</span></span>
<span data-ttu-id="a33d5-103">Ruft einen Containerregistrierungswebhook ab.</span><span class="sxs-lookup"><span data-stu-id="a33d5-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="a33d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a33d5-104">SYNTAX</span></span>

### <span data-ttu-id="a33d5-105">ListWebhookByNameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a33d5-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a33d5-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="a33d5-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a33d5-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a33d5-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a33d5-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a33d5-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a33d5-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a33d5-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a33d5-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a33d5-110">DESCRIPTION</span></span>
<span data-ttu-id="a33d5-111">Das Get-AzContainerRegistryWebhook-Cmdlet ruft einen angegebenen Webhook der Containerregistrierung oder alle Webhooks einer Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="a33d5-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="a33d5-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a33d5-112">EXAMPLES</span></span>

### <span data-ttu-id="a33d5-113">Beispiel 1: Einen angegebenen Webhook einer Containerregistrierung erhalten</span><span class="sxs-lookup"><span data-stu-id="a33d5-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="a33d5-114">Einen angegebenen Webhook einer Containerregistrierung erhalten</span><span class="sxs-lookup"><span data-stu-id="a33d5-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="a33d5-115">Beispiel 2: Alle Webhooks einer Containerregistrierung erhalten</span><span class="sxs-lookup"><span data-stu-id="a33d5-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="a33d5-116">Alle Webhooks einer Containerregistrierung erhalten</span><span class="sxs-lookup"><span data-stu-id="a33d5-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="a33d5-117">Beispiel 3: Einen angegebenen Webhook einer Containerregistrierung mit Konfigurationsdetails erhalten</span><span class="sxs-lookup"><span data-stu-id="a33d5-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="a33d5-118">Einen angegebenen Webhook einer Containerregistrierung mit Konfigurationsdetails erhalten</span><span class="sxs-lookup"><span data-stu-id="a33d5-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="a33d5-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a33d5-119">PARAMETERS</span></span>

### <span data-ttu-id="a33d5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a33d5-120">-DefaultProfile</span></span>
<span data-ttu-id="a33d5-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a33d5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a33d5-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a33d5-122">-IncludeConfiguration</span></span>
<span data-ttu-id="a33d5-123">Erhalten Sie die Konfigurationsinformationen für einen Webhook.</span><span class="sxs-lookup"><span data-stu-id="a33d5-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="a33d5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a33d5-124">-Name</span></span>
<span data-ttu-id="a33d5-125">Name des Webhook.</span><span class="sxs-lookup"><span data-stu-id="a33d5-125">Webhook Name.</span></span>

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

### <span data-ttu-id="a33d5-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="a33d5-126">-Registry</span></span>
<span data-ttu-id="a33d5-127">Containerregistrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="a33d5-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="a33d5-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="a33d5-128">-RegistryName</span></span>
<span data-ttu-id="a33d5-129">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="a33d5-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="a33d5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a33d5-130">-ResourceGroupName</span></span>
<span data-ttu-id="a33d5-131">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="a33d5-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="a33d5-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a33d5-132">-ResourceId</span></span>
<span data-ttu-id="a33d5-133">Die Containerregistrierungs-Webhook-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a33d5-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="a33d5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a33d5-134">CommonParameters</span></span>
<span data-ttu-id="a33d5-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a33d5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a33d5-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a33d5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a33d5-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a33d5-137">INPUTS</span></span>

### <span data-ttu-id="a33d5-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a33d5-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="a33d5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a33d5-139">System.String</span></span>

## <span data-ttu-id="a33d5-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a33d5-140">OUTPUTS</span></span>

### <span data-ttu-id="a33d5-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a33d5-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="a33d5-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a33d5-142">NOTES</span></span>

## <span data-ttu-id="a33d5-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a33d5-143">RELATED LINKS</span></span>

[<span data-ttu-id="a33d5-144">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a33d5-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="a33d5-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a33d5-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="a33d5-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a33d5-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="a33d5-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a33d5-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)