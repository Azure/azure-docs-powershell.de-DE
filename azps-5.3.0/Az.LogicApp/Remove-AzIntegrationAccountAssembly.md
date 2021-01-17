---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 4dceb934f5cf746908c289c7662de0dc3dae09a5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459103"
---
# <span data-ttu-id="2ec1c-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2ec1c-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="2ec1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ec1c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec1c-103">Entfernt eine Assembly für ein Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="2ec1c-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="2ec1c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ec1c-104">SYNTAX</span></span>

### <span data-ttu-id="2ec1c-105">ByIntegrationAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ec1c-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ec1c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2ec1c-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ec1c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2ec1c-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ec1c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ec1c-108">DESCRIPTION</span></span>
<span data-ttu-id="2ec1c-109">Das **Cmdlet "Remove-AzIntegrationAccountAssembly"** entfernt eine Assembly aus einem Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="2ec1c-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="2ec1c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2ec1c-110">EXAMPLES</span></span>

### <span data-ttu-id="2ec1c-111">Beispiel 1: Entfernen einer Assembly nach Parametern</span><span class="sxs-lookup"><span data-stu-id="2ec1c-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="2ec1c-112">Entfernt die Assembly mit dem Namen "sampleAssembly", die sich im Integrationskonto "sampleIntegrationAccount" befindet.</span><span class="sxs-lookup"><span data-stu-id="2ec1c-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="2ec1c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ec1c-113">PARAMETERS</span></span>

### <span data-ttu-id="2ec1c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec1c-114">-DefaultProfile</span></span>
<span data-ttu-id="2ec1c-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ec1c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ec1c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ec1c-116">-InputObject</span></span>
<span data-ttu-id="2ec1c-117">Eine Integrationskonto assembly.</span><span class="sxs-lookup"><span data-stu-id="2ec1c-117">An integration account assembly.</span></span>

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

### <span data-ttu-id="2ec1c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2ec1c-118">-Name</span></span>
<span data-ttu-id="2ec1c-119">Der Name der Integrationskonto assembly.</span><span class="sxs-lookup"><span data-stu-id="2ec1c-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="2ec1c-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="2ec1c-120">-ParentName</span></span>
<span data-ttu-id="2ec1c-121">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="2ec1c-121">The integration account name.</span></span>

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

### <span data-ttu-id="2ec1c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ec1c-122">-PassThru</span></span>
<span data-ttu-id="2ec1c-123">Gibt zurück, ob der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="2ec1c-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="2ec1c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ec1c-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ec1c-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2ec1c-125">The resource group name.</span></span>

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

### <span data-ttu-id="2ec1c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ec1c-126">-ResourceId</span></span>
<span data-ttu-id="2ec1c-127">Die Ressourcen-ID der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="2ec1c-127">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="2ec1c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ec1c-128">-Confirm</span></span>
<span data-ttu-id="2ec1c-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ec1c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ec1c-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2ec1c-130">-WhatIf</span></span>
<span data-ttu-id="2ec1c-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ec1c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ec1c-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ec1c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ec1c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec1c-133">CommonParameters</span></span>
<span data-ttu-id="2ec1c-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ec1c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec1c-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec1c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec1c-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2ec1c-136">INPUTS</span></span>

### <span data-ttu-id="2ec1c-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2ec1c-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="2ec1c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2ec1c-138">System.String</span></span>

## <span data-ttu-id="2ec1c-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2ec1c-139">OUTPUTS</span></span>

### <span data-ttu-id="2ec1c-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2ec1c-140">System.Boolean</span></span>

## <span data-ttu-id="2ec1c-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2ec1c-141">NOTES</span></span>

## <span data-ttu-id="2ec1c-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2ec1c-142">RELATED LINKS</span></span>
