---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 02d16be7c41a95c32d4aa7b6f3231b68c0ba7244
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497654"
---
# <span data-ttu-id="d9b93-101">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d9b93-101">Test-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="d9b93-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9b93-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b93-103">Löst ein webhook-Ping-Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="d9b93-103">Triggers a webhook ping event.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9b93-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9b93-104">SYNTAX</span></span>

### <span data-ttu-id="d9b93-105">ResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9b93-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzureRmContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d9b93-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9b93-106">NameResourceGroupParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9b93-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9b93-107">WebhookObjectParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9b93-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9b93-108">DESCRIPTION</span></span>
<span data-ttu-id="d9b93-109">Das Test-AzureRmContainerRegistryWebhook-Cmdlet löst ein webhook-Ping-Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="d9b93-109">The Test-AzureRmContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="d9b93-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9b93-110">EXAMPLES</span></span>

### <span data-ttu-id="d9b93-111">Beispiel 1: löst ein webhook-Ping-Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="d9b93-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="d9b93-112">Löst ein webhook-Ping-Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="d9b93-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="d9b93-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9b93-113">PARAMETERS</span></span>

### <span data-ttu-id="d9b93-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b93-114">-DefaultProfile</span></span>
<span data-ttu-id="d9b93-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9b93-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9b93-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d9b93-116">-Name</span></span>
<span data-ttu-id="d9b93-117">Webhook-Name.</span><span class="sxs-lookup"><span data-stu-id="d9b93-117">Webhook Name.</span></span>

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

### <span data-ttu-id="d9b93-118">-Registryname</span><span class="sxs-lookup"><span data-stu-id="d9b93-118">-RegistryName</span></span>
<span data-ttu-id="d9b93-119">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="d9b93-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="d9b93-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9b93-120">-ResourceGroupName</span></span>
<span data-ttu-id="d9b93-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d9b93-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="d9b93-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d9b93-122">-ResourceId</span></span>
<span data-ttu-id="d9b93-123">Die Ressourcen-ID des Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="d9b93-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="d9b93-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="d9b93-124">-Webhook</span></span>
<span data-ttu-id="d9b93-125">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="d9b93-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="d9b93-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b93-126">CommonParameters</span></span>
<span data-ttu-id="d9b93-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9b93-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b93-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9b93-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b93-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9b93-129">INPUTS</span></span>

### <span data-ttu-id="d9b93-130">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d9b93-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="d9b93-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d9b93-131">System.String</span></span>

## <span data-ttu-id="d9b93-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9b93-132">OUTPUTS</span></span>

### <span data-ttu-id="d9b93-133">Microsoft. Azure. Management. ContainerRegistry. Models. EventInfo</span><span class="sxs-lookup"><span data-stu-id="d9b93-133">Microsoft.Azure.Management.ContainerRegistry.Models.EventInfo</span></span>

## <span data-ttu-id="d9b93-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9b93-134">NOTES</span></span>

## <span data-ttu-id="d9b93-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9b93-135">RELATED LINKS</span></span>

[<span data-ttu-id="d9b93-136">Neu – AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d9b93-136">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="d9b93-137">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d9b93-137">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="d9b93-138">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d9b93-138">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="d9b93-139">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d9b93-139">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
