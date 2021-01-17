---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: 62b43668e8d886a11a26204edcd3c8b13635eff4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385775"
---
# <span data-ttu-id="af956-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="af956-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="af956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af956-102">SYNOPSIS</span></span>
<span data-ttu-id="af956-103">Ruft eine Lösung im Projekt "Migrieren" ab.</span><span class="sxs-lookup"><span data-stu-id="af956-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="af956-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af956-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="af956-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af956-105">DESCRIPTION</span></span>
<span data-ttu-id="af956-106">Ruft eine Lösung im Projekt "Migrieren" ab.</span><span class="sxs-lookup"><span data-stu-id="af956-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="af956-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="af956-107">EXAMPLES</span></span>

### <span data-ttu-id="af956-108">Beispiel 1: Erhalten</span><span class="sxs-lookup"><span data-stu-id="af956-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="af956-109">Projektmappe nach Name migrieren</span><span class="sxs-lookup"><span data-stu-id="af956-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="af956-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af956-110">PARAMETERS</span></span>

### <span data-ttu-id="af956-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af956-111">-DefaultProfile</span></span>
<span data-ttu-id="af956-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af956-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af956-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="af956-113">-MigrateProjectName</span></span>
<span data-ttu-id="af956-114">Name des Azure Migrate-Projekts.</span><span class="sxs-lookup"><span data-stu-id="af956-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="af956-115">-Name</span><span class="sxs-lookup"><span data-stu-id="af956-115">-Name</span></span>
<span data-ttu-id="af956-116">Eindeutiger Name einer Migrationslösung innerhalb eines Migrationsprojekts.</span><span class="sxs-lookup"><span data-stu-id="af956-116">Unique name of a migration solution within a migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af956-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af956-117">-ResourceGroupName</span></span>
<span data-ttu-id="af956-118">Der Name der Azure-Ressourcengruppe, zu der das Projekt migriert wird.</span><span class="sxs-lookup"><span data-stu-id="af956-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="af956-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af956-119">-SubscriptionId</span></span>
<span data-ttu-id="af956-120">Azure-Abonnement-ID, in der das Projekt migriert wurde.</span><span class="sxs-lookup"><span data-stu-id="af956-120">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="af956-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af956-121">CommonParameters</span></span>
<span data-ttu-id="af956-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af956-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af956-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af956-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af956-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="af956-124">INPUTS</span></span>

## <span data-ttu-id="af956-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="af956-125">OUTPUTS</span></span>

### <span data-ttu-id="af956-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="af956-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="af956-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="af956-127">NOTES</span></span>

<span data-ttu-id="af956-128">ALIASE</span><span class="sxs-lookup"><span data-stu-id="af956-128">ALIASES</span></span>

## <span data-ttu-id="af956-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="af956-129">RELATED LINKS</span></span>

