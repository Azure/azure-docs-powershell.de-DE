---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356766"
---
# <span data-ttu-id="672ee-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="672ee-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="672ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="672ee-102">SYNOPSIS</span></span>
<span data-ttu-id="672ee-103">Registriert ein Tool für das Projekt "Migrieren".</span><span class="sxs-lookup"><span data-stu-id="672ee-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="672ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="672ee-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="672ee-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="672ee-105">DESCRIPTION</span></span>
<span data-ttu-id="672ee-106">Registriert ein Tool für das Projekt "Migrieren".</span><span class="sxs-lookup"><span data-stu-id="672ee-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="672ee-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="672ee-107">EXAMPLES</span></span>

### <span data-ttu-id="672ee-108">Beispiel 1: REgister Tool.</span><span class="sxs-lookup"><span data-stu-id="672ee-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="672ee-109">Registriert ein Tool für das Projekt "Migrieren".</span><span class="sxs-lookup"><span data-stu-id="672ee-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="672ee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="672ee-110">PARAMETERS</span></span>

### <span data-ttu-id="672ee-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="672ee-111">-AcceptLanguage</span></span>
<span data-ttu-id="672ee-112">Standardanforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="672ee-112">Standard request header.</span></span>
<span data-ttu-id="672ee-113">Wird vom Dienst verwendet, um auf den Client in der entsprechenden Sprache zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="672ee-113">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="672ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="672ee-114">-DefaultProfile</span></span>
<span data-ttu-id="672ee-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="672ee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="672ee-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="672ee-116">-MigrateProjectName</span></span>
<span data-ttu-id="672ee-117">Name des Azure Migrate-Projekts.</span><span class="sxs-lookup"><span data-stu-id="672ee-117">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="672ee-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="672ee-118">-ResourceGroupName</span></span>
<span data-ttu-id="672ee-119">Der Name der Azure-Ressourcengruppe, zu der das Projekt migriert wird.</span><span class="sxs-lookup"><span data-stu-id="672ee-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="672ee-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="672ee-120">-SubscriptionId</span></span>
<span data-ttu-id="672ee-121">Azure-Abonnement-ID, in der das Projekt migriert wurde.</span><span class="sxs-lookup"><span data-stu-id="672ee-121">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="672ee-122">-Tool</span><span class="sxs-lookup"><span data-stu-id="672ee-122">-Tool</span></span>
<span data-ttu-id="672ee-123">Ruft das Tool ab oder legt es so fest, dass es registriert wird.</span><span class="sxs-lookup"><span data-stu-id="672ee-123">Gets or sets the tool to be registered.</span></span>

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

### <span data-ttu-id="672ee-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="672ee-124">-Confirm</span></span>
<span data-ttu-id="672ee-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="672ee-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="672ee-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="672ee-126">-WhatIf</span></span>
<span data-ttu-id="672ee-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="672ee-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="672ee-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="672ee-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="672ee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="672ee-129">CommonParameters</span></span>
<span data-ttu-id="672ee-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="672ee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="672ee-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="672ee-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="672ee-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="672ee-132">INPUTS</span></span>

## <span data-ttu-id="672ee-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="672ee-133">OUTPUTS</span></span>

### <span data-ttu-id="672ee-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="672ee-134">System.Boolean</span></span>

## <span data-ttu-id="672ee-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="672ee-135">NOTES</span></span>

<span data-ttu-id="672ee-136">ALIASE</span><span class="sxs-lookup"><span data-stu-id="672ee-136">ALIASES</span></span>

## <span data-ttu-id="672ee-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="672ee-137">RELATED LINKS</span></span>

