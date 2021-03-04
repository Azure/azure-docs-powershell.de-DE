---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlflexibleserverlocationbasedcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md
ms.openlocfilehash: efe45da6cd5426fda3b301efd4daf2ef532e4c02
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919483"
---
# <span data-ttu-id="882ea-101">Get-AzPostgreSqlFlexibleServerLocationBasedCapability</span><span class="sxs-lookup"><span data-stu-id="882ea-101">Get-AzPostgreSqlFlexibleServerLocationBasedCapability</span></span>

## <span data-ttu-id="882ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="882ea-102">SYNOPSIS</span></span>
<span data-ttu-id="882ea-103">Erhalten der verfügbaren SKU-Informationen für den Standort</span><span class="sxs-lookup"><span data-stu-id="882ea-103">Get the available SKU information for the location</span></span>

## <span data-ttu-id="882ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="882ea-104">SYNTAX</span></span>

```
Get-AzPostgreSqlFlexibleServerLocationBasedCapability -Location <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="882ea-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="882ea-105">DESCRIPTION</span></span>
<span data-ttu-id="882ea-106">Erhalten der verfügbaren SKU-Informationen für den Standort</span><span class="sxs-lookup"><span data-stu-id="882ea-106">Get the available SKU information for the location</span></span>

## <span data-ttu-id="882ea-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="882ea-107">EXAMPLES</span></span>

### <span data-ttu-id="882ea-108">Beispiel 1: Standortfunktionen nach Standortname erhalten</span><span class="sxs-lookup"><span data-stu-id="882ea-108">Example 1: Get location capabilities by location name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerLocationBasedCapability -Location eastus

SKU              Tier            Memory vCore
---              ----            ------ -----
Standard_B1ms    Burstable         2048     1
Standard_B2s     Burstable         2048     2
Standard_D2s_v3  GeneralPurpose    4096     2
Standard_D4s_v3  GeneralPurpose    4096     4
Standard_D8s_v3  GeneralPurpose    4096     8
Standard_D16s_v3 GeneralPurpose    4096    16
Standard_D32s_v3 GeneralPurpose    4096    32
Standard_D48s_v3 GeneralPurpose    4096    48
Standard_D64s_v3 GeneralPurpose    4096    64
Standard_E2s_v3  MemoryOptimized   8192     2
Standard_E4s_v3  MemoryOptimized   8192     4
Standard_E8s_v3  MemoryOptimized   8192     8
Standard_E16s_v3 MemoryOptimized   8192    16
Standard_E32s_v3 MemoryOptimized   8192    32
Standard_E48s_v3 MemoryOptimized   8192    48
Standard_E64s_v3 MemoryOptimized   6912    64
```

<span data-ttu-id="882ea-109">Dieses Cmdlet zeigt grundlegende Sku-Informationen des bereitgestellten Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="882ea-109">This cmdlet shows basic sku information of the provided location.</span></span>

## <span data-ttu-id="882ea-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="882ea-110">PARAMETERS</span></span>

### <span data-ttu-id="882ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="882ea-111">-DefaultProfile</span></span>
<span data-ttu-id="882ea-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="882ea-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="882ea-113">-Location</span><span class="sxs-lookup"><span data-stu-id="882ea-113">-Location</span></span>
<span data-ttu-id="882ea-114">Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="882ea-114">The name of the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="882ea-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="882ea-115">-SubscriptionId</span></span>
<span data-ttu-id="882ea-116">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="882ea-116">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="882ea-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="882ea-117">CommonParameters</span></span>
<span data-ttu-id="882ea-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="882ea-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="882ea-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="882ea-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="882ea-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="882ea-120">INPUTS</span></span>

## <span data-ttu-id="882ea-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="882ea-121">OUTPUTS</span></span>

### <span data-ttu-id="882ea-122">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.ICapabilityProperties</span><span class="sxs-lookup"><span data-stu-id="882ea-122">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.ICapabilityProperties</span></span>

## <span data-ttu-id="882ea-123">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="882ea-123">NOTES</span></span>

<span data-ttu-id="882ea-124">ALIASE</span><span class="sxs-lookup"><span data-stu-id="882ea-124">ALIASES</span></span>

## <span data-ttu-id="882ea-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="882ea-125">RELATED LINKS</span></span>

