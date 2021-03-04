---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: 60cc9b5b537c1d8e46f5bae56d93b33fa04f6c89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931003"
---
# <span data-ttu-id="7c2db-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="7c2db-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="7c2db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c2db-102">SYNOPSIS</span></span>
<span data-ttu-id="7c2db-103">Registriert ein Tool beim Migrieren des Projekts.</span><span class="sxs-lookup"><span data-stu-id="7c2db-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="7c2db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c2db-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7c2db-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c2db-105">DESCRIPTION</span></span>
<span data-ttu-id="7c2db-106">Registriert ein Tool beim Migrieren des Projekts.</span><span class="sxs-lookup"><span data-stu-id="7c2db-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="7c2db-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7c2db-107">EXAMPLES</span></span>

### <span data-ttu-id="7c2db-108">Beispiel 1: Tool "REgister".</span><span class="sxs-lookup"><span data-stu-id="7c2db-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="7c2db-109">Registriert ein Tool beim Migrieren des Projekts.</span><span class="sxs-lookup"><span data-stu-id="7c2db-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="7c2db-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7c2db-110">PARAMETERS</span></span>

### <span data-ttu-id="7c2db-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="7c2db-111">-AcceptLanguage</span></span>
<span data-ttu-id="7c2db-112">Standardanforderungskopf.</span><span class="sxs-lookup"><span data-stu-id="7c2db-112">Standard request header.</span></span>
<span data-ttu-id="7c2db-113">Wird vom Dienst verwendet, um auf den Client in der entsprechenden Sprache zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="7c2db-113">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="7c2db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c2db-114">-DefaultProfile</span></span>
<span data-ttu-id="7c2db-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c2db-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c2db-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="7c2db-116">-MigrateProjectName</span></span>
<span data-ttu-id="7c2db-117">Name des Azure Migrate-Projekts.</span><span class="sxs-lookup"><span data-stu-id="7c2db-117">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="7c2db-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c2db-118">-ResourceGroupName</span></span>
<span data-ttu-id="7c2db-119">Der Name der Azure-Ressourcengruppe, zu der das Projekt migriert wird.</span><span class="sxs-lookup"><span data-stu-id="7c2db-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="7c2db-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c2db-120">-SubscriptionId</span></span>
<span data-ttu-id="7c2db-121">Azure-Abonnement-ID, in der das Projekt migriert wurde.</span><span class="sxs-lookup"><span data-stu-id="7c2db-121">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="7c2db-122">-Tool</span><span class="sxs-lookup"><span data-stu-id="7c2db-122">-Tool</span></span>
<span data-ttu-id="7c2db-123">Ruft das Tool ab oder legt fest, dass es registriert wird.</span><span class="sxs-lookup"><span data-stu-id="7c2db-123">Gets or sets the tool to be registered.</span></span>

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

### <span data-ttu-id="7c2db-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7c2db-124">-Confirm</span></span>
<span data-ttu-id="7c2db-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c2db-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c2db-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c2db-126">-WhatIf</span></span>
<span data-ttu-id="7c2db-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c2db-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c2db-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c2db-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c2db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c2db-129">CommonParameters</span></span>
<span data-ttu-id="7c2db-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c2db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c2db-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c2db-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c2db-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7c2db-132">INPUTS</span></span>

## <span data-ttu-id="7c2db-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7c2db-133">OUTPUTS</span></span>

### <span data-ttu-id="7c2db-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c2db-134">System.Boolean</span></span>

## <span data-ttu-id="7c2db-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7c2db-135">NOTES</span></span>

<span data-ttu-id="7c2db-136">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7c2db-136">ALIASES</span></span>

## <span data-ttu-id="7c2db-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7c2db-137">RELATED LINKS</span></span>

