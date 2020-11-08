---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 159b320b24ff1e9ab1b4c71e6c374931ecfeffdd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178584"
---
# <span data-ttu-id="30a0e-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30a0e-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="30a0e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="30a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="30a0e-103">verweigert eine private Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="30a0e-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="30a0e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="30a0e-104">SYNTAX</span></span>

### <span data-ttu-id="30a0e-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="30a0e-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30a0e-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="30a0e-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30a0e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30a0e-107">DESCRIPTION</span></span>
<span data-ttu-id="30a0e-108">Das Cmdlet **Deny-AzPrivateEndpointConnection** verweigert eine private Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="30a0e-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="30a0e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30a0e-109">EXAMPLES</span></span>

### <span data-ttu-id="30a0e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="30a0e-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="30a0e-111">In diesem Beispiel wird eine private Endpunkt Verbindung verweigert.</span><span class="sxs-lookup"><span data-stu-id="30a0e-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="30a0e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="30a0e-112">PARAMETERS</span></span>

### <span data-ttu-id="30a0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a0e-113">-DefaultProfile</span></span>
<span data-ttu-id="30a0e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="30a0e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30a0e-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30a0e-115">-Description</span></span>
<span data-ttu-id="30a0e-116">Der Grund für die Aktion.</span><span class="sxs-lookup"><span data-stu-id="30a0e-116">The reason of action.</span></span>

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

### <span data-ttu-id="30a0e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="30a0e-117">-Name</span></span>
<span data-ttu-id="30a0e-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="30a0e-118">The resource name.</span></span>

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

### <span data-ttu-id="30a0e-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="30a0e-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="30a0e-120">Der Ressourcentyp "privater Link".</span><span class="sxs-lookup"><span data-stu-id="30a0e-120">The private link resource type.</span></span>

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

### <span data-ttu-id="30a0e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30a0e-121">-ResourceGroupName</span></span>
<span data-ttu-id="30a0e-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="30a0e-122">The resource group name.</span></span>

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

### <span data-ttu-id="30a0e-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="30a0e-123">-ResourceId</span></span>
<span data-ttu-id="30a0e-124">Die Azure Resource Manager-ID der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="30a0e-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="30a0e-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="30a0e-125">-ServiceName</span></span>
<span data-ttu-id="30a0e-126">Der Name des Diensts, zu dem eine private Endpunkt Verbindung gehört.</span><span class="sxs-lookup"><span data-stu-id="30a0e-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="30a0e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a0e-127">CommonParameters</span></span>
<span data-ttu-id="30a0e-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a0e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a0e-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30a0e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a0e-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="30a0e-130">INPUTS</span></span>

### <span data-ttu-id="30a0e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="30a0e-131">System.String</span></span>

## <span data-ttu-id="30a0e-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="30a0e-132">OUTPUTS</span></span>

### <span data-ttu-id="30a0e-133">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="30a0e-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="30a0e-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="30a0e-134">NOTES</span></span>

## <span data-ttu-id="30a0e-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="30a0e-135">RELATED LINKS</span></span>

[<span data-ttu-id="30a0e-136">Genehmigen – AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30a0e-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="30a0e-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30a0e-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="30a0e-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30a0e-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="30a0e-139">Satz-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30a0e-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)