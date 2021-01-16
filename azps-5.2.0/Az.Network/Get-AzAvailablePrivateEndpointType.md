---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: 1ca9e604a1371d83fdedd2986534fa8926b6286b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296789"
---
# <span data-ttu-id="2c768-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2c768-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="2c768-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c768-102">SYNOPSIS</span></span>
<span data-ttu-id="2c768-103">Geben Sie verfügbare private Endpunkttypen an der Position zurück.</span><span class="sxs-lookup"><span data-stu-id="2c768-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="2c768-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c768-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c768-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c768-105">DESCRIPTION</span></span>
<span data-ttu-id="2c768-106">Das **Cmdlet "Get-AzAvailablePrivateEndpointType"** gibt alle verfügbaren privaten Endpunkttypen an der Position zurück.</span><span class="sxs-lookup"><span data-stu-id="2c768-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="2c768-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2c768-107">EXAMPLES</span></span>

### <span data-ttu-id="2c768-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2c768-108">Example 1</span></span>
```powershell
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

<span data-ttu-id="2c768-109">In diesem Beispiel werden alle verfügbaren privaten Endpunkttypen an der Position zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2c768-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="2c768-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c768-110">PARAMETERS</span></span>

### <span data-ttu-id="2c768-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c768-111">-DefaultProfile</span></span>
<span data-ttu-id="2c768-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c768-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c768-113">-Location</span><span class="sxs-lookup"><span data-stu-id="2c768-113">-Location</span></span>
<span data-ttu-id="2c768-114">Der Ort.</span><span class="sxs-lookup"><span data-stu-id="2c768-114">The location.</span></span>

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

### <span data-ttu-id="2c768-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c768-115">-ResourceGroupName</span></span>
<span data-ttu-id="2c768-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2c768-116">The resource group name.</span></span>

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

### <span data-ttu-id="2c768-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c768-117">CommonParameters</span></span>
<span data-ttu-id="2c768-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c768-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c768-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c768-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c768-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2c768-120">INPUTS</span></span>

### <span data-ttu-id="2c768-121">System.String</span><span class="sxs-lookup"><span data-stu-id="2c768-121">System.String</span></span>

## <span data-ttu-id="2c768-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2c768-122">OUTPUTS</span></span>

### <span data-ttu-id="2c768-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2c768-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="2c768-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2c768-124">NOTES</span></span>

## <span data-ttu-id="2c768-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2c768-125">RELATED LINKS</span></span>
