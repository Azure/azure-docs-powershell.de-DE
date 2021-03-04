---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: 2cf661ab2bcc531c0a88ae86934a53b212bb91d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919504"
---
# <span data-ttu-id="720ed-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="720ed-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="720ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="720ed-102">SYNOPSIS</span></span>
<span data-ttu-id="720ed-103">Erstellt ein StaticRoute-Objekt, das dann einem RoutingConfiguration-Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="720ed-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="720ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="720ed-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="720ed-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="720ed-105">DESCRIPTION</span></span>
<span data-ttu-id="720ed-106">Erstellt ein StaticRoute-Objekt.</span><span class="sxs-lookup"><span data-stu-id="720ed-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="720ed-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="720ed-107">EXAMPLES</span></span>

### <span data-ttu-id="720ed-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="720ed-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="720ed-109">Mit dem obigen Befehl wird ein StaticRoute-Objekt erstellt, das dann einem RoutingConfiguration-Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="720ed-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="720ed-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="720ed-110">PARAMETERS</span></span>

### <span data-ttu-id="720ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="720ed-111">-DefaultProfile</span></span>
<span data-ttu-id="720ed-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="720ed-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720ed-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="720ed-113">-AddressPrefix</span></span>
<span data-ttu-id="720ed-114">Liste der Adresspräfixe.</span><span class="sxs-lookup"><span data-stu-id="720ed-114">List of address prefixes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720ed-115">-Name</span><span class="sxs-lookup"><span data-stu-id="720ed-115">-Name</span></span>
<span data-ttu-id="720ed-116">Der Routenname.</span><span class="sxs-lookup"><span data-stu-id="720ed-116">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720ed-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="720ed-117">-NextHopIpAddress</span></span>
<span data-ttu-id="720ed-118">Die nächste Hop-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="720ed-118">The next hop ip address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720ed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="720ed-119">CommonParameters</span></span>
<span data-ttu-id="720ed-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="720ed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="720ed-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="720ed-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="720ed-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="720ed-122">INPUTS</span></span>

### <span data-ttu-id="720ed-123">System.String</span><span class="sxs-lookup"><span data-stu-id="720ed-123">System.String</span></span>

## <span data-ttu-id="720ed-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="720ed-124">OUTPUTS</span></span>

### <span data-ttu-id="720ed-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="720ed-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="720ed-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="720ed-126">NOTES</span></span>

## <span data-ttu-id="720ed-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="720ed-127">RELATED LINKS</span></span>

[<span data-ttu-id="720ed-128">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="720ed-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
