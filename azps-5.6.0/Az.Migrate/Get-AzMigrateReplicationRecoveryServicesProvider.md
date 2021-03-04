---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: 2e890de56cdcf0ac2b17853b10629a58fce6c3b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934032"
---
# <span data-ttu-id="29d20-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="29d20-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="29d20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29d20-102">SYNOPSIS</span></span>
<span data-ttu-id="29d20-103">Ruft die Details des registrierten Wiederherstellungsdiensteanbieters ab.</span><span class="sxs-lookup"><span data-stu-id="29d20-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="29d20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29d20-104">SYNTAX</span></span>

### <span data-ttu-id="29d20-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="29d20-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="29d20-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="29d20-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="29d20-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29d20-107">DESCRIPTION</span></span>
<span data-ttu-id="29d20-108">Ruft die Details des registrierten Wiederherstellungsdiensteanbieters ab.</span><span class="sxs-lookup"><span data-stu-id="29d20-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="29d20-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29d20-109">EXAMPLES</span></span>

### <span data-ttu-id="29d20-110">Beispiel 1: Alle Anbieter im Tresor erhalten</span><span class="sxs-lookup"><span data-stu-id="29d20-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="29d20-111">Alle auflisten.</span><span class="sxs-lookup"><span data-stu-id="29d20-111">List all.</span></span>

## <span data-ttu-id="29d20-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="29d20-112">PARAMETERS</span></span>

### <span data-ttu-id="29d20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d20-113">-DefaultProfile</span></span>
<span data-ttu-id="29d20-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29d20-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29d20-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="29d20-115">-FabricName</span></span>
<span data-ttu-id="29d20-116">Fabricname.</span><span class="sxs-lookup"><span data-stu-id="29d20-116">Fabric name.</span></span>

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

### <span data-ttu-id="29d20-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="29d20-117">-ProviderName</span></span>
<span data-ttu-id="29d20-118">Name des Wiederherstellungsdiensteanbieters</span><span class="sxs-lookup"><span data-stu-id="29d20-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="29d20-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29d20-119">-ResourceGroupName</span></span>
<span data-ttu-id="29d20-120">Der Name der Ressourcengruppe, in der sich der Wiederherstellungsdiensttresor befindet.</span><span class="sxs-lookup"><span data-stu-id="29d20-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="29d20-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="29d20-121">-ResourceName</span></span>
<span data-ttu-id="29d20-122">Der Name des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="29d20-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="29d20-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="29d20-123">-SubscriptionId</span></span>
<span data-ttu-id="29d20-124">Azure-Abonnement-ID, in der das Projekt migriert wurde.</span><span class="sxs-lookup"><span data-stu-id="29d20-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="29d20-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d20-125">CommonParameters</span></span>
<span data-ttu-id="29d20-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29d20-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d20-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29d20-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d20-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29d20-128">INPUTS</span></span>

## <span data-ttu-id="29d20-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29d20-129">OUTPUTS</span></span>

### <span data-ttu-id="29d20-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="29d20-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="29d20-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="29d20-131">NOTES</span></span>

<span data-ttu-id="29d20-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="29d20-132">ALIASES</span></span>

## <span data-ttu-id="29d20-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="29d20-133">RELATED LINKS</span></span>

