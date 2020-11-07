---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 786a8009d1423b6b12fae4d7eb8da6899a8cd108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824036"
---
# <span data-ttu-id="09ee0-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="09ee0-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="09ee0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="09ee0-103">Ruft eine Liste der Peering-Dienstanbieter ab, die mit Microsoft in Partnerschaft sind.</span><span class="sxs-lookup"><span data-stu-id="09ee0-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="09ee0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09ee0-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09ee0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09ee0-105">DESCRIPTION</span></span>
<span data-ttu-id="09ee0-106">Listen Peering-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="09ee0-106">List peering service providers</span></span>

## <span data-ttu-id="09ee0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09ee0-107">EXAMPLES</span></span>

### <span data-ttu-id="09ee0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="09ee0-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="09ee0-109">Ruft verfügbare Peering-Dienstanbieter ab</span><span class="sxs-lookup"><span data-stu-id="09ee0-109">Gets available peering service providers</span></span>

## <span data-ttu-id="09ee0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="09ee0-110">PARAMETERS</span></span>

### <span data-ttu-id="09ee0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ee0-111">-DefaultProfile</span></span>
<span data-ttu-id="09ee0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09ee0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09ee0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ee0-113">CommonParameters</span></span>
<span data-ttu-id="09ee0-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09ee0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ee0-115">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09ee0-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ee0-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09ee0-116">INPUTS</span></span>

### <span data-ttu-id="09ee0-117">Keine</span><span class="sxs-lookup"><span data-stu-id="09ee0-117">None</span></span>

## <span data-ttu-id="09ee0-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09ee0-118">OUTPUTS</span></span>

### <span data-ttu-id="09ee0-119">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="09ee0-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="09ee0-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="09ee0-120">NOTES</span></span>

## <span data-ttu-id="09ee0-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09ee0-121">RELATED LINKS</span></span>
