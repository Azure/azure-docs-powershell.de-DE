---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
ms.openlocfilehash: bc5c09913209713df192603aff7ea7646e651699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663650"
---
# <span data-ttu-id="e3a12-101">Get-AzureRmAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="e3a12-101">Get-AzureRmAvailableServiceDelegation</span></span>

## <span data-ttu-id="e3a12-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3a12-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a12-103">Abrufen verfügbarer Dienst Delegierungen in der Region</span><span class="sxs-lookup"><span data-stu-id="e3a12-103">Get available service delegations in the region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3a12-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3a12-104">SYNTAX</span></span>

```
Get-AzureRmAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3a12-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3a12-105">DESCRIPTION</span></span>
<span data-ttu-id="e3a12-106">Mit dem Cmdlet **Get-AzureRmAvailableServiceDelegation** können Sie alle verfügbaren Dienst Delegierungen für ein Subnetz am angegebenen Speicherort abrufen.</span><span class="sxs-lookup"><span data-stu-id="e3a12-106">The **Get-AzureRmAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="e3a12-107">Dieses Cmdlet beschreibt *nicht* , welche Delegierungen möglicherweise in einem einzelnen Subnetz nebeneinander vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e3a12-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="e3a12-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3a12-108">EXAMPLES</span></span>

### <span data-ttu-id="e3a12-109">1: Abrufen aller verfügbaren Dienst Delegierungen</span><span class="sxs-lookup"><span data-stu-id="e3a12-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzureRmAvailableServiceDelegation -Location "westus"

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

## <span data-ttu-id="e3a12-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3a12-110">PARAMETERS</span></span>

### <span data-ttu-id="e3a12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a12-111">-DefaultProfile</span></span>
<span data-ttu-id="e3a12-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e3a12-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a12-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="e3a12-113">-Location</span></span>
<span data-ttu-id="e3a12-114">Die Position.</span><span class="sxs-lookup"><span data-stu-id="e3a12-114">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a12-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a12-115">CommonParameters</span></span>
<span data-ttu-id="e3a12-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a12-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e3a12-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3a12-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a12-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3a12-118">INPUTS</span></span>

### <span data-ttu-id="e3a12-119">System. String</span><span class="sxs-lookup"><span data-stu-id="e3a12-119">System.String</span></span>

## <span data-ttu-id="e3a12-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3a12-120">OUTPUTS</span></span>

### <span data-ttu-id="e3a12-121">Microsoft. Azure. Commands. Network. Models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="e3a12-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="e3a12-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3a12-122">NOTES</span></span>

## <span data-ttu-id="e3a12-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3a12-123">RELATED LINKS</span></span>
<span data-ttu-id="e3a12-124">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Neu – AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="e3a12-124">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span></span>
