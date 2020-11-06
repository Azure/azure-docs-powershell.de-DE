---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 4f20f177b172ab9b5372de6b95d821202e991000
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481297"
---
# <span data-ttu-id="0a991-101">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0a991-101">Get-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="0a991-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a991-102">SYNOPSIS</span></span>
<span data-ttu-id="0a991-103">Ruft einen Container Registrierungs webhook ab.</span><span class="sxs-lookup"><span data-stu-id="0a991-103">Gets a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a991-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a991-104">SYNTAX</span></span>

### <span data-ttu-id="0a991-105">ListWebhookByNameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0a991-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a991-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a991-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a991-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a991-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a991-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a991-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a991-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a991-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a991-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a991-110">DESCRIPTION</span></span>
<span data-ttu-id="0a991-111">Das Get-AzureRmContainerRegistryWebhook-Cmdlet ruft einen angegebenen webhook der Container Registrierung oder alle webhooks einer Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="0a991-111">The Get-AzureRmContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="0a991-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a991-112">EXAMPLES</span></span>

### <span data-ttu-id="0a991-113">Beispiel 1: Abrufen eines angegebenen webhooks einer Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="0a991-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="0a991-114">Abrufen eines angegebenen webhooks einer Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="0a991-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="0a991-115">Beispiel 2: Abrufen aller webhooks einer Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="0a991-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="0a991-116">Abrufen aller webhooks einer Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="0a991-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="0a991-117">Beispiel 3: Abrufen eines angegebenen webhooks einer Container Registrierung mit Konfigurationsdetails</span><span class="sxs-lookup"><span data-stu-id="0a991-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="0a991-118">Abrufen eines angegebenen webhooks einer Container Registrierung mit Konfigurationsdetails</span><span class="sxs-lookup"><span data-stu-id="0a991-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="0a991-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a991-119">PARAMETERS</span></span>

### <span data-ttu-id="0a991-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a991-120">-DefaultProfile</span></span>
<span data-ttu-id="0a991-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a991-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a991-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a991-122">-IncludeConfiguration</span></span>
<span data-ttu-id="0a991-123">Rufen Sie die Konfigurationsinformationen für einen webhook ab.</span><span class="sxs-lookup"><span data-stu-id="0a991-123">Get the configuration information for a webhook.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a991-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0a991-124">-Name</span></span>
<span data-ttu-id="0a991-125">Webhook-Name.</span><span class="sxs-lookup"><span data-stu-id="0a991-125">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a991-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="0a991-126">-Registry</span></span>
<span data-ttu-id="0a991-127">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0a991-127">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a991-128">-Registryname</span><span class="sxs-lookup"><span data-stu-id="0a991-128">-RegistryName</span></span>
<span data-ttu-id="0a991-129">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="0a991-129">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a991-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a991-130">-ResourceGroupName</span></span>
<span data-ttu-id="0a991-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0a991-131">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a991-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0a991-132">-ResourceId</span></span>
<span data-ttu-id="0a991-133">Die Ressourcen-ID des Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="0a991-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="0a991-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a991-134">CommonParameters</span></span>
<span data-ttu-id="0a991-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a991-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a991-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a991-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a991-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a991-137">INPUTS</span></span>

### <span data-ttu-id="0a991-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0a991-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="0a991-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0a991-139">System.String</span></span>

## <span data-ttu-id="0a991-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a991-140">OUTPUTS</span></span>

### <span data-ttu-id="0a991-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0a991-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="0a991-142">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook, Microsoft. Azure. Commands. ContainerRegistry, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0a991-142">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook, Microsoft.Azure.Commands.ContainerRegistry, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0a991-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a991-143">NOTES</span></span>

## <span data-ttu-id="0a991-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a991-144">RELATED LINKS</span></span>

[<span data-ttu-id="0a991-145">Neu – AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0a991-145">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="0a991-146">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0a991-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="0a991-147">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0a991-147">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="0a991-148">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0a991-148">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
