---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385747"
---
# <span data-ttu-id="b5d07-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="b5d07-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="b5d07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5d07-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d07-103">Erstellt ein neues Projekt "Migrieren".</span><span class="sxs-lookup"><span data-stu-id="b5d07-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="b5d07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5d07-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b5d07-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5d07-105">DESCRIPTION</span></span>
<span data-ttu-id="b5d07-106">Erstellt ein neues Projekt "Migrieren".</span><span class="sxs-lookup"><span data-stu-id="b5d07-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="b5d07-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b5d07-107">EXAMPLES</span></span>

### <span data-ttu-id="b5d07-108">Beispiel 1: Erstellen (Standard)</span><span class="sxs-lookup"><span data-stu-id="b5d07-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="b5d07-109">Methode zum Erstellen eines neuen Migrationprojekts.</span><span class="sxs-lookup"><span data-stu-id="b5d07-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="b5d07-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5d07-110">PARAMETERS</span></span>

### <span data-ttu-id="b5d07-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="b5d07-111">-ETag</span></span>
<span data-ttu-id="b5d07-112">Gibt den Namen des VMware-Computers an.</span><span class="sxs-lookup"><span data-stu-id="b5d07-112">Specifies the VMware machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d07-113">-Location</span><span class="sxs-lookup"><span data-stu-id="b5d07-113">-Location</span></span>
<span data-ttu-id="b5d07-114">Gibt den Namen des VMware-Computers an.</span><span class="sxs-lookup"><span data-stu-id="b5d07-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="b5d07-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b5d07-115">-Name</span></span>
<span data-ttu-id="b5d07-116">Gibt den Namen des Projekts "Migrieren" an.</span><span class="sxs-lookup"><span data-stu-id="b5d07-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="b5d07-117">-Property</span><span class="sxs-lookup"><span data-stu-id="b5d07-117">-Property</span></span>
<span data-ttu-id="b5d07-118">Gibt die Projekteigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="b5d07-118">Specifies the project properties.</span></span>
<span data-ttu-id="b5d07-119">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu EIGENSCHAFTENeigenschaften und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b5d07-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProjectProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d07-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5d07-120">-ResourceGroupName</span></span>
<span data-ttu-id="b5d07-121">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b5d07-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="b5d07-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5d07-122">-SubscriptionId</span></span>
<span data-ttu-id="b5d07-123">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="b5d07-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="b5d07-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5d07-124">-Confirm</span></span>
<span data-ttu-id="b5d07-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5d07-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5d07-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b5d07-126">-WhatIf</span></span>
<span data-ttu-id="b5d07-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5d07-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5d07-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5d07-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5d07-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d07-129">CommonParameters</span></span>
<span data-ttu-id="b5d07-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5d07-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d07-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5d07-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d07-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b5d07-132">INPUTS</span></span>

## <span data-ttu-id="b5d07-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b5d07-133">OUTPUTS</span></span>

## <span data-ttu-id="b5d07-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b5d07-134">NOTES</span></span>

<span data-ttu-id="b5d07-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b5d07-135">ALIASES</span></span>

<span data-ttu-id="b5d07-136">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b5d07-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b5d07-137">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b5d07-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b5d07-138">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b5d07-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b5d07-139">EIGENSCHAFT: <IMigrateProjectProperties> Gibt die Projekteigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="b5d07-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="b5d07-140">`[ProvisioningState <ProvisioningState?>]`: Bereitstellungszustand des Migrierenprojekts.</span><span class="sxs-lookup"><span data-stu-id="b5d07-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="b5d07-141">`[RegisteredTool <String[]>]`: Ruft die Liste der Tools ab, die für das Projekt zum Migrieren registriert sind, oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="b5d07-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="b5d07-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b5d07-142">RELATED LINKS</span></span>

