---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: a5e35096966355a69ad5b363b61ab3cd5d2f0d0b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299680"
---
# <span data-ttu-id="9ddcf-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="9ddcf-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="9ddcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ddcf-102">SYNOPSIS</span></span>
<span data-ttu-id="9ddcf-103">Ruft die Details einer Replikationsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="9ddcf-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="9ddcf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ddcf-104">SYNTAX</span></span>

### <span data-ttu-id="9ddcf-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ddcf-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9ddcf-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="9ddcf-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9ddcf-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ddcf-107">DESCRIPTION</span></span>
<span data-ttu-id="9ddcf-108">Ruft die Details einer Replikationsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="9ddcf-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="9ddcf-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ddcf-109">EXAMPLES</span></span>

### <span data-ttu-id="9ddcf-110">Beispiel 1: Alle Richtlinien in einem Tresor speichern</span><span class="sxs-lookup"><span data-stu-id="9ddcf-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="9ddcf-111">Alle Richtlinien erhalten.</span><span class="sxs-lookup"><span data-stu-id="9ddcf-111">Get all policies.</span></span>

### <span data-ttu-id="9ddcf-112">Beispiel 2: Erhalten einer bestimmten Richtlinie</span><span class="sxs-lookup"><span data-stu-id="9ddcf-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="9ddcf-113">Holen Sie sich einen bestimmten.</span><span class="sxs-lookup"><span data-stu-id="9ddcf-113">Get a specific one.</span></span>

## <span data-ttu-id="9ddcf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ddcf-114">PARAMETERS</span></span>

### <span data-ttu-id="9ddcf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ddcf-115">-DefaultProfile</span></span>
<span data-ttu-id="9ddcf-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ddcf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ddcf-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="9ddcf-117">-PolicyName</span></span>
<span data-ttu-id="9ddcf-118">Name der Replikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="9ddcf-118">Replication policy name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddcf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ddcf-119">-ResourceGroupName</span></span>
<span data-ttu-id="9ddcf-120">Der Name der Ressourcengruppe, in der sich der Tresor der Wiederherstellungsdienste befindet.</span><span class="sxs-lookup"><span data-stu-id="9ddcf-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="9ddcf-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9ddcf-121">-ResourceName</span></span>
<span data-ttu-id="9ddcf-122">Der Name des Tresors der Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="9ddcf-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="9ddcf-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ddcf-123">-SubscriptionId</span></span>
<span data-ttu-id="9ddcf-124">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="9ddcf-124">The subscription Id.</span></span>

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

### <span data-ttu-id="9ddcf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ddcf-125">CommonParameters</span></span>
<span data-ttu-id="9ddcf-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ddcf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ddcf-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ddcf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ddcf-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ddcf-128">INPUTS</span></span>

## <span data-ttu-id="9ddcf-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ddcf-129">OUTPUTS</span></span>

### <span data-ttu-id="9ddcf-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="9ddcf-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="9ddcf-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9ddcf-131">NOTES</span></span>

<span data-ttu-id="9ddcf-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="9ddcf-132">ALIASES</span></span>

## <span data-ttu-id="9ddcf-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9ddcf-133">RELATED LINKS</span></span>

