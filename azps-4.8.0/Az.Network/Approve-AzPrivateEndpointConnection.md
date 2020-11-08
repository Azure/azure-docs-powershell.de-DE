---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174612"
---
# <span data-ttu-id="9761f-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9761f-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="9761f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9761f-102">SYNOPSIS</span></span>
<span data-ttu-id="9761f-103">Genehmigt eine private Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="9761f-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="9761f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9761f-104">SYNTAX</span></span>

### <span data-ttu-id="9761f-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="9761f-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9761f-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="9761f-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9761f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9761f-107">DESCRIPTION</span></span>
<span data-ttu-id="9761f-108">Das Cmdlet " **genehmigen-AzPrivateEndpointConnection** " genehmigt eine private Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="9761f-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="9761f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9761f-109">EXAMPLES</span></span>

### <span data-ttu-id="9761f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9761f-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="9761f-111">In diesem Beispiel wird eine private Endpunkt Verbindung genehmigt.</span><span class="sxs-lookup"><span data-stu-id="9761f-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="9761f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9761f-112">PARAMETERS</span></span>

### <span data-ttu-id="9761f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9761f-113">-DefaultProfile</span></span>
<span data-ttu-id="9761f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9761f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9761f-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9761f-115">-Description</span></span>
<span data-ttu-id="9761f-116">Der Grund für die Aktion.</span><span class="sxs-lookup"><span data-stu-id="9761f-116">The reason of action.</span></span>

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

### <span data-ttu-id="9761f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9761f-117">-Name</span></span>
<span data-ttu-id="9761f-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="9761f-118">The resource name.</span></span>

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

### <span data-ttu-id="9761f-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="9761f-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="9761f-120">Der Ressourcentyp "privater Link".</span><span class="sxs-lookup"><span data-stu-id="9761f-120">The private link resource type.</span></span>

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

### <span data-ttu-id="9761f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9761f-121">-ResourceGroupName</span></span>
<span data-ttu-id="9761f-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9761f-122">The resource group name.</span></span>

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

### <span data-ttu-id="9761f-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9761f-123">-ResourceId</span></span>
<span data-ttu-id="9761f-124">Die Azure Resource Manager-ID der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="9761f-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="9761f-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9761f-125">-ServiceName</span></span>
<span data-ttu-id="9761f-126">Der Name des privaten Link Diensts.</span><span class="sxs-lookup"><span data-stu-id="9761f-126">The private link service name.</span></span>

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


### <span data-ttu-id="9761f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9761f-127">CommonParameters</span></span>
<span data-ttu-id="9761f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9761f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9761f-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9761f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9761f-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9761f-130">INPUTS</span></span>

### <span data-ttu-id="9761f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9761f-131">System.String</span></span>

## <span data-ttu-id="9761f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9761f-132">OUTPUTS</span></span>

### <span data-ttu-id="9761f-133">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9761f-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="9761f-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="9761f-134">NOTES</span></span>

## <span data-ttu-id="9761f-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9761f-135">RELATED LINKS</span></span>

[<span data-ttu-id="9761f-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9761f-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9761f-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9761f-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9761f-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9761f-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9761f-139">Satz-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9761f-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)