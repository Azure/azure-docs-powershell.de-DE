---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: c0bc2b5a14fd8e3dee8694a8564e831c0f39a229
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845436"
---
# <span data-ttu-id="67929-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="67929-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="67929-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67929-102">SYNOPSIS</span></span>
<span data-ttu-id="67929-103">Gibt verfügbare private Endpunkttypen an der Position zurück.</span><span class="sxs-lookup"><span data-stu-id="67929-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="67929-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67929-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67929-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67929-105">DESCRIPTION</span></span>
<span data-ttu-id="67929-106">Das Cmdlet " **Get-AzAvailablePrivateEndpointType** " gibt alle verfügbaren privaten Endpunkttypen an der Position zurück.</span><span class="sxs-lookup"><span data-stu-id="67929-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="67929-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67929-107">EXAMPLES</span></span>

### <span data-ttu-id="67929-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="67929-108">Example</span></span>
```
Get-AzAvailablePrivateEndpointType -Location eastus

[
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename1",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Sql/servers"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename2",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Storage/accounts"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename3",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Cosmos/cosmosDbAccounts"
  }
]
```

<span data-ttu-id="67929-109">In diesem Beispiel werden alle verfügbaren privaten Endpunkttypen an der Position zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="67929-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="67929-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="67929-110">PARAMETERS</span></span>

### <span data-ttu-id="67929-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67929-111">-DefaultProfile</span></span>
<span data-ttu-id="67929-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67929-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67929-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="67929-113">-Location</span></span>
<span data-ttu-id="67929-114">Die Position.</span><span class="sxs-lookup"><span data-stu-id="67929-114">The location.</span></span>

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

### <span data-ttu-id="67929-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67929-115">-ResourceGroupName</span></span>
<span data-ttu-id="67929-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="67929-116">The resource group name.</span></span>

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

### <span data-ttu-id="67929-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67929-117">CommonParameters</span></span>
<span data-ttu-id="67929-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67929-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67929-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67929-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67929-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67929-120">INPUTS</span></span>

### <span data-ttu-id="67929-121">System. String</span><span class="sxs-lookup"><span data-stu-id="67929-121">System.String</span></span>

## <span data-ttu-id="67929-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67929-122">OUTPUTS</span></span>

### <span data-ttu-id="67929-123">Microsoft. Azure. Commands. Network. Models. PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="67929-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="67929-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="67929-124">NOTES</span></span>

## <span data-ttu-id="67929-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67929-125">RELATED LINKS</span></span>
