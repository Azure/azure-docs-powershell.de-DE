---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 197d18f5d7585f6ae7e865b1c2b0449d032b4238
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380174"
---
# <span data-ttu-id="b7d67-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="b7d67-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="b7d67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7d67-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d67-103">Ruft eine ExpressRoutePort-Linkkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="b7d67-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="b7d67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7d67-104">SYNTAX</span></span>

### <span data-ttu-id="b7d67-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b7d67-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7d67-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7d67-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7d67-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7d67-107">DESCRIPTION</span></span>
<span data-ttu-id="b7d67-108">Das **Cmdlet "Get-AzExpressRoutePortLinkConfig"** ruft die Konfiguration eines Links eines ExpressRoutePort ab.</span><span class="sxs-lookup"><span data-stu-id="b7d67-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="b7d67-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b7d67-109">EXAMPLES</span></span>

### <span data-ttu-id="b7d67-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b7d67-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="b7d67-111">Ruft die Link1-Konfiguration von ExpressRoutePort-$erport</span><span class="sxs-lookup"><span data-stu-id="b7d67-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="b7d67-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b7d67-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="b7d67-113">Ruft die Konfiguration der Verknüpfung mit "ResourceId"-$id in ExpressRoutePort-$erport</span><span class="sxs-lookup"><span data-stu-id="b7d67-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="b7d67-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7d67-114">PARAMETERS</span></span>

### <span data-ttu-id="b7d67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d67-115">-DefaultProfile</span></span>
<span data-ttu-id="b7d67-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7d67-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7d67-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b7d67-117">-ExpressRoutePort</span></span>
<span data-ttu-id="b7d67-118">Der Verweis auf die ExpressRoutePort-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b7d67-118">The reference of the ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d67-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b7d67-119">-Name</span></span>
<span data-ttu-id="b7d67-120">Der Name des Links.</span><span class="sxs-lookup"><span data-stu-id="b7d67-120">Name of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7d67-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7d67-121">-ResourceId</span></span>
<span data-ttu-id="b7d67-122">ResourceId des Links.</span><span class="sxs-lookup"><span data-stu-id="b7d67-122">ResourceId of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d67-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d67-123">CommonParameters</span></span>
<span data-ttu-id="b7d67-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7d67-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7d67-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7d67-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d67-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b7d67-126">INPUTS</span></span>

### <span data-ttu-id="b7d67-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b7d67-127">System.String</span></span>

### <span data-ttu-id="b7d67-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b7d67-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="b7d67-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b7d67-129">OUTPUTS</span></span>

### <span data-ttu-id="b7d67-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="b7d67-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="b7d67-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b7d67-131">NOTES</span></span>

## <span data-ttu-id="b7d67-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b7d67-132">RELATED LINKS</span></span>
