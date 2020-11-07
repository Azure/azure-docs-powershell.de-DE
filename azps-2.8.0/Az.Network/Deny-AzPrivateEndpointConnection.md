---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 4a67914fd3709ef972adac8eba6b1b2fa211fbf6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821956"
---
# <span data-ttu-id="d050a-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d050a-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="d050a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d050a-102">SYNOPSIS</span></span>
<span data-ttu-id="d050a-103">verweigert eine private Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="d050a-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="d050a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d050a-104">SYNTAX</span></span>

### <span data-ttu-id="d050a-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="d050a-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d050a-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="d050a-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d050a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d050a-107">DESCRIPTION</span></span>
<span data-ttu-id="d050a-108">Das Cmdlet **Deny-AzPrivateEndpointConnection** verweigert eine private Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="d050a-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="d050a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d050a-109">EXAMPLES</span></span>

### <span data-ttu-id="d050a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d050a-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="d050a-111">In diesem Beispiel wird eine private Endpunkt Verbindung verweigert.</span><span class="sxs-lookup"><span data-stu-id="d050a-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="d050a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d050a-112">PARAMETERS</span></span>

### <span data-ttu-id="d050a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d050a-113">-DefaultProfile</span></span>
<span data-ttu-id="d050a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d050a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d050a-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d050a-115">-Description</span></span>
<span data-ttu-id="d050a-116">Der Grund für die Aktion.</span><span class="sxs-lookup"><span data-stu-id="d050a-116">The reason of action.</span></span>

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

### <span data-ttu-id="d050a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d050a-117">-Name</span></span>
<span data-ttu-id="d050a-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="d050a-118">The resource name.</span></span>

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

### <span data-ttu-id="d050a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d050a-119">-ResourceGroupName</span></span>
<span data-ttu-id="d050a-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d050a-120">The resource group name.</span></span>

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

### <span data-ttu-id="d050a-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d050a-121">-ResourceId</span></span>
<span data-ttu-id="d050a-122">Die Azure Resource Manager-ID der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="d050a-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="d050a-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d050a-123">-ServiceName</span></span>
<span data-ttu-id="d050a-124">Der Name des privaten Link Diensts.</span><span class="sxs-lookup"><span data-stu-id="d050a-124">The private link service name.</span></span>

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

### <span data-ttu-id="d050a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d050a-125">CommonParameters</span></span>
<span data-ttu-id="d050a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d050a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d050a-127">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d050a-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d050a-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d050a-128">INPUTS</span></span>

### <span data-ttu-id="d050a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d050a-129">System.String</span></span>

## <span data-ttu-id="d050a-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d050a-130">OUTPUTS</span></span>

### <span data-ttu-id="d050a-131">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d050a-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="d050a-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d050a-132">NOTES</span></span>

## <span data-ttu-id="d050a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d050a-133">RELATED LINKS</span></span>

[<span data-ttu-id="d050a-134">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d050a-134">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="d050a-135">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d050a-135">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="d050a-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d050a-136">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)