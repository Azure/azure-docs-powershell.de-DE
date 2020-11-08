---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009029"
---
# <span data-ttu-id="2f613-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2f613-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="2f613-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f613-102">SYNOPSIS</span></span>
<span data-ttu-id="2f613-103">Aktualisiert einen privaten Endpunkt Verbindungsstatus für den privaten Link Dienst.</span><span class="sxs-lookup"><span data-stu-id="2f613-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="2f613-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f613-104">SYNTAX</span></span>

### <span data-ttu-id="2f613-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f613-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f613-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="2f613-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f613-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f613-107">DESCRIPTION</span></span>
<span data-ttu-id="2f613-108">Das Cmdlet " **Satz-AzPrivateEndpointConnection** " aktualisiert einen privaten Endpunkt Verbindungsstatus für einen privaten Link Dienst</span><span class="sxs-lookup"><span data-stu-id="2f613-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="2f613-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f613-109">EXAMPLES</span></span>

### <span data-ttu-id="2f613-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2f613-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="2f613-111">In diesem Beispiel wird ein privater Endpunkt Verbindungsstatus auf genehmigt aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2f613-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="2f613-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f613-112">PARAMETERS</span></span>

### <span data-ttu-id="2f613-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f613-113">-DefaultProfile</span></span>
<span data-ttu-id="2f613-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f613-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f613-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f613-115">-Description</span></span>
<span data-ttu-id="2f613-116">Der Grund für die Aktion.</span><span class="sxs-lookup"><span data-stu-id="2f613-116">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f613-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2f613-117">-Name</span></span>
<span data-ttu-id="2f613-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="2f613-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f613-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="2f613-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="2f613-120">Der Ressourcentyp "privater Link".</span><span class="sxs-lookup"><span data-stu-id="2f613-120">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f613-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="2f613-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="2f613-122">Die Ressource wurde genehmigt oder abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="2f613-122">Approved or rejected the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f613-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f613-123">-ResourceGroupName</span></span>
<span data-ttu-id="2f613-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2f613-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f613-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2f613-125">-ResourceId</span></span>
<span data-ttu-id="2f613-126">Die Azure Resource Manager-ID der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="2f613-126">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f613-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2f613-127">-ServiceName</span></span>
<span data-ttu-id="2f613-128">Der Name des privaten Link Diensts.</span><span class="sxs-lookup"><span data-stu-id="2f613-128">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f613-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f613-129">CommonParameters</span></span>
<span data-ttu-id="2f613-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f613-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f613-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f613-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f613-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f613-132">INPUTS</span></span>

### <span data-ttu-id="2f613-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2f613-133">System.String</span></span>

## <span data-ttu-id="2f613-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f613-134">OUTPUTS</span></span>

### <span data-ttu-id="2f613-135">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2f613-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="2f613-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f613-136">NOTES</span></span>

## <span data-ttu-id="2f613-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f613-137">RELATED LINKS</span></span>

[<span data-ttu-id="2f613-138">Genehmigen – AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2f613-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2f613-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2f613-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2f613-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2f613-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2f613-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2f613-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)