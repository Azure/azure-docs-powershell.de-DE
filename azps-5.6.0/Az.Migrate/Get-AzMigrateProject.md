---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 4176b07f8a19538a05899b526d21f21cfcc20c9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934088"
---
# <span data-ttu-id="eb3f3-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="eb3f3-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="eb3f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="eb3f3-103">Methode zum Erhalten eines Migrierenprojekts.</span><span class="sxs-lookup"><span data-stu-id="eb3f3-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="eb3f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb3f3-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="eb3f3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb3f3-105">DESCRIPTION</span></span>
<span data-ttu-id="eb3f3-106">Methode zum Erhalten eines Migrierenprojekts.</span><span class="sxs-lookup"><span data-stu-id="eb3f3-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="eb3f3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eb3f3-107">EXAMPLES</span></span>

### <span data-ttu-id="eb3f3-108">Beispiel 1: Get</span><span class="sxs-lookup"><span data-stu-id="eb3f3-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="eb3f3-109">Methode zum Erhalten eines Migrierenprojekts.</span><span class="sxs-lookup"><span data-stu-id="eb3f3-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="eb3f3-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eb3f3-110">PARAMETERS</span></span>

### <span data-ttu-id="eb3f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb3f3-111">-DefaultProfile</span></span>
<span data-ttu-id="eb3f3-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb3f3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb3f3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="eb3f3-113">-Name</span></span>
<span data-ttu-id="eb3f3-114">Name des Azure Migrate-Projekts.</span><span class="sxs-lookup"><span data-stu-id="eb3f3-114">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3f3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb3f3-115">-ResourceGroupName</span></span>
<span data-ttu-id="eb3f3-116">Der Name der Azure-Ressourcengruppe, zu der das Projekt migriert wird.</span><span class="sxs-lookup"><span data-stu-id="eb3f3-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="eb3f3-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eb3f3-117">-SubscriptionId</span></span>
<span data-ttu-id="eb3f3-118">Azure-Abonnement-ID, in der das Projekt migriert wurde.</span><span class="sxs-lookup"><span data-stu-id="eb3f3-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="eb3f3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb3f3-119">CommonParameters</span></span>
<span data-ttu-id="eb3f3-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb3f3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb3f3-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb3f3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb3f3-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eb3f3-122">INPUTS</span></span>

## <span data-ttu-id="eb3f3-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eb3f3-123">OUTPUTS</span></span>

### <span data-ttu-id="eb3f3-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="eb3f3-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="eb3f3-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eb3f3-125">NOTES</span></span>

<span data-ttu-id="eb3f3-126">ALIASE</span><span class="sxs-lookup"><span data-stu-id="eb3f3-126">ALIASES</span></span>

## <span data-ttu-id="eb3f3-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eb3f3-127">RELATED LINKS</span></span>

