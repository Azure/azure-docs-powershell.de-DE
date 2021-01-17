---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303704"
---
# <span data-ttu-id="47484-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="47484-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="47484-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47484-102">SYNOPSIS</span></span>
<span data-ttu-id="47484-103">Erstellen Sie eine neue Konfiguration des Regelmoduls für eine angegebene Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="47484-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="47484-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47484-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47484-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47484-105">DESCRIPTION</span></span>
<span data-ttu-id="47484-106">Erstellen Sie eine neue Konfiguration des Regelmoduls für eine angegebene Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="47484-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="47484-107">Verwenden Sie das Cmdlet "New-AzFrontDullRulesEngineRule", um Regeln des Moduls für Regeln zu erstellen, die an den Parameter "-Rules" dieses Cmdlets übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47484-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="47484-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="47484-108">EXAMPLES</span></span>

### <span data-ttu-id="47484-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="47484-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="47484-110">Erstellen Sie eine neue Konfiguration des Regelmoduls für angegebene Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="47484-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="47484-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47484-111">PARAMETERS</span></span>

### <span data-ttu-id="47484-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47484-112">-DefaultProfile</span></span>
<span data-ttu-id="47484-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47484-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47484-114">-FrontD ernennenName</span><span class="sxs-lookup"><span data-stu-id="47484-114">-FrontDoorName</span></span>
<span data-ttu-id="47484-115">Name der Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="47484-115">Front Door name.</span></span>

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

### <span data-ttu-id="47484-116">-Name</span><span class="sxs-lookup"><span data-stu-id="47484-116">-Name</span></span>
<span data-ttu-id="47484-117">Name des Regelmoduls.</span><span class="sxs-lookup"><span data-stu-id="47484-117">Rules engine name.</span></span>

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

### <span data-ttu-id="47484-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47484-118">-ResourceGroupName</span></span>
<span data-ttu-id="47484-119">Der Ressourcengruppenname, in dem die Eingangstür erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="47484-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="47484-120">-Rule</span><span class="sxs-lookup"><span data-stu-id="47484-120">-Rule</span></span>
<span data-ttu-id="47484-121">Eine Liste von Regeln, die eine bestimmte Konfiguration des Regelmoduls definieren.</span><span class="sxs-lookup"><span data-stu-id="47484-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47484-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47484-122">-Confirm</span></span>
<span data-ttu-id="47484-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47484-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47484-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="47484-124">-WhatIf</span></span>
<span data-ttu-id="47484-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47484-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47484-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47484-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47484-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47484-127">CommonParameters</span></span>
<span data-ttu-id="47484-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47484-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47484-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47484-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47484-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="47484-130">INPUTS</span></span>

### <span data-ttu-id="47484-131">Keine</span><span class="sxs-lookup"><span data-stu-id="47484-131">None</span></span>

## <span data-ttu-id="47484-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="47484-132">OUTPUTS</span></span>

### <span data-ttu-id="47484-133">Microsoft.Azure.Commands.Frontd selbst.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="47484-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="47484-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="47484-134">NOTES</span></span>

## <span data-ttu-id="47484-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="47484-135">RELATED LINKS</span></span>
