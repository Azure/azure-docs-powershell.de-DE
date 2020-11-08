---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179070"
---
# <span data-ttu-id="0ef63-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="0ef63-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="0ef63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ef63-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef63-103">Erstellt ein neues migrate-Projekt.</span><span class="sxs-lookup"><span data-stu-id="0ef63-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="0ef63-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ef63-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0ef63-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ef63-105">DESCRIPTION</span></span>
<span data-ttu-id="0ef63-106">Erstellt ein neues migrate-Projekt.</span><span class="sxs-lookup"><span data-stu-id="0ef63-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="0ef63-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ef63-107">EXAMPLES</span></span>

### <span data-ttu-id="0ef63-108">Beispiel 1: erstellen (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ef63-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="0ef63-109">-Methode zum Erstellen eines neuen migrieren-Projekts</span><span class="sxs-lookup"><span data-stu-id="0ef63-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="0ef63-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ef63-110">PARAMETERS</span></span>

### <span data-ttu-id="0ef63-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="0ef63-111">-ETag</span></span>
<span data-ttu-id="0ef63-112">Gibt den Namen des VMware-Computers an.</span><span class="sxs-lookup"><span data-stu-id="0ef63-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="0ef63-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="0ef63-113">-Location</span></span>
<span data-ttu-id="0ef63-114">Gibt den Namen des VMware-Computers an.</span><span class="sxs-lookup"><span data-stu-id="0ef63-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="0ef63-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0ef63-115">-Name</span></span>
<span data-ttu-id="0ef63-116">Gibt den Namen des Projekts migrieren an.</span><span class="sxs-lookup"><span data-stu-id="0ef63-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="0ef63-117">-Property</span><span class="sxs-lookup"><span data-stu-id="0ef63-117">-Property</span></span>
<span data-ttu-id="0ef63-118">Gibt die Projekteigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="0ef63-118">Specifies the project properties.</span></span>
<span data-ttu-id="0ef63-119">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Eigenschafts Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0ef63-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="0ef63-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ef63-120">-ResourceGroupName</span></span>
<span data-ttu-id="0ef63-121">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0ef63-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="0ef63-122">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="0ef63-122">-SubscriptionId</span></span>
<span data-ttu-id="0ef63-123">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="0ef63-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="0ef63-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ef63-124">-Confirm</span></span>
<span data-ttu-id="0ef63-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0ef63-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ef63-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ef63-126">-WhatIf</span></span>
<span data-ttu-id="0ef63-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ef63-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ef63-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ef63-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ef63-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef63-129">CommonParameters</span></span>
<span data-ttu-id="0ef63-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ef63-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef63-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ef63-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef63-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ef63-132">INPUTS</span></span>

## <span data-ttu-id="0ef63-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ef63-133">OUTPUTS</span></span>

## <span data-ttu-id="0ef63-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ef63-134">NOTES</span></span>

<span data-ttu-id="0ef63-135">Aliase</span><span class="sxs-lookup"><span data-stu-id="0ef63-135">ALIASES</span></span>

<span data-ttu-id="0ef63-136">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0ef63-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0ef63-137">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0ef63-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ef63-138">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="0ef63-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0ef63-139">Eigenschaft <IMigrateProjectProperties> : gibt die Projekteigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="0ef63-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="0ef63-140">`[ProvisioningState <ProvisioningState?>]`: Bereitstellungsstatus des Projekts migrieren.</span><span class="sxs-lookup"><span data-stu-id="0ef63-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="0ef63-141">`[RegisteredTool <String[]>]`: Ruft die Liste der für das migrate-Projekt registrierten Tools ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="0ef63-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="0ef63-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ef63-142">RELATED LINKS</span></span>

