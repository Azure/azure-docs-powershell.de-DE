---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 169b7c2daffdf2c241a60468e745752ac7582d7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165815"
---
# <span data-ttu-id="677de-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="677de-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="677de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="677de-102">SYNOPSIS</span></span>
<span data-ttu-id="677de-103">Abrufen verfügbarer Dienst Delegierungen in der Region</span><span class="sxs-lookup"><span data-stu-id="677de-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="677de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="677de-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="677de-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="677de-105">DESCRIPTION</span></span>
<span data-ttu-id="677de-106">Mit dem Cmdlet **Get-AzAvailableServiceDelegation** können Sie alle verfügbaren Dienst Delegierungen für ein Subnetz am angegebenen Speicherort abrufen.</span><span class="sxs-lookup"><span data-stu-id="677de-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="677de-107">Dieses Cmdlet beschreibt *nicht* , welche Delegierungen möglicherweise in einem einzelnen Subnetz nebeneinander vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="677de-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="677de-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="677de-108">EXAMPLES</span></span>

### <span data-ttu-id="677de-109">1: Abrufen aller verfügbaren Dienst Delegierungen</span><span class="sxs-lookup"><span data-stu-id="677de-109">1: Getting all available service delegations</span></span>
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

## <span data-ttu-id="677de-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="677de-110">PARAMETERS</span></span>

### <span data-ttu-id="677de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="677de-111">-DefaultProfile</span></span>
<span data-ttu-id="677de-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="677de-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="677de-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="677de-113">-Location</span></span>
<span data-ttu-id="677de-114">Die Position.</span><span class="sxs-lookup"><span data-stu-id="677de-114">The location.</span></span>

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

### <span data-ttu-id="677de-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="677de-115">CommonParameters</span></span>
<span data-ttu-id="677de-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="677de-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="677de-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="677de-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="677de-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="677de-118">INPUTS</span></span>

### <span data-ttu-id="677de-119">System. String</span><span class="sxs-lookup"><span data-stu-id="677de-119">System.String</span></span>

## <span data-ttu-id="677de-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="677de-120">OUTPUTS</span></span>

### <span data-ttu-id="677de-121">Microsoft. Azure. Commands. Network. Models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="677de-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="677de-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="677de-122">NOTES</span></span>

## <span data-ttu-id="677de-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="677de-123">RELATED LINKS</span></span>

<span data-ttu-id="677de-124">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Neu – AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="677de-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>