---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 4dceb934f5cf746908c289c7662de0dc3dae09a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996095"
---
# <span data-ttu-id="96062-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="96062-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="96062-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96062-102">SYNOPSIS</span></span>
<span data-ttu-id="96062-103">Entfernt eine Integration-Konto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="96062-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="96062-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96062-104">SYNTAX</span></span>

### <span data-ttu-id="96062-105">ByIntegrationAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="96062-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96062-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="96062-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96062-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="96062-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96062-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96062-108">DESCRIPTION</span></span>
<span data-ttu-id="96062-109">Das Cmdlet **Remove-AzIntegrationAccountAssembly** entfernt eine Assembly aus einem Integrations Konto.</span><span class="sxs-lookup"><span data-stu-id="96062-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="96062-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96062-110">EXAMPLES</span></span>

### <span data-ttu-id="96062-111">Beispiel 1: Entfernen einer Assembly anhand von Parametern</span><span class="sxs-lookup"><span data-stu-id="96062-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="96062-112">Entfernt die Assembly mit dem Namen "SampleAssembly", die sich im Integrations Konto "sampleIntegrationAccount" befindet.</span><span class="sxs-lookup"><span data-stu-id="96062-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="96062-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="96062-113">PARAMETERS</span></span>

### <span data-ttu-id="96062-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96062-114">-DefaultProfile</span></span>
<span data-ttu-id="96062-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="96062-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96062-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="96062-116">-InputObject</span></span>
<span data-ttu-id="96062-117">Eine Integration Account-Assembly.</span><span class="sxs-lookup"><span data-stu-id="96062-117">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96062-118">-Name</span><span class="sxs-lookup"><span data-stu-id="96062-118">-Name</span></span>
<span data-ttu-id="96062-119">Der Name der Integrations Konto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="96062-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96062-120">-Übergeordneter</span><span class="sxs-lookup"><span data-stu-id="96062-120">-ParentName</span></span>
<span data-ttu-id="96062-121">Der Name des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="96062-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96062-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96062-122">-PassThru</span></span>
<span data-ttu-id="96062-123">Gibt zurück, ob der Befehl erfolgreich war oder nicht.</span><span class="sxs-lookup"><span data-stu-id="96062-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="96062-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96062-124">-ResourceGroupName</span></span>
<span data-ttu-id="96062-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="96062-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96062-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="96062-126">-ResourceId</span></span>
<span data-ttu-id="96062-127">Die Ressourcen-ID der Integrations Konto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="96062-127">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96062-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="96062-128">-Confirm</span></span>
<span data-ttu-id="96062-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="96062-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96062-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96062-130">-WhatIf</span></span>
<span data-ttu-id="96062-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96062-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96062-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96062-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96062-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96062-133">CommonParameters</span></span>
<span data-ttu-id="96062-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96062-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96062-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96062-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96062-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96062-136">INPUTS</span></span>

### <span data-ttu-id="96062-137">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="96062-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="96062-138">System. String</span><span class="sxs-lookup"><span data-stu-id="96062-138">System.String</span></span>

## <span data-ttu-id="96062-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96062-139">OUTPUTS</span></span>

### <span data-ttu-id="96062-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96062-140">System.Boolean</span></span>

## <span data-ttu-id="96062-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="96062-141">NOTES</span></span>

## <span data-ttu-id="96062-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96062-142">RELATED LINKS</span></span>
