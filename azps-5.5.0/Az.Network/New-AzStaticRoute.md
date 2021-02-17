---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: e4d9b8cd09aa1bf1528de1cd2179a76e7907e82b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154241"
---
# <span data-ttu-id="e10a4-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="e10a4-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="e10a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e10a4-102">SYNOPSIS</span></span>
<span data-ttu-id="e10a4-103">Erstellt ein StaticRoute-Objekt, das dann einem RoutingConfiguration-Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e10a4-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="e10a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e10a4-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e10a4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e10a4-105">DESCRIPTION</span></span>
<span data-ttu-id="e10a4-106">Erstellt ein StaticRoute-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e10a4-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="e10a4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e10a4-107">EXAMPLES</span></span>

### <span data-ttu-id="e10a4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e10a4-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="e10a4-109">Mit dem oben angegebenen Befehl wird ein StaticRoute-Objekt erstellt, das dann einem RoutingConfiguration-Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e10a4-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="e10a4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e10a4-110">PARAMETERS</span></span>

### <span data-ttu-id="e10a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e10a4-111">-DefaultProfile</span></span>
<span data-ttu-id="e10a4-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e10a4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e10a4-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e10a4-113">-AddressPrefix</span></span>
<span data-ttu-id="e10a4-114">Liste der Adresspräfixe.</span><span class="sxs-lookup"><span data-stu-id="e10a4-114">List of address prefixes.</span></span>

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

### <span data-ttu-id="e10a4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e10a4-115">-Name</span></span>
<span data-ttu-id="e10a4-116">Der Routenname.</span><span class="sxs-lookup"><span data-stu-id="e10a4-116">The route name.</span></span>

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

### <span data-ttu-id="e10a4-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="e10a4-117">-NextHopIpAddress</span></span>
<span data-ttu-id="e10a4-118">Die ip-Adresse des nächsten Hops.</span><span class="sxs-lookup"><span data-stu-id="e10a4-118">The next hop ip address.</span></span>

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

### <span data-ttu-id="e10a4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e10a4-119">CommonParameters</span></span>
<span data-ttu-id="e10a4-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e10a4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e10a4-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e10a4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e10a4-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e10a4-122">INPUTS</span></span>

### <span data-ttu-id="e10a4-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e10a4-123">System.String</span></span>

## <span data-ttu-id="e10a4-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e10a4-124">OUTPUTS</span></span>

### <span data-ttu-id="e10a4-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="e10a4-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="e10a4-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e10a4-126">NOTES</span></span>

## <span data-ttu-id="e10a4-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e10a4-127">RELATED LINKS</span></span>

[<span data-ttu-id="e10a4-128">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="e10a4-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
