---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 169b7c2daffdf2c241a60468e745752ac7582d7d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172897"
---
# <span data-ttu-id="00101-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="00101-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="00101-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00101-102">SYNOPSIS</span></span>
<span data-ttu-id="00101-103">Holen Sie sich den verfügbaren Dienst in der Region.</span><span class="sxs-lookup"><span data-stu-id="00101-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="00101-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00101-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00101-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00101-105">DESCRIPTION</span></span>
<span data-ttu-id="00101-106">Mit **dem Cmdlet "Get-AzAvailableServiceDelegation"** können Sie alle verfügbaren Dienstdienste für ein Subnetz am angegebenen Standort abrufen.</span><span class="sxs-lookup"><span data-stu-id="00101-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="00101-107">Dieses Cmdlet beschreibt *nicht,* welche Subnetze in einem einzelnen Subnetz vorhanden sein können.</span><span class="sxs-lookup"><span data-stu-id="00101-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="00101-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="00101-108">EXAMPLES</span></span>

### <span data-ttu-id="00101-109">1: Abrufen aller verfügbaren Dienste</span><span class="sxs-lookup"><span data-stu-id="00101-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzAvailableServiceDelegation -Location "westus"

Name        : Microsoft.Web.serverFarms
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Web.serverFarms
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Web/serverFarms
Actions     : {Microsoft.Network/virtualNetworks/subnets/action}

Name        : Microsoft.Sql.servers
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Sql.servers
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Sql/servers
Actions     : {}
```

## <span data-ttu-id="00101-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00101-110">PARAMETERS</span></span>

### <span data-ttu-id="00101-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00101-111">-DefaultProfile</span></span>
<span data-ttu-id="00101-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00101-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00101-113">-Location</span><span class="sxs-lookup"><span data-stu-id="00101-113">-Location</span></span>
<span data-ttu-id="00101-114">Der Ort.</span><span class="sxs-lookup"><span data-stu-id="00101-114">The location.</span></span>

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

### <span data-ttu-id="00101-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00101-115">CommonParameters</span></span>
<span data-ttu-id="00101-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00101-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00101-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00101-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00101-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="00101-118">INPUTS</span></span>

### <span data-ttu-id="00101-119">System.String</span><span class="sxs-lookup"><span data-stu-id="00101-119">System.String</span></span>

## <span data-ttu-id="00101-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="00101-120">OUTPUTS</span></span>

### <span data-ttu-id="00101-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="00101-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="00101-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="00101-122">NOTES</span></span>

## <span data-ttu-id="00101-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="00101-123">RELATED LINKS</span></span>

<span data-ttu-id="00101-124">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="00101-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>