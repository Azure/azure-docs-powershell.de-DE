---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/initialize-azmigratereplicationinfrastructure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Initialize-AzMigrateReplicationInfrastructure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Initialize-AzMigrateReplicationInfrastructure.md
ms.openlocfilehash: 27206ac1c4e256efcd4093c8cdc9647b6059b3ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934008"
---
# <span data-ttu-id="605e8-101">Initialize-AzMigrateReplicationInfrastructure</span><span class="sxs-lookup"><span data-stu-id="605e8-101">Initialize-AzMigrateReplicationInfrastructure</span></span>

## <span data-ttu-id="605e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="605e8-102">SYNOPSIS</span></span>
<span data-ttu-id="605e8-103">Initialisiert die Infrastruktur für das Migrieren des Projekts.</span><span class="sxs-lookup"><span data-stu-id="605e8-103">Initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="605e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="605e8-104">SYNTAX</span></span>

```
Initialize-AzMigrateReplicationInfrastructure -ProjectName <String> -ResourceGroupName <String>
 -Scenario <String> -TargetRegion <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="605e8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="605e8-105">DESCRIPTION</span></span>
<span data-ttu-id="605e8-106">Das Initialize-AzMigrateReplicationInfrastructure cmdlet initialisiert die Infrastruktur für das Migrationsprojekt.</span><span class="sxs-lookup"><span data-stu-id="605e8-106">The Initialize-AzMigrateReplicationInfrastructure cmdlet initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="605e8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="605e8-107">EXAMPLES</span></span>

### <span data-ttu-id="605e8-108">Beispiel 1: Initialisiert die Infrastruktur für das Migrationsprojekt.</span><span class="sxs-lookup"><span data-stu-id="605e8-108">Example 1: Initialises the infrastructure for the migrate project.</span></span>
```powershell
PS C:\> Initialize-AzMigrateReplicationInfrastructure.ps1 -ResourceGroupName TestRG  -ProjectName TestProject -Vmwareagentless -TargetRegion centralus

True
```

<span data-ttu-id="605e8-109">Initialisiert die Infrastruktur für das Migrieren des Projekts.</span><span class="sxs-lookup"><span data-stu-id="605e8-109">Initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="605e8-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="605e8-110">PARAMETERS</span></span>

### <span data-ttu-id="605e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="605e8-111">-DefaultProfile</span></span>
<span data-ttu-id="605e8-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="605e8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="605e8-113">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="605e8-113">-ProjectName</span></span>
<span data-ttu-id="605e8-114">Gibt den Namen des Azure Migrate-Projekts an, das für die Servermigration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="605e8-114">Specifies the name of the Azure Migrate project to be used for server migration.</span></span>

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

### <span data-ttu-id="605e8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="605e8-115">-ResourceGroupName</span></span>
<span data-ttu-id="605e8-116">Gibt die Ressourcengruppe des Azure Migrate Project im aktuellen Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="605e8-116">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="605e8-117">-Scenario</span><span class="sxs-lookup"><span data-stu-id="605e8-117">-Scenario</span></span>
<span data-ttu-id="605e8-118">Gibt das Servermigrationsszenario an, für das die Replikationsinfrastruktur initialisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="605e8-118">Specifies the server migration scenario for which the replication infrastructure needs to be initialized.</span></span>

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

### <span data-ttu-id="605e8-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="605e8-119">-SubscriptionId</span></span>
<span data-ttu-id="605e8-120">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="605e8-120">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="605e8-121">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="605e8-121">-TargetRegion</span></span>
<span data-ttu-id="605e8-122">Gibt die Azure-Zielregion für Servermigrationen an.</span><span class="sxs-lookup"><span data-stu-id="605e8-122">Specifies the target Azure region for server migrations.</span></span>

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

### <span data-ttu-id="605e8-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="605e8-123">-Confirm</span></span>
<span data-ttu-id="605e8-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="605e8-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="605e8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="605e8-125">-WhatIf</span></span>
<span data-ttu-id="605e8-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="605e8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="605e8-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="605e8-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="605e8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="605e8-128">CommonParameters</span></span>
<span data-ttu-id="605e8-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="605e8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="605e8-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="605e8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="605e8-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="605e8-131">INPUTS</span></span>

## <span data-ttu-id="605e8-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="605e8-132">OUTPUTS</span></span>

### <span data-ttu-id="605e8-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="605e8-133">System.Boolean</span></span>

## <span data-ttu-id="605e8-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="605e8-134">NOTES</span></span>

<span data-ttu-id="605e8-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="605e8-135">ALIASES</span></span>

## <span data-ttu-id="605e8-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="605e8-136">RELATED LINKS</span></span>

