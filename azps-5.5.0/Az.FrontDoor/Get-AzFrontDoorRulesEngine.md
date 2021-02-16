---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: c0742344db01e40a01a0aeee3b61b93b92cc3f07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175449"
---
# <span data-ttu-id="efa2c-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="efa2c-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="efa2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efa2c-102">SYNOPSIS</span></span>
<span data-ttu-id="efa2c-103">"Regelmodulkonfigurationen" erhalten.</span><span class="sxs-lookup"><span data-stu-id="efa2c-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="efa2c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="efa2c-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efa2c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="efa2c-105">DESCRIPTION</span></span>
<span data-ttu-id="efa2c-106">Das **Cmdlet "Get-AzFrontDspezifischRulesEngine"** erhält eine bestimmte Konfiguration der Engine für Regeln oder alle Konfigurationen von Regelnmodulen, die mit einer Front Door verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="efa2c-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="efa2c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="efa2c-107">EXAMPLES</span></span>

### <span data-ttu-id="efa2c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="efa2c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="efa2c-109">Holen Sie sich die Konfiguration eines bestimmten Regelmoduls.</span><span class="sxs-lookup"><span data-stu-id="efa2c-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="efa2c-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="efa2c-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="efa2c-111">Lassen Sie alle Konfigurationen der Engine für Regeln direkt neben sich.</span><span class="sxs-lookup"><span data-stu-id="efa2c-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="efa2c-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="efa2c-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="efa2c-113">Erwartete Ausgabe beim Abrufen eines nicht vorhandenen Regelmoduls.</span><span class="sxs-lookup"><span data-stu-id="efa2c-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="efa2c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efa2c-114">PARAMETERS</span></span>

### <span data-ttu-id="efa2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa2c-115">-DefaultProfile</span></span>
<span data-ttu-id="efa2c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="efa2c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efa2c-117">-FrontD ernennenName</span><span class="sxs-lookup"><span data-stu-id="efa2c-117">-FrontDoorName</span></span>
<span data-ttu-id="efa2c-118">Name der Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="efa2c-118">Front Door name.</span></span>

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

### <span data-ttu-id="efa2c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="efa2c-119">-Name</span></span>
<span data-ttu-id="efa2c-120">Name des Regelmoduls.</span><span class="sxs-lookup"><span data-stu-id="efa2c-120">Rules engine name.</span></span>

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

### <span data-ttu-id="efa2c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efa2c-121">-ResourceGroupName</span></span>
<span data-ttu-id="efa2c-122">Der Ressourcengruppenname, in dem die Eingangstür erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="efa2c-122">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="efa2c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa2c-123">CommonParameters</span></span>
<span data-ttu-id="efa2c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efa2c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa2c-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efa2c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa2c-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="efa2c-126">INPUTS</span></span>

### <span data-ttu-id="efa2c-127">Keine</span><span class="sxs-lookup"><span data-stu-id="efa2c-127">None</span></span>

## <span data-ttu-id="efa2c-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="efa2c-128">OUTPUTS</span></span>

### <span data-ttu-id="efa2c-129">Microsoft.Azure.Commands.Frontd selbst.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="efa2c-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="efa2c-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="efa2c-130">NOTES</span></span>

## <span data-ttu-id="efa2c-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="efa2c-131">RELATED LINKS</span></span>
