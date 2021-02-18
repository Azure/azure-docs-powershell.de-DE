---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173092"
---
# <span data-ttu-id="978f7-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="978f7-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="978f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="978f7-102">SYNOPSIS</span></span>
<span data-ttu-id="978f7-103">Methode zum Erhalten eines Projektmigrationsprojekts.</span><span class="sxs-lookup"><span data-stu-id="978f7-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="978f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="978f7-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="978f7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="978f7-105">DESCRIPTION</span></span>
<span data-ttu-id="978f7-106">Methode zum Erhalten eines Projektmigrationsprojekts.</span><span class="sxs-lookup"><span data-stu-id="978f7-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="978f7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="978f7-107">EXAMPLES</span></span>

### <span data-ttu-id="978f7-108">Beispiel 1: Get</span><span class="sxs-lookup"><span data-stu-id="978f7-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="978f7-109">Methode zum Erhalten eines Projektmigrationsprojekts.</span><span class="sxs-lookup"><span data-stu-id="978f7-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="978f7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="978f7-110">PARAMETERS</span></span>

### <span data-ttu-id="978f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="978f7-111">-DefaultProfile</span></span>
<span data-ttu-id="978f7-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="978f7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="978f7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="978f7-113">-Name</span></span>
<span data-ttu-id="978f7-114">Name des Azure Migrate-Projekts.</span><span class="sxs-lookup"><span data-stu-id="978f7-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="978f7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="978f7-115">-ResourceGroupName</span></span>
<span data-ttu-id="978f7-116">Der Name der Azure-Ressourcengruppe, zu der das Projekt migriert wird.</span><span class="sxs-lookup"><span data-stu-id="978f7-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="978f7-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="978f7-117">-SubscriptionId</span></span>
<span data-ttu-id="978f7-118">Azure-Abonnement-ID, in der das Projekt migriert wurde.</span><span class="sxs-lookup"><span data-stu-id="978f7-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="978f7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="978f7-119">CommonParameters</span></span>
<span data-ttu-id="978f7-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="978f7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="978f7-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="978f7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="978f7-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="978f7-122">INPUTS</span></span>

## <span data-ttu-id="978f7-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="978f7-123">OUTPUTS</span></span>

### <span data-ttu-id="978f7-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="978f7-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="978f7-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="978f7-125">NOTES</span></span>

<span data-ttu-id="978f7-126">ALIASE</span><span class="sxs-lookup"><span data-stu-id="978f7-126">ALIASES</span></span>

## <span data-ttu-id="978f7-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="978f7-127">RELATED LINKS</span></span>

