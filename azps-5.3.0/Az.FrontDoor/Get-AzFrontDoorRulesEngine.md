---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: c0742344db01e40a01a0aeee3b61b93b92cc3f07
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469812"
---
# <span data-ttu-id="c6373-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="c6373-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="c6373-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6373-102">SYNOPSIS</span></span>
<span data-ttu-id="c6373-103">"Regelmodulkonfigurationen" erhalten.</span><span class="sxs-lookup"><span data-stu-id="c6373-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="c6373-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6373-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6373-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6373-105">DESCRIPTION</span></span>
<span data-ttu-id="c6373-106">Das **Cmdlet "Get-AzFrontDspezifischRulesEngine"** ruft eine bestimmte Konfiguration des Enginemoduls für Regeln oder alle mit einer Front Door verknüpften Konfigurationen für das Regelmodul ab.</span><span class="sxs-lookup"><span data-stu-id="c6373-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="c6373-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c6373-107">EXAMPLES</span></span>

### <span data-ttu-id="c6373-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6373-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="c6373-109">Holen Sie sich die Konfiguration eines bestimmten Regelmoduls.</span><span class="sxs-lookup"><span data-stu-id="c6373-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="c6373-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c6373-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="c6373-111">Holen Sie sich alle Konfigurationen der Engine für Regeln in eine Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="c6373-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="c6373-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c6373-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="c6373-113">Erwartete Ausgabe beim Abrufen eines nicht vorhandenen Regelmoduls.</span><span class="sxs-lookup"><span data-stu-id="c6373-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="c6373-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6373-114">PARAMETERS</span></span>

### <span data-ttu-id="c6373-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6373-115">-DefaultProfile</span></span>
<span data-ttu-id="c6373-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6373-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6373-117">-FrontD ernennenName</span><span class="sxs-lookup"><span data-stu-id="c6373-117">-FrontDoorName</span></span>
<span data-ttu-id="c6373-118">Name der Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="c6373-118">Front Door name.</span></span>

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

### <span data-ttu-id="c6373-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c6373-119">-Name</span></span>
<span data-ttu-id="c6373-120">Name des Regelmoduls.</span><span class="sxs-lookup"><span data-stu-id="c6373-120">Rules engine name.</span></span>

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

### <span data-ttu-id="c6373-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6373-121">-ResourceGroupName</span></span>
<span data-ttu-id="c6373-122">Der Ressourcengruppenname, in dem die Eingangstür erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c6373-122">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="c6373-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6373-123">CommonParameters</span></span>
<span data-ttu-id="c6373-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6373-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6373-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6373-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6373-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c6373-126">INPUTS</span></span>

### <span data-ttu-id="c6373-127">Keine</span><span class="sxs-lookup"><span data-stu-id="c6373-127">None</span></span>

## <span data-ttu-id="c6373-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c6373-128">OUTPUTS</span></span>

### <span data-ttu-id="c6373-129">Microsoft.Azure.Commands.Frontd selbst.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="c6373-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="c6373-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c6373-130">NOTES</span></span>

## <span data-ttu-id="c6373-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c6373-131">RELATED LINKS</span></span>
