---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 231ff710e2c8c2945947ecf2d09845e635ee6244
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176951"
---
# <span data-ttu-id="1cddb-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1cddb-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="1cddb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1cddb-102">SYNOPSIS</span></span>
<span data-ttu-id="1cddb-103">Ruft einen Container Registrierungs webhook ab.</span><span class="sxs-lookup"><span data-stu-id="1cddb-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="1cddb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cddb-104">SYNTAX</span></span>

### <span data-ttu-id="1cddb-105">ListWebhookByNameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1cddb-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cddb-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cddb-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cddb-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cddb-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cddb-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cddb-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cddb-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cddb-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cddb-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1cddb-110">DESCRIPTION</span></span>
<span data-ttu-id="1cddb-111">Das Get-AzContainerRegistryWebhook-Cmdlet ruft einen angegebenen webhook der Container Registrierung oder alle webhooks einer Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="1cddb-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="1cddb-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1cddb-112">EXAMPLES</span></span>

### <span data-ttu-id="1cddb-113">Beispiel 1: Abrufen eines angegebenen webhooks einer Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="1cddb-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="1cddb-114">Abrufen eines angegebenen webhooks einer Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="1cddb-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="1cddb-115">Beispiel 2: Abrufen aller webhooks einer Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="1cddb-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="1cddb-116">Abrufen aller webhooks einer Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="1cddb-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="1cddb-117">Beispiel 3: Abrufen eines angegebenen webhooks einer Container Registrierung mit Konfigurationsdetails</span><span class="sxs-lookup"><span data-stu-id="1cddb-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="1cddb-118">Abrufen eines angegebenen webhooks einer Container Registrierung mit Konfigurationsdetails</span><span class="sxs-lookup"><span data-stu-id="1cddb-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="1cddb-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cddb-119">PARAMETERS</span></span>

### <span data-ttu-id="1cddb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cddb-120">-DefaultProfile</span></span>
<span data-ttu-id="1cddb-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1cddb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cddb-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="1cddb-122">-IncludeConfiguration</span></span>
<span data-ttu-id="1cddb-123">Rufen Sie die Konfigurationsinformationen für einen webhook ab.</span><span class="sxs-lookup"><span data-stu-id="1cddb-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="1cddb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1cddb-124">-Name</span></span>
<span data-ttu-id="1cddb-125">Webhook-Name.</span><span class="sxs-lookup"><span data-stu-id="1cddb-125">Webhook Name.</span></span>

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

### <span data-ttu-id="1cddb-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="1cddb-126">-Registry</span></span>
<span data-ttu-id="1cddb-127">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="1cddb-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="1cddb-128">-Registryname</span><span class="sxs-lookup"><span data-stu-id="1cddb-128">-RegistryName</span></span>
<span data-ttu-id="1cddb-129">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="1cddb-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="1cddb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cddb-130">-ResourceGroupName</span></span>
<span data-ttu-id="1cddb-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1cddb-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="1cddb-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1cddb-132">-ResourceId</span></span>
<span data-ttu-id="1cddb-133">Die Ressourcen-ID des Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="1cddb-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="1cddb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cddb-134">CommonParameters</span></span>
<span data-ttu-id="1cddb-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cddb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cddb-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cddb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cddb-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1cddb-137">INPUTS</span></span>

### <span data-ttu-id="1cddb-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1cddb-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="1cddb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1cddb-139">System.String</span></span>

## <span data-ttu-id="1cddb-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1cddb-140">OUTPUTS</span></span>

### <span data-ttu-id="1cddb-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1cddb-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="1cddb-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="1cddb-142">NOTES</span></span>

## <span data-ttu-id="1cddb-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1cddb-143">RELATED LINKS</span></span>

[<span data-ttu-id="1cddb-144">Neu – AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1cddb-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="1cddb-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1cddb-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="1cddb-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1cddb-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="1cddb-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1cddb-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)