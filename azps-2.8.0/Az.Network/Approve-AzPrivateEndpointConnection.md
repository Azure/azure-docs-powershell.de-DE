---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 9b47fb1954b13e28268f6b7aad66fa8190e20584
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821964"
---
# <span data-ttu-id="0c69f-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c69f-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="0c69f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c69f-102">SYNOPSIS</span></span>
<span data-ttu-id="0c69f-103">Genehmigt eine private Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="0c69f-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="0c69f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c69f-104">SYNTAX</span></span>

### <span data-ttu-id="0c69f-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="0c69f-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c69f-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="0c69f-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c69f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c69f-107">DESCRIPTION</span></span>
<span data-ttu-id="0c69f-108">Das Cmdlet " **genehmigen-AzPrivateEndpointConnection** " genehmigt eine private Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="0c69f-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="0c69f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c69f-109">EXAMPLES</span></span>

### <span data-ttu-id="0c69f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0c69f-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="0c69f-111">In diesem Beispiel wird eine private Endpunkt Verbindung genehmigt.</span><span class="sxs-lookup"><span data-stu-id="0c69f-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="0c69f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c69f-112">PARAMETERS</span></span>

### <span data-ttu-id="0c69f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c69f-113">-DefaultProfile</span></span>
<span data-ttu-id="0c69f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0c69f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c69f-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c69f-115">-Description</span></span>
<span data-ttu-id="0c69f-116">Der Grund für die Aktion.</span><span class="sxs-lookup"><span data-stu-id="0c69f-116">The reason of action.</span></span>

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

### <span data-ttu-id="0c69f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0c69f-117">-Name</span></span>
<span data-ttu-id="0c69f-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="0c69f-118">The resource name.</span></span>

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

### <span data-ttu-id="0c69f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c69f-119">-ResourceGroupName</span></span>
<span data-ttu-id="0c69f-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0c69f-120">The resource group name.</span></span>

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

### <span data-ttu-id="0c69f-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0c69f-121">-ResourceId</span></span>
<span data-ttu-id="0c69f-122">Die Azure Resource Manager-ID der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="0c69f-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="0c69f-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0c69f-123">-ServiceName</span></span>
<span data-ttu-id="0c69f-124">Der Name des privaten Link Diensts.</span><span class="sxs-lookup"><span data-stu-id="0c69f-124">The private link service name.</span></span>

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

### <span data-ttu-id="0c69f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c69f-125">CommonParameters</span></span>
<span data-ttu-id="0c69f-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c69f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c69f-127">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c69f-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c69f-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c69f-128">INPUTS</span></span>

### <span data-ttu-id="0c69f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0c69f-129">System.String</span></span>

## <span data-ttu-id="0c69f-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c69f-130">OUTPUTS</span></span>

### <span data-ttu-id="0c69f-131">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0c69f-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="0c69f-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c69f-132">NOTES</span></span>

## <span data-ttu-id="0c69f-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c69f-133">RELATED LINKS</span></span>

[<span data-ttu-id="0c69f-134">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c69f-134">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0c69f-135">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c69f-135">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0c69f-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c69f-136">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)