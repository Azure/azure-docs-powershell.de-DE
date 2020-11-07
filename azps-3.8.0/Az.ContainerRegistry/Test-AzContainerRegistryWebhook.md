---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1245c92e13af691b0b439d6745a35a917bdf4d89
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845655"
---
# <span data-ttu-id="b0c23-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b0c23-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="b0c23-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0c23-102">SYNOPSIS</span></span>
<span data-ttu-id="b0c23-103">Löst ein webhook-Ping-Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="b0c23-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="b0c23-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0c23-104">SYNTAX</span></span>

### <span data-ttu-id="b0c23-105">ResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b0c23-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0c23-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c23-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0c23-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c23-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0c23-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0c23-108">DESCRIPTION</span></span>
<span data-ttu-id="b0c23-109">Das Test-AzContainerRegistryWebhook-Cmdlet löst ein webhook-Ping-Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="b0c23-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="b0c23-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0c23-110">EXAMPLES</span></span>

### <span data-ttu-id="b0c23-111">Beispiel 1: löst ein webhook-Ping-Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="b0c23-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="b0c23-112">Löst ein webhook-Ping-Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="b0c23-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="b0c23-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0c23-113">PARAMETERS</span></span>

### <span data-ttu-id="b0c23-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0c23-114">-DefaultProfile</span></span>
<span data-ttu-id="b0c23-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b0c23-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0c23-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b0c23-116">-Name</span></span>
<span data-ttu-id="b0c23-117">Webhook-Name.</span><span class="sxs-lookup"><span data-stu-id="b0c23-117">Webhook Name.</span></span>

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

### <span data-ttu-id="b0c23-118">-Registryname</span><span class="sxs-lookup"><span data-stu-id="b0c23-118">-RegistryName</span></span>
<span data-ttu-id="b0c23-119">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="b0c23-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="b0c23-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0c23-120">-ResourceGroupName</span></span>
<span data-ttu-id="b0c23-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b0c23-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="b0c23-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b0c23-122">-ResourceId</span></span>
<span data-ttu-id="b0c23-123">Die Ressourcen-ID des Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="b0c23-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="b0c23-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="b0c23-124">-Webhook</span></span>
<span data-ttu-id="b0c23-125">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="b0c23-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="b0c23-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0c23-126">CommonParameters</span></span>
<span data-ttu-id="b0c23-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0c23-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0c23-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0c23-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0c23-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0c23-129">INPUTS</span></span>

### <span data-ttu-id="b0c23-130">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b0c23-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="b0c23-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b0c23-131">System.String</span></span>

## <span data-ttu-id="b0c23-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0c23-132">OUTPUTS</span></span>

### <span data-ttu-id="b0c23-133">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="b0c23-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="b0c23-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0c23-134">NOTES</span></span>

## <span data-ttu-id="b0c23-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0c23-135">RELATED LINKS</span></span>

[<span data-ttu-id="b0c23-136">Neu – AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b0c23-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b0c23-137">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b0c23-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b0c23-138">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b0c23-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b0c23-139">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b0c23-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)