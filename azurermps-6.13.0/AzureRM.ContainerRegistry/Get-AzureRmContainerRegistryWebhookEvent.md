---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhookEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhookEvent.md
ms.openlocfilehash: 5e14d1e3f146281ec800914474c5caf3ca3cd47e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476162"
---
# <span data-ttu-id="0e144-101">Get-AzureRmContainerRegistryWebhookEvent</span><span class="sxs-lookup"><span data-stu-id="0e144-101">Get-AzureRmContainerRegistryWebhookEvent</span></span>

## <span data-ttu-id="0e144-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e144-102">SYNOPSIS</span></span>
<span data-ttu-id="0e144-103">Ruft Ereignisse eines Container Registrierungs webhooks ab.</span><span class="sxs-lookup"><span data-stu-id="0e144-103">Gets events of a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e144-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e144-104">SYNTAX</span></span>

### <span data-ttu-id="0e144-105">ListWebhookEventsByNameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0e144-105">ListWebhookEventsByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhookEvent [-WebhookName] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e144-106">ListWebhookEventsByWebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e144-106">ListWebhookEventsByWebhookObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhookEvent -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e144-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e144-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhookEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e144-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e144-108">DESCRIPTION</span></span>
<span data-ttu-id="0e144-109">Das Get-AzureRmContainerRegistryWebhookEvent-Cmdlet listet alle Ereignisse eines webhooks auf.</span><span class="sxs-lookup"><span data-stu-id="0e144-109">The Get-AzureRmContainerRegistryWebhookEvent cmdlet lists all the events of a webhook.</span></span>

## <span data-ttu-id="0e144-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e144-110">EXAMPLES</span></span>

### <span data-ttu-id="0e144-111">Beispiel 1: Ruft alle Ereignisse eines webhooks ab.</span><span class="sxs-lookup"><span data-stu-id="0e144-111">Example 1: Gets all the events of a webhook.</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhookEvent -ResourceGroupName mattacrtest001 -RegistryName premium001 -Name webhook001

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

<span data-ttu-id="0e144-112">Ruft alle Ereignisse eines webhooks ab.</span><span class="sxs-lookup"><span data-stu-id="0e144-112">Gets all the events of a webhook.</span></span>

## <span data-ttu-id="0e144-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e144-113">PARAMETERS</span></span>

### <span data-ttu-id="0e144-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e144-114">-DefaultProfile</span></span>
<span data-ttu-id="0e144-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e144-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e144-116">-Registryname</span><span class="sxs-lookup"><span data-stu-id="0e144-116">-RegistryName</span></span>
<span data-ttu-id="0e144-117">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="0e144-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="0e144-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e144-118">-ResourceGroupName</span></span>
<span data-ttu-id="0e144-119">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0e144-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="0e144-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0e144-120">-ResourceId</span></span>
<span data-ttu-id="0e144-121">Die Ressourcen-ID des Container Registrierungs webhooks</span><span class="sxs-lookup"><span data-stu-id="0e144-121">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="0e144-122">-Webhook</span><span class="sxs-lookup"><span data-stu-id="0e144-122">-Webhook</span></span>
<span data-ttu-id="0e144-123">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0e144-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="0e144-124">-Webhookname</span><span class="sxs-lookup"><span data-stu-id="0e144-124">-WebhookName</span></span>
<span data-ttu-id="0e144-125">Webhook-Name.</span><span class="sxs-lookup"><span data-stu-id="0e144-125">Webhook Name.</span></span>

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

### <span data-ttu-id="0e144-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e144-126">CommonParameters</span></span>
<span data-ttu-id="0e144-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e144-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e144-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e144-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e144-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e144-129">INPUTS</span></span>

### <span data-ttu-id="0e144-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0e144-130">System.String</span></span>

## <span data-ttu-id="0e144-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e144-131">OUTPUTS</span></span>

### <span data-ttu-id="0e144-132">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhookEvent</span><span class="sxs-lookup"><span data-stu-id="0e144-132">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhookEvent</span></span>

## <span data-ttu-id="0e144-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e144-133">NOTES</span></span>

## <span data-ttu-id="0e144-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e144-134">RELATED LINKS</span></span>

[<span data-ttu-id="0e144-135">Neu – AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0e144-135">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="0e144-136">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0e144-136">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="0e144-137">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0e144-137">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="0e144-138">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0e144-138">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="0e144-139">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0e144-139">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)

