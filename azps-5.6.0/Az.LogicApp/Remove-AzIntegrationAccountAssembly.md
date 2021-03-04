---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: d1c61a611b3e2a90c1aa0b0cd21eebdff99ed04b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925544"
---
# <span data-ttu-id="46294-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="46294-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="46294-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46294-102">SYNOPSIS</span></span>
<span data-ttu-id="46294-103">Entfernt eine Integrationskonto assembly.</span><span class="sxs-lookup"><span data-stu-id="46294-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="46294-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46294-104">SYNTAX</span></span>

### <span data-ttu-id="46294-105">ByIntegrationAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="46294-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46294-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="46294-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46294-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="46294-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46294-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46294-108">DESCRIPTION</span></span>
<span data-ttu-id="46294-109">Das **Cmdlet Remove-AzIntegrationAccountAssembly** entfernt eine Assembly aus einem Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="46294-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="46294-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="46294-110">EXAMPLES</span></span>

### <span data-ttu-id="46294-111">Beispiel 1: Entfernen einer Assembly nach Parametern</span><span class="sxs-lookup"><span data-stu-id="46294-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="46294-112">Entfernt die Assembly mit dem Namen "sampleAssembly" im Integrationskonto "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="46294-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="46294-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="46294-113">PARAMETERS</span></span>

### <span data-ttu-id="46294-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46294-114">-DefaultProfile</span></span>
<span data-ttu-id="46294-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46294-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46294-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46294-116">-InputObject</span></span>
<span data-ttu-id="46294-117">Eine Integrationskonto assembly.</span><span class="sxs-lookup"><span data-stu-id="46294-117">An integration account assembly.</span></span>

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

### <span data-ttu-id="46294-118">-Name</span><span class="sxs-lookup"><span data-stu-id="46294-118">-Name</span></span>
<span data-ttu-id="46294-119">Der Assemblyname des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="46294-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="46294-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="46294-120">-ParentName</span></span>
<span data-ttu-id="46294-121">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="46294-121">The integration account name.</span></span>

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

### <span data-ttu-id="46294-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46294-122">-PassThru</span></span>
<span data-ttu-id="46294-123">Geben Sie zurück, ob der Befehl erfolgreich war oder nicht.</span><span class="sxs-lookup"><span data-stu-id="46294-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="46294-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46294-124">-ResourceGroupName</span></span>
<span data-ttu-id="46294-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="46294-125">The resource group name.</span></span>

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

### <span data-ttu-id="46294-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46294-126">-ResourceId</span></span>
<span data-ttu-id="46294-127">Die Ressourcen-ID der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="46294-127">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="46294-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46294-128">-Confirm</span></span>
<span data-ttu-id="46294-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46294-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46294-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46294-130">-WhatIf</span></span>
<span data-ttu-id="46294-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46294-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46294-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46294-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46294-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46294-133">CommonParameters</span></span>
<span data-ttu-id="46294-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46294-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46294-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46294-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46294-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="46294-136">INPUTS</span></span>

### <span data-ttu-id="46294-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="46294-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="46294-138">System.String</span><span class="sxs-lookup"><span data-stu-id="46294-138">System.String</span></span>

## <span data-ttu-id="46294-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="46294-139">OUTPUTS</span></span>

### <span data-ttu-id="46294-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="46294-140">System.Boolean</span></span>

## <span data-ttu-id="46294-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="46294-141">NOTES</span></span>

## <span data-ttu-id="46294-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="46294-142">RELATED LINKS</span></span>
