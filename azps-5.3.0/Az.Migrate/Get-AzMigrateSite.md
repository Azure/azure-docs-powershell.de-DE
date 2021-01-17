---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467588"
---
# <span data-ttu-id="8fc22-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="8fc22-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="8fc22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fc22-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc22-103">Methode zum Erhalten einer Website.</span><span class="sxs-lookup"><span data-stu-id="8fc22-103">Method to get a site.</span></span>

## <span data-ttu-id="8fc22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8fc22-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8fc22-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8fc22-105">DESCRIPTION</span></span>
<span data-ttu-id="8fc22-106">Methode zum Erhalten einer Website.</span><span class="sxs-lookup"><span data-stu-id="8fc22-106">Method to get a site.</span></span>

## <span data-ttu-id="8fc22-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8fc22-107">EXAMPLES</span></span>

### <span data-ttu-id="8fc22-108">Beispiel 1: Get (Standard)</span><span class="sxs-lookup"><span data-stu-id="8fc22-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="8fc22-109">Website nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="8fc22-109">Get site by name</span></span>

## <span data-ttu-id="8fc22-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fc22-110">PARAMETERS</span></span>

### <span data-ttu-id="8fc22-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc22-111">-DefaultProfile</span></span>
<span data-ttu-id="8fc22-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8fc22-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fc22-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8fc22-113">-Name</span></span>
<span data-ttu-id="8fc22-114">Websitename.</span><span class="sxs-lookup"><span data-stu-id="8fc22-114">Site name.</span></span>

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

### <span data-ttu-id="8fc22-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fc22-115">-ResourceGroupName</span></span>
<span data-ttu-id="8fc22-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8fc22-116">The name of the resource group.</span></span>
<span data-ttu-id="8fc22-117">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="8fc22-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8fc22-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8fc22-118">-SubscriptionId</span></span>
<span data-ttu-id="8fc22-119">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="8fc22-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8fc22-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc22-120">CommonParameters</span></span>
<span data-ttu-id="8fc22-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fc22-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc22-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8fc22-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc22-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8fc22-123">INPUTS</span></span>

## <span data-ttu-id="8fc22-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8fc22-124">OUTPUTS</span></span>

### <span data-ttu-id="8fc22-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span><span class="sxs-lookup"><span data-stu-id="8fc22-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="8fc22-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8fc22-126">NOTES</span></span>

<span data-ttu-id="8fc22-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="8fc22-127">ALIASES</span></span>

## <span data-ttu-id="8fc22-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8fc22-128">RELATED LINKS</span></span>

