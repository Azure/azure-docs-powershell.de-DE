---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: d9edb00bf7944400fa681f857dd7005d9eaf69b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944993"
---
# <span data-ttu-id="9ae3e-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="9ae3e-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="9ae3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ae3e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae3e-103">Löschen Sie das Migrieren des Projekts.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-103">Delete the migrate project.</span></span>
<span data-ttu-id="9ae3e-104">Das Löschen eines nicht vorhandenen Projekts ist kein Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="9ae3e-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ae3e-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9ae3e-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ae3e-106">DESCRIPTION</span></span>
<span data-ttu-id="9ae3e-107">Löschen Sie das Migrieren des Projekts.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-107">Delete the migrate project.</span></span>
<span data-ttu-id="9ae3e-108">Das Löschen eines nicht vorhandenen Projekts ist kein Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="9ae3e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ae3e-109">EXAMPLES</span></span>

### <span data-ttu-id="9ae3e-110">Beispiel 1: Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ae3e-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="9ae3e-111">Löschen Sie das Migrieren des Projekts.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-111">Delete the migrate project.</span></span>
<span data-ttu-id="9ae3e-112">Das Löschen eines nicht vorhandenen Projekts ist kein Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="9ae3e-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9ae3e-113">PARAMETERS</span></span>

### <span data-ttu-id="9ae3e-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="9ae3e-114">-AcceptLanguage</span></span>
<span data-ttu-id="9ae3e-115">Standardanforderungskopf.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-115">Standard request header.</span></span>
<span data-ttu-id="9ae3e-116">Wird vom Dienst verwendet, um auf den Client in der entsprechenden Sprache zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="9ae3e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ae3e-117">-DefaultProfile</span></span>
<span data-ttu-id="9ae3e-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ae3e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9ae3e-119">-Name</span></span>
<span data-ttu-id="9ae3e-120">Name des Azure Migrate-Projekts.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-120">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="9ae3e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ae3e-121">-PassThru</span></span>
<span data-ttu-id="9ae3e-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9ae3e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ae3e-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ae3e-124">Der Name der Azure-Ressourcengruppe, zu der das Projekt migriert wird.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="9ae3e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ae3e-125">-SubscriptionId</span></span>
<span data-ttu-id="9ae3e-126">Azure-Abonnement-ID, in der das Projekt migriert wurde.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="9ae3e-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ae3e-127">-Confirm</span></span>
<span data-ttu-id="9ae3e-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ae3e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ae3e-129">-WhatIf</span></span>
<span data-ttu-id="9ae3e-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ae3e-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ae3e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae3e-132">CommonParameters</span></span>
<span data-ttu-id="9ae3e-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ae3e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae3e-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ae3e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae3e-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ae3e-135">INPUTS</span></span>

## <span data-ttu-id="9ae3e-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ae3e-136">OUTPUTS</span></span>

### <span data-ttu-id="9ae3e-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9ae3e-137">System.Boolean</span></span>

## <span data-ttu-id="9ae3e-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9ae3e-138">NOTES</span></span>

<span data-ttu-id="9ae3e-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="9ae3e-139">ALIASES</span></span>

## <span data-ttu-id="9ae3e-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9ae3e-140">RELATED LINKS</span></span>

