---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: e0918573b7fc1190d32aaaaa4bfe73ed9fe05fe6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459040"
---
# <span data-ttu-id="90e47-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="90e47-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="90e47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90e47-102">SYNOPSIS</span></span>
<span data-ttu-id="90e47-103">Löschen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="90e47-103">Delete the migrate project.</span></span>
<span data-ttu-id="90e47-104">Das Löschen eines nicht vorhandenen Projekts ist keine Operation.</span><span class="sxs-lookup"><span data-stu-id="90e47-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="90e47-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90e47-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="90e47-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90e47-106">DESCRIPTION</span></span>
<span data-ttu-id="90e47-107">Löschen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="90e47-107">Delete the migrate project.</span></span>
<span data-ttu-id="90e47-108">Das Löschen eines nicht vorhandenen Projekts ist keine Operation.</span><span class="sxs-lookup"><span data-stu-id="90e47-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="90e47-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="90e47-109">EXAMPLES</span></span>

### <span data-ttu-id="90e47-110">Beispiel 1: Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="90e47-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="90e47-111">Löschen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="90e47-111">Delete the migrate project.</span></span>
<span data-ttu-id="90e47-112">Das Löschen eines nicht vorhandenen Projekts ist keine Operation.</span><span class="sxs-lookup"><span data-stu-id="90e47-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="90e47-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90e47-113">PARAMETERS</span></span>

### <span data-ttu-id="90e47-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="90e47-114">-AcceptLanguage</span></span>
<span data-ttu-id="90e47-115">Standardanforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="90e47-115">Standard request header.</span></span>
<span data-ttu-id="90e47-116">Wird vom Dienst verwendet, um auf den Client in der entsprechenden Sprache zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="90e47-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="90e47-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e47-117">-DefaultProfile</span></span>
<span data-ttu-id="90e47-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90e47-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90e47-119">-Name</span><span class="sxs-lookup"><span data-stu-id="90e47-119">-Name</span></span>
<span data-ttu-id="90e47-120">Name des Azure Migrate-Projekts.</span><span class="sxs-lookup"><span data-stu-id="90e47-120">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="90e47-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90e47-121">-PassThru</span></span>
<span data-ttu-id="90e47-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="90e47-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e47-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e47-123">-ResourceGroupName</span></span>
<span data-ttu-id="90e47-124">Der Name der Azure-Ressourcengruppe, zu der das Projekt migriert wird.</span><span class="sxs-lookup"><span data-stu-id="90e47-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="90e47-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90e47-125">-SubscriptionId</span></span>
<span data-ttu-id="90e47-126">Azure-Abonnement-ID, in der das Projekt migriert wurde.</span><span class="sxs-lookup"><span data-stu-id="90e47-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="90e47-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90e47-127">-Confirm</span></span>
<span data-ttu-id="90e47-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90e47-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e47-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="90e47-129">-WhatIf</span></span>
<span data-ttu-id="90e47-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90e47-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90e47-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90e47-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e47-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e47-132">CommonParameters</span></span>
<span data-ttu-id="90e47-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90e47-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e47-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90e47-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e47-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="90e47-135">INPUTS</span></span>

## <span data-ttu-id="90e47-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="90e47-136">OUTPUTS</span></span>

### <span data-ttu-id="90e47-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="90e47-137">System.Boolean</span></span>

## <span data-ttu-id="90e47-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="90e47-138">NOTES</span></span>

<span data-ttu-id="90e47-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="90e47-139">ALIASES</span></span>

## <span data-ttu-id="90e47-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="90e47-140">RELATED LINKS</span></span>

