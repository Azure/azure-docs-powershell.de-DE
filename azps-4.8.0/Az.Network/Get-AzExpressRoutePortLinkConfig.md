---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 197d18f5d7585f6ae7e865b1c2b0449d032b4238
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174366"
---
# <span data-ttu-id="cf402-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="cf402-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="cf402-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf402-102">SYNOPSIS</span></span>
<span data-ttu-id="cf402-103">Ruft eine ExpressRoutePort-Verknüpfungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="cf402-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="cf402-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf402-104">SYNTAX</span></span>

### <span data-ttu-id="cf402-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cf402-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf402-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf402-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf402-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf402-107">DESCRIPTION</span></span>
<span data-ttu-id="cf402-108">Das Cmdlet " **Get-AzExpressRoutePortLinkConfig** " Ruft die Konfiguration eines Links eines ExpressRoutePort ab.</span><span class="sxs-lookup"><span data-stu-id="cf402-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="cf402-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf402-109">EXAMPLES</span></span>

### <span data-ttu-id="cf402-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cf402-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="cf402-111">Ruft die Link1-Konfiguration von ExpressRoutePort $ERPort</span><span class="sxs-lookup"><span data-stu-id="cf402-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="cf402-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cf402-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="cf402-113">Ruft die Konfiguration der Verknüpfung mit der $ID in ExpressRoutePort $ERPort</span><span class="sxs-lookup"><span data-stu-id="cf402-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="cf402-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf402-114">PARAMETERS</span></span>

### <span data-ttu-id="cf402-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf402-115">-DefaultProfile</span></span>
<span data-ttu-id="cf402-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf402-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf402-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cf402-117">-ExpressRoutePort</span></span>
<span data-ttu-id="cf402-118">Der Verweis der ExpressRoutePort-Ressource.</span><span class="sxs-lookup"><span data-stu-id="cf402-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="cf402-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cf402-119">-Name</span></span>
<span data-ttu-id="cf402-120">Name des Links.</span><span class="sxs-lookup"><span data-stu-id="cf402-120">Name of the link.</span></span>

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

### <span data-ttu-id="cf402-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cf402-121">-ResourceId</span></span>
<span data-ttu-id="cf402-122">Die Quelle des Links.</span><span class="sxs-lookup"><span data-stu-id="cf402-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="cf402-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf402-123">CommonParameters</span></span>
<span data-ttu-id="cf402-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf402-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf402-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf402-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf402-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf402-126">INPUTS</span></span>

### <span data-ttu-id="cf402-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cf402-127">System.String</span></span>

### <span data-ttu-id="cf402-128">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cf402-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="cf402-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf402-129">OUTPUTS</span></span>

### <span data-ttu-id="cf402-130">Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="cf402-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="cf402-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf402-131">NOTES</span></span>

## <span data-ttu-id="cf402-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf402-132">RELATED LINKS</span></span>
