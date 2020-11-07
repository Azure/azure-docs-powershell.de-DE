---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: 588402480cbd626a747208705ec59fd10c572075
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823836"
---
# <span data-ttu-id="63aca-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="63aca-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="63aca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63aca-102">SYNOPSIS</span></span>
<span data-ttu-id="63aca-103">Aktualisiert einen privaten Endpunkt Verbindungsstatus für den privaten Link Dienst.</span><span class="sxs-lookup"><span data-stu-id="63aca-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="63aca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63aca-104">SYNTAX</span></span>

```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63aca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63aca-105">DESCRIPTION</span></span>
<span data-ttu-id="63aca-106">Das Cmdlet " **Satz-AzPrivateEndpointConnection** " aktualisiert einen privaten Endpunkt Verbindungsstatus für einen privaten Link Dienst</span><span class="sxs-lookup"><span data-stu-id="63aca-106">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="63aca-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63aca-107">EXAMPLES</span></span>

### <span data-ttu-id="63aca-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="63aca-108">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="63aca-109">In diesem Beispiel wird ein privater Endpunkt Verbindungsstatus auf genehmigt aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="63aca-109">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="63aca-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="63aca-110">PARAMETERS</span></span>

### <span data-ttu-id="63aca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63aca-111">-DefaultProfile</span></span>
<span data-ttu-id="63aca-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="63aca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63aca-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63aca-113">-Description</span></span>
<span data-ttu-id="63aca-114">Der Grund für die Aktion.</span><span class="sxs-lookup"><span data-stu-id="63aca-114">The reason of action.</span></span>

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

### <span data-ttu-id="63aca-115">-Name</span><span class="sxs-lookup"><span data-stu-id="63aca-115">-Name</span></span>
<span data-ttu-id="63aca-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="63aca-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63aca-117">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="63aca-117">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="63aca-118">Die Ressource wurde genehmigt oder abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="63aca-118">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="63aca-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63aca-119">-ResourceGroupName</span></span>
<span data-ttu-id="63aca-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="63aca-120">The resource group name.</span></span>

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

### <span data-ttu-id="63aca-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="63aca-121">-ServiceName</span></span>
<span data-ttu-id="63aca-122">Der Name des privaten Link Diensts.</span><span class="sxs-lookup"><span data-stu-id="63aca-122">The private link service name.</span></span>

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

### <span data-ttu-id="63aca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63aca-123">CommonParameters</span></span>
<span data-ttu-id="63aca-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63aca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63aca-125">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63aca-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63aca-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63aca-126">INPUTS</span></span>

### <span data-ttu-id="63aca-127">System. String</span><span class="sxs-lookup"><span data-stu-id="63aca-127">System.String</span></span>

## <span data-ttu-id="63aca-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63aca-128">OUTPUTS</span></span>

### <span data-ttu-id="63aca-129">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="63aca-129">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="63aca-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="63aca-130">NOTES</span></span>

## <span data-ttu-id="63aca-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63aca-131">RELATED LINKS</span></span>
