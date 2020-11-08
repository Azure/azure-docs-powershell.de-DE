---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: c0742344db01e40a01a0aeee3b61b93b92cc3f07
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175164"
---
# <span data-ttu-id="c3d03-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="c3d03-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="c3d03-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3d03-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d03-103">Abrufen von Regelmodul Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="c3d03-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="c3d03-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3d03-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3d03-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3d03-105">DESCRIPTION</span></span>
<span data-ttu-id="c3d03-106">Das Cmdlet " **Get-AzFrontDoorRulesEngine** " Ruft eine bestimmte Regelmodul Konfiguration ab oder ruft alle Regelmodul Konfigurationen ab, die mit einer Haustür verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="c3d03-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="c3d03-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3d03-107">EXAMPLES</span></span>

### <span data-ttu-id="c3d03-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3d03-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="c3d03-109">Abrufen einer bestimmten Regelmodul Konfiguration</span><span class="sxs-lookup"><span data-stu-id="c3d03-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="c3d03-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c3d03-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="c3d03-111">Alle Regelmodul Konfigurationen in einer Haustür abrufen.</span><span class="sxs-lookup"><span data-stu-id="c3d03-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="c3d03-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c3d03-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="c3d03-113">Erwartete Ausgabe beim Abrufen eines nicht vorhandenen Regelmoduls.</span><span class="sxs-lookup"><span data-stu-id="c3d03-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="c3d03-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3d03-114">PARAMETERS</span></span>

### <span data-ttu-id="c3d03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d03-115">-DefaultProfile</span></span>
<span data-ttu-id="c3d03-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3d03-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3d03-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="c3d03-117">-FrontDoorName</span></span>
<span data-ttu-id="c3d03-118">Name der Haustüre</span><span class="sxs-lookup"><span data-stu-id="c3d03-118">Front Door name.</span></span>

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

### <span data-ttu-id="c3d03-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c3d03-119">-Name</span></span>
<span data-ttu-id="c3d03-120">Name des Regelmoduls</span><span class="sxs-lookup"><span data-stu-id="c3d03-120">Rules engine name.</span></span>

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

### <span data-ttu-id="c3d03-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3d03-121">-ResourceGroupName</span></span>
<span data-ttu-id="c3d03-122">Der Ressourcengruppenname, in dem die Haustür erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c3d03-122">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="c3d03-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d03-123">CommonParameters</span></span>
<span data-ttu-id="c3d03-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3d03-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d03-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3d03-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d03-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3d03-126">INPUTS</span></span>

### <span data-ttu-id="c3d03-127">Keine</span><span class="sxs-lookup"><span data-stu-id="c3d03-127">None</span></span>

## <span data-ttu-id="c3d03-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3d03-128">OUTPUTS</span></span>

### <span data-ttu-id="c3d03-129">Microsoft. Azure. Commands. Haustür. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="c3d03-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="c3d03-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3d03-130">NOTES</span></span>

## <span data-ttu-id="c3d03-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3d03-131">RELATED LINKS</span></span>
