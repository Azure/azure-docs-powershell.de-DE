---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: e4d9b8cd09aa1bf1528de1cd2179a76e7907e82b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009666"
---
# <span data-ttu-id="028ab-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="028ab-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="028ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="028ab-102">SYNOPSIS</span></span>
<span data-ttu-id="028ab-103">Erstellt ein STATICROUTE-Objekt, das einem RoutingConfiguration-Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="028ab-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="028ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="028ab-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="028ab-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="028ab-105">DESCRIPTION</span></span>
<span data-ttu-id="028ab-106">Erstellt ein STATICROUTE-Objekt.</span><span class="sxs-lookup"><span data-stu-id="028ab-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="028ab-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="028ab-107">EXAMPLES</span></span>

### <span data-ttu-id="028ab-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="028ab-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="028ab-109">Mit dem obigen Befehl wird ein STATICROUTE-Objekt erstellt, das einem RoutingConfiguration-Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="028ab-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="028ab-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="028ab-110">PARAMETERS</span></span>

### <span data-ttu-id="028ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="028ab-111">-DefaultProfile</span></span>
<span data-ttu-id="028ab-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="028ab-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="028ab-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="028ab-113">-AddressPrefix</span></span>
<span data-ttu-id="028ab-114">Liste der Adresspräfixe</span><span class="sxs-lookup"><span data-stu-id="028ab-114">List of address prefixes.</span></span>

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

### <span data-ttu-id="028ab-115">-Name</span><span class="sxs-lookup"><span data-stu-id="028ab-115">-Name</span></span>
<span data-ttu-id="028ab-116">Der Name der Route.</span><span class="sxs-lookup"><span data-stu-id="028ab-116">The route name.</span></span>

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

### <span data-ttu-id="028ab-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="028ab-117">-NextHopIpAddress</span></span>
<span data-ttu-id="028ab-118">Die IP-Adresse des nächsten Hop.</span><span class="sxs-lookup"><span data-stu-id="028ab-118">The next hop ip address.</span></span>

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

### <span data-ttu-id="028ab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="028ab-119">CommonParameters</span></span>
<span data-ttu-id="028ab-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="028ab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="028ab-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="028ab-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="028ab-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="028ab-122">INPUTS</span></span>

### <span data-ttu-id="028ab-123">System. String</span><span class="sxs-lookup"><span data-stu-id="028ab-123">System.String</span></span>

## <span data-ttu-id="028ab-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="028ab-124">OUTPUTS</span></span>

### <span data-ttu-id="028ab-125">Microsoft. Azure. Commands. Network. Models. PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="028ab-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="028ab-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="028ab-126">NOTES</span></span>

## <span data-ttu-id="028ab-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="028ab-127">RELATED LINKS</span></span>

[<span data-ttu-id="028ab-128">Neu – AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="028ab-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
