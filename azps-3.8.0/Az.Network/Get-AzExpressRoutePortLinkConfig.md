---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 197d18f5d7585f6ae7e865b1c2b0449d032b4238
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003561"
---
# <span data-ttu-id="a5262-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="a5262-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="a5262-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5262-102">SYNOPSIS</span></span>
<span data-ttu-id="a5262-103">Ruft eine ExpressRoutePort-Verknüpfungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="a5262-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="a5262-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5262-104">SYNTAX</span></span>

### <span data-ttu-id="a5262-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5262-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5262-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5262-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5262-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5262-107">DESCRIPTION</span></span>
<span data-ttu-id="a5262-108">Das Cmdlet " **Get-AzExpressRoutePortLinkConfig** " Ruft die Konfiguration eines Links eines ExpressRoutePort ab.</span><span class="sxs-lookup"><span data-stu-id="a5262-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="a5262-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5262-109">EXAMPLES</span></span>

### <span data-ttu-id="a5262-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5262-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="a5262-111">Ruft die Link1-Konfiguration von ExpressRoutePort $ERPort</span><span class="sxs-lookup"><span data-stu-id="a5262-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="a5262-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a5262-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="a5262-113">Ruft die Konfiguration der Verknüpfung mit der $ID in ExpressRoutePort $ERPort</span><span class="sxs-lookup"><span data-stu-id="a5262-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="a5262-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5262-114">PARAMETERS</span></span>

### <span data-ttu-id="a5262-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5262-115">-DefaultProfile</span></span>
<span data-ttu-id="a5262-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5262-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5262-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a5262-117">-ExpressRoutePort</span></span>
<span data-ttu-id="a5262-118">Der Verweis der ExpressRoutePort-Ressource.</span><span class="sxs-lookup"><span data-stu-id="a5262-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="a5262-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a5262-119">-Name</span></span>
<span data-ttu-id="a5262-120">Name des Links.</span><span class="sxs-lookup"><span data-stu-id="a5262-120">Name of the link.</span></span>

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

### <span data-ttu-id="a5262-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a5262-121">-ResourceId</span></span>
<span data-ttu-id="a5262-122">Die Quelle des Links.</span><span class="sxs-lookup"><span data-stu-id="a5262-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="a5262-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5262-123">CommonParameters</span></span>
<span data-ttu-id="a5262-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5262-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5262-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5262-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5262-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5262-126">INPUTS</span></span>

### <span data-ttu-id="a5262-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a5262-127">System.String</span></span>

### <span data-ttu-id="a5262-128">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a5262-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="a5262-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5262-129">OUTPUTS</span></span>

### <span data-ttu-id="a5262-130">Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="a5262-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="a5262-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5262-131">NOTES</span></span>

## <span data-ttu-id="a5262-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5262-132">RELATED LINKS</span></span>
