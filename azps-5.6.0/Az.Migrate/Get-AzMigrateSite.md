---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: b00010096b39cd714f01f33012309f8528a5ae3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934016"
---
# <span data-ttu-id="84274-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="84274-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="84274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84274-102">SYNOPSIS</span></span>
<span data-ttu-id="84274-103">Methode zum Erhalten einer Website.</span><span class="sxs-lookup"><span data-stu-id="84274-103">Method to get a site.</span></span>

## <span data-ttu-id="84274-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84274-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="84274-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84274-105">DESCRIPTION</span></span>
<span data-ttu-id="84274-106">Methode zum Erhalten einer Website.</span><span class="sxs-lookup"><span data-stu-id="84274-106">Method to get a site.</span></span>

## <span data-ttu-id="84274-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="84274-107">EXAMPLES</span></span>

### <span data-ttu-id="84274-108">Beispiel 1: Get (Standard)</span><span class="sxs-lookup"><span data-stu-id="84274-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="84274-109">Website nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="84274-109">Get site by name</span></span>

## <span data-ttu-id="84274-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="84274-110">PARAMETERS</span></span>

### <span data-ttu-id="84274-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84274-111">-DefaultProfile</span></span>
<span data-ttu-id="84274-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84274-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84274-113">-Name</span><span class="sxs-lookup"><span data-stu-id="84274-113">-Name</span></span>
<span data-ttu-id="84274-114">Websitename.</span><span class="sxs-lookup"><span data-stu-id="84274-114">Site name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84274-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84274-115">-ResourceGroupName</span></span>
<span data-ttu-id="84274-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="84274-116">The name of the resource group.</span></span>
<span data-ttu-id="84274-117">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="84274-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="84274-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="84274-118">-SubscriptionId</span></span>
<span data-ttu-id="84274-119">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="84274-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="84274-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84274-120">CommonParameters</span></span>
<span data-ttu-id="84274-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84274-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84274-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84274-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84274-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="84274-123">INPUTS</span></span>

## <span data-ttu-id="84274-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="84274-124">OUTPUTS</span></span>

### <span data-ttu-id="84274-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span><span class="sxs-lookup"><span data-stu-id="84274-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="84274-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="84274-126">NOTES</span></span>

<span data-ttu-id="84274-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="84274-127">ALIASES</span></span>

## <span data-ttu-id="84274-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="84274-128">RELATED LINKS</span></span>

