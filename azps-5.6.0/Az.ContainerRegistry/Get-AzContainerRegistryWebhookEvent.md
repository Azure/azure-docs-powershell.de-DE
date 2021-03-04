---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrywebhookevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhookEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhookEvent.md
ms.openlocfilehash: 1a47a965b32cdeab04e9cf48a5ad544e82b52d55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922048"
---
# <span data-ttu-id="30645-101">Get-AzContainerRegistryWebhookEvent</span><span class="sxs-lookup"><span data-stu-id="30645-101">Get-AzContainerRegistryWebhookEvent</span></span>

## <span data-ttu-id="30645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30645-102">SYNOPSIS</span></span>
<span data-ttu-id="30645-103">Ruft Ereignisse eines Containerregistrierungswebhooks ab.</span><span class="sxs-lookup"><span data-stu-id="30645-103">Gets events of a container registry webhook.</span></span>

## <span data-ttu-id="30645-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30645-104">SYNTAX</span></span>

### <span data-ttu-id="30645-105">ListWebhookEventsByNameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="30645-105">ListWebhookEventsByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhookEvent [-WebhookName] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30645-106">ListWebhookEventsByWebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30645-106">ListWebhookEventsByWebhookObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhookEvent -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30645-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30645-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhookEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30645-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30645-108">DESCRIPTION</span></span>
<span data-ttu-id="30645-109">Im Get-AzContainerRegistryWebhookEvent cmdlet werden alle Ereignisse eines Webhooks aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="30645-109">The Get-AzContainerRegistryWebhookEvent cmdlet lists all the events of a webhook.</span></span>

## <span data-ttu-id="30645-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="30645-110">EXAMPLES</span></span>

### <span data-ttu-id="30645-111">Beispiel 1: Ruft alle Ereignisse eines Webhooks ab.</span><span class="sxs-lookup"><span data-stu-id="30645-111">Example 1: Gets all the events of a webhook.</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhookEvent -ResourceGroupName mattacrtest001 -RegistryName premium001 -Name webhook001

   Webhook service Uri: http://www.bing.com/

ID                                       Action   Timestamp                      Response
                                                                                 StatusCode
--                                       ------   ---------                      ----------
3c6281b6-47cd-4129-948b-4036780236f0     ping     11/17/2017 5:10:09 PM          200
70f1d41d-15fe-4251-87b6-43c32a91eae7     ping     11/17/2017 6:56:23 AM          200
5d25556b-32d0-4377-8031-d8ba7a263d6a     ping     11/17/2017 6:27:41 AM          200
c1e7d8aa-9f1b-447c-9583-2a58b7f81026     ping     11/17/2017 12:09:41 AM         200
eb4aa503-0d14-4f25-8ae5-33cce9a8fd50     ping     11/16/2017 11:35:03 PM         200
85a93d7f-3923-4ec5-bb8e-9ded5b6549c1     ping     11/17/2017 5:10:09 PM          200
9e3c8b5f-e0ee-47cf-9727-df1c8d45a497     ping     11/17/2017 6:56:23 AM          200
2d0ce294-9b59-4f5c-953a-47f2b270526f     ping     11/17/2017 6:27:41 AM          200
```

<span data-ttu-id="30645-112">Ruft alle Ereignisse eines Webhooks ab.</span><span class="sxs-lookup"><span data-stu-id="30645-112">Gets all the events of a webhook.</span></span>

## <span data-ttu-id="30645-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="30645-113">PARAMETERS</span></span>

### <span data-ttu-id="30645-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30645-114">-DefaultProfile</span></span>
<span data-ttu-id="30645-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="30645-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30645-116">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="30645-116">-RegistryName</span></span>
<span data-ttu-id="30645-117">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="30645-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30645-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30645-118">-ResourceGroupName</span></span>
<span data-ttu-id="30645-119">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="30645-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30645-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30645-120">-ResourceId</span></span>
<span data-ttu-id="30645-121">Die Containerregistrierungs-Webhook-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="30645-121">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="30645-122">-Webhook</span><span class="sxs-lookup"><span data-stu-id="30645-122">-Webhook</span></span>
<span data-ttu-id="30645-123">Containerregistrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="30645-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: ListWebhookEventsByWebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30645-124">-WebhookName</span><span class="sxs-lookup"><span data-stu-id="30645-124">-WebhookName</span></span>
<span data-ttu-id="30645-125">Webhookname.</span><span class="sxs-lookup"><span data-stu-id="30645-125">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30645-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30645-126">CommonParameters</span></span>
<span data-ttu-id="30645-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30645-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30645-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30645-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30645-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="30645-129">INPUTS</span></span>

### <span data-ttu-id="30645-130">System.String</span><span class="sxs-lookup"><span data-stu-id="30645-130">System.String</span></span>

## <span data-ttu-id="30645-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="30645-131">OUTPUTS</span></span>

### <span data-ttu-id="30645-132">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhookEvent</span><span class="sxs-lookup"><span data-stu-id="30645-132">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhookEvent</span></span>

## <span data-ttu-id="30645-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="30645-133">NOTES</span></span>

## <span data-ttu-id="30645-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="30645-134">RELATED LINKS</span></span>

[<span data-ttu-id="30645-135">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="30645-135">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="30645-136">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="30645-136">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="30645-137">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="30645-137">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="30645-138">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="30645-138">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="30645-139">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="30645-139">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

