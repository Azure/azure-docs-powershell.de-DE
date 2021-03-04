---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 8b3a14c9e8416c1ffc9809d09d664b7809f53a1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933960"
---
# <span data-ttu-id="c8873-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="c8873-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="c8873-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8873-102">SYNOPSIS</span></span>
<span data-ttu-id="c8873-103">Erstellt ein neues Migrieren-Projekt.</span><span class="sxs-lookup"><span data-stu-id="c8873-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="c8873-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8873-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c8873-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8873-105">DESCRIPTION</span></span>
<span data-ttu-id="c8873-106">Erstellt ein neues Migrieren-Projekt.</span><span class="sxs-lookup"><span data-stu-id="c8873-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="c8873-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c8873-107">EXAMPLES</span></span>

### <span data-ttu-id="c8873-108">Beispiel 1: Erstellen (Standard)</span><span class="sxs-lookup"><span data-stu-id="c8873-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="c8873-109">Methode zum Erstellen eines neuen Migrierenprojekts.</span><span class="sxs-lookup"><span data-stu-id="c8873-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="c8873-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c8873-110">PARAMETERS</span></span>

### <span data-ttu-id="c8873-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="c8873-111">-ETag</span></span>
<span data-ttu-id="c8873-112">Gibt den VMware-Computernamen an.</span><span class="sxs-lookup"><span data-stu-id="c8873-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="c8873-113">-Location</span><span class="sxs-lookup"><span data-stu-id="c8873-113">-Location</span></span>
<span data-ttu-id="c8873-114">Gibt den VMware-Computernamen an.</span><span class="sxs-lookup"><span data-stu-id="c8873-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="c8873-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c8873-115">-Name</span></span>
<span data-ttu-id="c8873-116">Gibt den Namen des Projekts migrieren an.</span><span class="sxs-lookup"><span data-stu-id="c8873-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="c8873-117">-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c8873-117">-Property</span></span>
<span data-ttu-id="c8873-118">Gibt die Projekteigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="c8873-118">Specifies the project properties.</span></span>
<span data-ttu-id="c8873-119">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu EIGENSCHAFTENeigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c8873-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="c8873-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8873-120">-ResourceGroupName</span></span>
<span data-ttu-id="c8873-121">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c8873-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="c8873-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8873-122">-SubscriptionId</span></span>
<span data-ttu-id="c8873-123">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="c8873-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="c8873-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c8873-124">-Confirm</span></span>
<span data-ttu-id="c8873-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8873-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8873-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8873-126">-WhatIf</span></span>
<span data-ttu-id="c8873-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8873-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8873-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8873-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8873-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8873-129">CommonParameters</span></span>
<span data-ttu-id="c8873-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8873-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8873-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8873-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8873-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c8873-132">INPUTS</span></span>

## <span data-ttu-id="c8873-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c8873-133">OUTPUTS</span></span>

## <span data-ttu-id="c8873-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c8873-134">NOTES</span></span>

<span data-ttu-id="c8873-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c8873-135">ALIASES</span></span>

<span data-ttu-id="c8873-136">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c8873-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c8873-137">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="c8873-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c8873-138">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c8873-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c8873-139">EIGENSCHAFT <IMigrateProjectProperties> : Gibt die Projekteigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="c8873-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="c8873-140">`[ProvisioningState <ProvisioningState?>]`: Bereitstellungszustand des Migrierenprojekts.</span><span class="sxs-lookup"><span data-stu-id="c8873-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="c8873-141">`[RegisteredTool <String[]>]`: Ruft die Liste der tools ab, die für das Migrierenprojekt registriert sind, oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="c8873-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="c8873-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c8873-142">RELATED LINKS</span></span>

