---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserverlocationbasedcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md
ms.openlocfilehash: 063abe34cbbd6c0f10e275e5b4b63f3c163b87e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146385"
---
# <span data-ttu-id="eb0d7-101">Get-AzPostgreSqlFlexibleServerLocationBasedCapability</span><span class="sxs-lookup"><span data-stu-id="eb0d7-101">Get-AzPostgreSqlFlexibleServerLocationBasedCapability</span></span>

## <span data-ttu-id="eb0d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb0d7-102">SYNOPSIS</span></span>
<span data-ttu-id="eb0d7-103">Verfügbare SKU-Informationen für den Speicherort</span><span class="sxs-lookup"><span data-stu-id="eb0d7-103">Get the available SKU information for the location</span></span>

## <span data-ttu-id="eb0d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb0d7-104">SYNTAX</span></span>

```
Get-AzPostgreSqlFlexibleServerLocationBasedCapability -Location <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="eb0d7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb0d7-105">DESCRIPTION</span></span>
<span data-ttu-id="eb0d7-106">Verfügbare SKU-Informationen für den Speicherort</span><span class="sxs-lookup"><span data-stu-id="eb0d7-106">Get the available SKU information for the location</span></span>

## <span data-ttu-id="eb0d7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eb0d7-107">EXAMPLES</span></span>

### <span data-ttu-id="eb0d7-108">Beispiel 1: Erhalten von Standortfunktionen nach Standortname</span><span class="sxs-lookup"><span data-stu-id="eb0d7-108">Example 1: Get location capabilities by location name</span></span>
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

<span data-ttu-id="eb0d7-109">Dieses Cmdlet zeigt grundlegende SKU-Informationen des bereitgestellten Speicherorts an.</span><span class="sxs-lookup"><span data-stu-id="eb0d7-109">This cmdlet shows basic sku information of the provided location.</span></span>

## <span data-ttu-id="eb0d7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb0d7-110">PARAMETERS</span></span>

### <span data-ttu-id="eb0d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb0d7-111">-DefaultProfile</span></span>
<span data-ttu-id="eb0d7-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb0d7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb0d7-113">-Location</span><span class="sxs-lookup"><span data-stu-id="eb0d7-113">-Location</span></span>
<span data-ttu-id="eb0d7-114">Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="eb0d7-114">The name of the location.</span></span>

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

### <span data-ttu-id="eb0d7-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eb0d7-115">-SubscriptionId</span></span>
<span data-ttu-id="eb0d7-116">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="eb0d7-116">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="eb0d7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb0d7-117">CommonParameters</span></span>
<span data-ttu-id="eb0d7-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb0d7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb0d7-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb0d7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb0d7-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eb0d7-120">INPUTS</span></span>

## <span data-ttu-id="eb0d7-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eb0d7-121">OUTPUTS</span></span>

### <span data-ttu-id="eb0d7-122">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.ICapabilityProperties</span><span class="sxs-lookup"><span data-stu-id="eb0d7-122">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.ICapabilityProperties</span></span>

## <span data-ttu-id="eb0d7-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="eb0d7-123">NOTES</span></span>

<span data-ttu-id="eb0d7-124">ALIASE</span><span class="sxs-lookup"><span data-stu-id="eb0d7-124">ALIASES</span></span>

## <span data-ttu-id="eb0d7-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="eb0d7-125">RELATED LINKS</span></span>

