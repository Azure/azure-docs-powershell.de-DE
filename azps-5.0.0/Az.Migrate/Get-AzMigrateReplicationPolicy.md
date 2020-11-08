---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: a5e35096966355a69ad5b363b61ab3cd5d2f0d0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180274"
---
# <span data-ttu-id="2a622-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="2a622-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="2a622-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2a622-102">SYNOPSIS</span></span>
<span data-ttu-id="2a622-103">Ruft die Details einer Replikationsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="2a622-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="2a622-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a622-104">SYNTAX</span></span>

### <span data-ttu-id="2a622-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="2a622-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2a622-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="2a622-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2a622-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a622-107">DESCRIPTION</span></span>
<span data-ttu-id="2a622-108">Ruft die Details einer Replikationsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="2a622-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="2a622-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2a622-109">EXAMPLES</span></span>

### <span data-ttu-id="2a622-110">Beispiel 1: Abrufen aller Richtlinien in einem Tresor</span><span class="sxs-lookup"><span data-stu-id="2a622-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="2a622-111">Alle Richtlinien abrufen.</span><span class="sxs-lookup"><span data-stu-id="2a622-111">Get all policies.</span></span>

### <span data-ttu-id="2a622-112">Beispiel 2: Abrufen einer bestimmten Richtlinie</span><span class="sxs-lookup"><span data-stu-id="2a622-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="2a622-113">Besorgen Sie sich einen bestimmten.</span><span class="sxs-lookup"><span data-stu-id="2a622-113">Get a specific one.</span></span>

## <span data-ttu-id="2a622-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a622-114">PARAMETERS</span></span>

### <span data-ttu-id="2a622-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a622-115">-DefaultProfile</span></span>
<span data-ttu-id="2a622-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2a622-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a622-117">-Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="2a622-117">-PolicyName</span></span>
<span data-ttu-id="2a622-118">Name der Replikationsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="2a622-118">Replication policy name.</span></span>

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

### <span data-ttu-id="2a622-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a622-119">-ResourceGroupName</span></span>
<span data-ttu-id="2a622-120">Der Name der Ressourcengruppe, in der der Vault für Wiederherstellungsdienste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2a622-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="2a622-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2a622-121">-ResourceName</span></span>
<span data-ttu-id="2a622-122">Der Name des Speichers für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="2a622-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="2a622-123">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2a622-123">-SubscriptionId</span></span>
<span data-ttu-id="2a622-124">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="2a622-124">The subscription Id.</span></span>

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

### <span data-ttu-id="2a622-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a622-125">CommonParameters</span></span>
<span data-ttu-id="2a622-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a622-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a622-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a622-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a622-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2a622-128">INPUTS</span></span>

## <span data-ttu-id="2a622-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2a622-129">OUTPUTS</span></span>

### <span data-ttu-id="2a622-130">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. iPolicy</span><span class="sxs-lookup"><span data-stu-id="2a622-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="2a622-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="2a622-131">NOTES</span></span>

<span data-ttu-id="2a622-132">Aliase</span><span class="sxs-lookup"><span data-stu-id="2a622-132">ALIASES</span></span>

## <span data-ttu-id="2a622-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2a622-133">RELATED LINKS</span></span>

