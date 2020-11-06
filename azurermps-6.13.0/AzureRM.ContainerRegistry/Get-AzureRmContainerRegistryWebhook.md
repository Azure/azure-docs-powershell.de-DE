---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: d2fee7d402ddf25a2bcc4b32528e31e44f500618
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503014"
---
# <span data-ttu-id="2868f-101">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2868f-101">Get-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="2868f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2868f-102">SYNOPSIS</span></span>
<span data-ttu-id="2868f-103">Ruft einen Container Registrierungs webhook ab.</span><span class="sxs-lookup"><span data-stu-id="2868f-103">Gets a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2868f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2868f-104">SYNTAX</span></span>

### <span data-ttu-id="2868f-105">ListWebhookByNameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2868f-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2868f-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="2868f-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2868f-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2868f-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2868f-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2868f-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2868f-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2868f-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2868f-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2868f-110">DESCRIPTION</span></span>
<span data-ttu-id="2868f-111">Das Get-AzureRmContainerRegistryWebhook-Cmdlet ruft einen angegebenen webhook der Container Registrierung oder alle webhooks einer Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="2868f-111">The Get-AzureRmContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="2868f-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2868f-112">EXAMPLES</span></span>

### <span data-ttu-id="2868f-113">Beispiel 1: Abrufen eines angegebenen webhooks einer Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="2868f-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="2868f-114">Abrufen eines angegebenen webhooks einer Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="2868f-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="2868f-115">Beispiel 2: Abrufen aller webhooks einer Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="2868f-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="2868f-116">Abrufen aller webhooks einer Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="2868f-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="2868f-117">Beispiel 3: Abrufen eines angegebenen webhooks einer Container Registrierung mit Konfigurationsdetails</span><span class="sxs-lookup"><span data-stu-id="2868f-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="2868f-118">Abrufen eines angegebenen webhooks einer Container Registrierung mit Konfigurationsdetails</span><span class="sxs-lookup"><span data-stu-id="2868f-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="2868f-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="2868f-119">PARAMETERS</span></span>

### <span data-ttu-id="2868f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2868f-120">-DefaultProfile</span></span>
<span data-ttu-id="2868f-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2868f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2868f-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2868f-122">-IncludeConfiguration</span></span>
<span data-ttu-id="2868f-123">Rufen Sie die Konfigurationsinformationen für einen webhook ab.</span><span class="sxs-lookup"><span data-stu-id="2868f-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="2868f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2868f-124">-Name</span></span>
<span data-ttu-id="2868f-125">Webhook-Name.</span><span class="sxs-lookup"><span data-stu-id="2868f-125">Webhook Name.</span></span>

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

### <span data-ttu-id="2868f-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="2868f-126">-Registry</span></span>
<span data-ttu-id="2868f-127">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="2868f-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="2868f-128">-Registryname</span><span class="sxs-lookup"><span data-stu-id="2868f-128">-RegistryName</span></span>
<span data-ttu-id="2868f-129">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="2868f-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="2868f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2868f-130">-ResourceGroupName</span></span>
<span data-ttu-id="2868f-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2868f-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="2868f-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2868f-132">-ResourceId</span></span>
<span data-ttu-id="2868f-133">Die Ressourcen-ID des Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="2868f-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="2868f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2868f-134">CommonParameters</span></span>
<span data-ttu-id="2868f-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2868f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2868f-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2868f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2868f-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2868f-137">INPUTS</span></span>

### <span data-ttu-id="2868f-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2868f-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="2868f-139">Parameter: Registrierung (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2868f-139">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="2868f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2868f-140">System.String</span></span>

## <span data-ttu-id="2868f-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2868f-141">OUTPUTS</span></span>

### <span data-ttu-id="2868f-142">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2868f-142">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="2868f-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="2868f-143">NOTES</span></span>

## <span data-ttu-id="2868f-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2868f-144">RELATED LINKS</span></span>

[<span data-ttu-id="2868f-145">Neu – AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2868f-145">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="2868f-146">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2868f-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="2868f-147">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2868f-147">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="2868f-148">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2868f-148">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
