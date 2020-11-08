---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177622"
---
# <span data-ttu-id="16331-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="16331-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="16331-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16331-102">SYNOPSIS</span></span>
<span data-ttu-id="16331-103">Erstellen Sie eine neue Regelmodul Konfiguration für eine angegebene Haustür.</span><span class="sxs-lookup"><span data-stu-id="16331-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="16331-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16331-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16331-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16331-105">DESCRIPTION</span></span>
<span data-ttu-id="16331-106">Erstellen Sie eine neue Regelmodul Konfiguration für eine angegebene Haustür.</span><span class="sxs-lookup"><span data-stu-id="16331-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="16331-107">Verwenden Sie das Cmdlet "New-AzFrontDoorRulesEngineRule", um Regeln Modul Regeln zu erstellen, die an den Parameter "-Rules" dieses Cmdlets übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="16331-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="16331-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16331-108">EXAMPLES</span></span>

### <span data-ttu-id="16331-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16331-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="16331-110">Erstellen Sie eine neue Regelmodul Konfiguration für die angegebene Haustür.</span><span class="sxs-lookup"><span data-stu-id="16331-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="16331-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="16331-111">PARAMETERS</span></span>

### <span data-ttu-id="16331-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16331-112">-DefaultProfile</span></span>
<span data-ttu-id="16331-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16331-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16331-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="16331-114">-FrontDoorName</span></span>
<span data-ttu-id="16331-115">Name der Haustüre</span><span class="sxs-lookup"><span data-stu-id="16331-115">Front Door name.</span></span>

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

### <span data-ttu-id="16331-116">-Name</span><span class="sxs-lookup"><span data-stu-id="16331-116">-Name</span></span>
<span data-ttu-id="16331-117">Name des Regelmoduls</span><span class="sxs-lookup"><span data-stu-id="16331-117">Rules engine name.</span></span>

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

### <span data-ttu-id="16331-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16331-118">-ResourceGroupName</span></span>
<span data-ttu-id="16331-119">Der Ressourcengruppenname, in dem die Haustür erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="16331-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="16331-120">-Rule</span><span class="sxs-lookup"><span data-stu-id="16331-120">-Rule</span></span>
<span data-ttu-id="16331-121">Eine Liste von Regeln, die eine bestimmte Regelmodul Konfiguration definieren.</span><span class="sxs-lookup"><span data-stu-id="16331-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="16331-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="16331-122">-Confirm</span></span>
<span data-ttu-id="16331-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16331-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16331-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16331-124">-WhatIf</span></span>
<span data-ttu-id="16331-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16331-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16331-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16331-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16331-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16331-127">CommonParameters</span></span>
<span data-ttu-id="16331-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16331-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16331-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16331-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16331-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16331-130">INPUTS</span></span>

### <span data-ttu-id="16331-131">Keine</span><span class="sxs-lookup"><span data-stu-id="16331-131">None</span></span>

## <span data-ttu-id="16331-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16331-132">OUTPUTS</span></span>

### <span data-ttu-id="16331-133">Microsoft. Azure. Commands. Haustür. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="16331-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="16331-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="16331-134">NOTES</span></span>

## <span data-ttu-id="16331-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16331-135">RELATED LINKS</span></span>
