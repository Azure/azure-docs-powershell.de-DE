---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178839"
---
# <span data-ttu-id="7fa7d-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="7fa7d-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="7fa7d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7fa7d-102">SYNOPSIS</span></span>
<span data-ttu-id="7fa7d-103">Registriert ein Tool beim Migrieren eines Projekts.</span><span class="sxs-lookup"><span data-stu-id="7fa7d-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="7fa7d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fa7d-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7fa7d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7fa7d-105">DESCRIPTION</span></span>
<span data-ttu-id="7fa7d-106">Registriert ein Tool beim Migrieren eines Projekts.</span><span class="sxs-lookup"><span data-stu-id="7fa7d-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="7fa7d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7fa7d-107">EXAMPLES</span></span>

### <span data-ttu-id="7fa7d-108">Beispiel 1: Registrieren eines Tools</span><span class="sxs-lookup"><span data-stu-id="7fa7d-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="7fa7d-109">Registriert ein Tool beim Migrieren eines Projekts.</span><span class="sxs-lookup"><span data-stu-id="7fa7d-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="7fa7d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fa7d-110">PARAMETERS</span></span>

### <span data-ttu-id="7fa7d-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="7fa7d-111">-AcceptLanguage</span></span>
<span data-ttu-id="7fa7d-112">Standard Anforderungs Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="7fa7d-112">Standard request header.</span></span>
<span data-ttu-id="7fa7d-113">Wird vom Dienst verwendet, um auf den Client in der entsprechenden Sprache zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="7fa7d-113">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="7fa7d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fa7d-114">-DefaultProfile</span></span>
<span data-ttu-id="7fa7d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7fa7d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fa7d-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="7fa7d-116">-MigrateProjectName</span></span>
<span data-ttu-id="7fa7d-117">Name des Azure-Migrationsprojekts</span><span class="sxs-lookup"><span data-stu-id="7fa7d-117">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="7fa7d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fa7d-118">-ResourceGroupName</span></span>
<span data-ttu-id="7fa7d-119">Der Name der Azure-Ressourcengruppe, in der Project migriert wird.</span><span class="sxs-lookup"><span data-stu-id="7fa7d-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="7fa7d-120">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7fa7d-120">-SubscriptionId</span></span>
<span data-ttu-id="7fa7d-121">Azure-Abonnement-ID, in der das Projekt "migrieren" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7fa7d-121">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="7fa7d-122">-Tool</span><span class="sxs-lookup"><span data-stu-id="7fa7d-122">-Tool</span></span>
<span data-ttu-id="7fa7d-123">Ruft das zu Registrier Tool ab oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="7fa7d-123">Gets or sets the tool to be registered.</span></span>

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

### <span data-ttu-id="7fa7d-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7fa7d-124">-Confirm</span></span>
<span data-ttu-id="7fa7d-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7fa7d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fa7d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fa7d-126">-WhatIf</span></span>
<span data-ttu-id="7fa7d-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7fa7d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fa7d-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7fa7d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fa7d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fa7d-129">CommonParameters</span></span>
<span data-ttu-id="7fa7d-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fa7d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fa7d-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fa7d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fa7d-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7fa7d-132">INPUTS</span></span>

## <span data-ttu-id="7fa7d-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7fa7d-133">OUTPUTS</span></span>

### <span data-ttu-id="7fa7d-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7fa7d-134">System.Boolean</span></span>

## <span data-ttu-id="7fa7d-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="7fa7d-135">NOTES</span></span>

<span data-ttu-id="7fa7d-136">Aliase</span><span class="sxs-lookup"><span data-stu-id="7fa7d-136">ALIASES</span></span>

## <span data-ttu-id="7fa7d-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7fa7d-137">RELATED LINKS</span></span>

