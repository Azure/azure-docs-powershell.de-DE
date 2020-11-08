---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: e0918573b7fc1190d32aaaaa4bfe73ed9fe05fe6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178834"
---
# <span data-ttu-id="7e43e-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="7e43e-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="7e43e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e43e-102">SYNOPSIS</span></span>
<span data-ttu-id="7e43e-103">Löschen Sie das Projekt migrieren.</span><span class="sxs-lookup"><span data-stu-id="7e43e-103">Delete the migrate project.</span></span>
<span data-ttu-id="7e43e-104">Das Löschen eines nicht vorhandenen Projekts ist kein Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7e43e-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="7e43e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e43e-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7e43e-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e43e-106">DESCRIPTION</span></span>
<span data-ttu-id="7e43e-107">Löschen Sie das Projekt migrieren.</span><span class="sxs-lookup"><span data-stu-id="7e43e-107">Delete the migrate project.</span></span>
<span data-ttu-id="7e43e-108">Das Löschen eines nicht vorhandenen Projekts ist kein Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7e43e-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="7e43e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e43e-109">EXAMPLES</span></span>

### <span data-ttu-id="7e43e-110">Beispiel 1: Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e43e-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="7e43e-111">Löschen Sie das Projekt migrieren.</span><span class="sxs-lookup"><span data-stu-id="7e43e-111">Delete the migrate project.</span></span>
<span data-ttu-id="7e43e-112">Das Löschen eines nicht vorhandenen Projekts ist kein Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7e43e-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="7e43e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e43e-113">PARAMETERS</span></span>

### <span data-ttu-id="7e43e-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="7e43e-114">-AcceptLanguage</span></span>
<span data-ttu-id="7e43e-115">Standard Anforderungs Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="7e43e-115">Standard request header.</span></span>
<span data-ttu-id="7e43e-116">Wird vom Dienst verwendet, um auf den Client in der entsprechenden Sprache zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="7e43e-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="7e43e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e43e-117">-DefaultProfile</span></span>
<span data-ttu-id="7e43e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e43e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e43e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7e43e-119">-Name</span></span>
<span data-ttu-id="7e43e-120">Name des Azure-Migrationsprojekts</span><span class="sxs-lookup"><span data-stu-id="7e43e-120">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="7e43e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e43e-121">-PassThru</span></span>
<span data-ttu-id="7e43e-122">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="7e43e-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7e43e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e43e-123">-ResourceGroupName</span></span>
<span data-ttu-id="7e43e-124">Der Name der Azure-Ressourcengruppe, in der Project migriert wird.</span><span class="sxs-lookup"><span data-stu-id="7e43e-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="7e43e-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7e43e-125">-SubscriptionId</span></span>
<span data-ttu-id="7e43e-126">Azure-Abonnement-ID, in der das Projekt "migrieren" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7e43e-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="7e43e-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7e43e-127">-Confirm</span></span>
<span data-ttu-id="7e43e-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e43e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e43e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e43e-129">-WhatIf</span></span>
<span data-ttu-id="7e43e-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e43e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e43e-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e43e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e43e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e43e-132">CommonParameters</span></span>
<span data-ttu-id="7e43e-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e43e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e43e-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e43e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e43e-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e43e-135">INPUTS</span></span>

## <span data-ttu-id="7e43e-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e43e-136">OUTPUTS</span></span>

### <span data-ttu-id="7e43e-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e43e-137">System.Boolean</span></span>

## <span data-ttu-id="7e43e-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e43e-138">NOTES</span></span>

<span data-ttu-id="7e43e-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="7e43e-139">ALIASES</span></span>

## <span data-ttu-id="7e43e-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e43e-140">RELATED LINKS</span></span>

