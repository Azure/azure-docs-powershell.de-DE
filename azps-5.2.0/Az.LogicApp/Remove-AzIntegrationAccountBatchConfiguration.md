---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 848ce0e0c5608271f1f8facb955aad2df95b6a0a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291550"
---
# <span data-ttu-id="cd2a5-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd2a5-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="cd2a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd2a5-102">SYNOPSIS</span></span>
<span data-ttu-id="cd2a5-103">Entfernt die Batchkonfiguration eines Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="cd2a5-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="cd2a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd2a5-104">SYNTAX</span></span>

### <span data-ttu-id="cd2a5-105">ByIntegrationAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="cd2a5-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd2a5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cd2a5-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd2a5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cd2a5-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd2a5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd2a5-108">DESCRIPTION</span></span>
<span data-ttu-id="cd2a5-109">Das **Cmdlet "Remove-AzIntegrationAccountBatchConfiguration"** entfernt eine Batchkonfiguration aus einem Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="cd2a5-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="cd2a5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cd2a5-110">EXAMPLES</span></span>

### <span data-ttu-id="cd2a5-111">Beispiel 1: Entfernen einer Batchkonfiguration nach Parametern</span><span class="sxs-lookup"><span data-stu-id="cd2a5-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="cd2a5-112">Entfernt die Batchkonfiguration mit dem Namen "sampleBatchConfig", die sich im Integrationskonto "sampleIntegrationAccount" befindet.</span><span class="sxs-lookup"><span data-stu-id="cd2a5-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="cd2a5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd2a5-113">PARAMETERS</span></span>

### <span data-ttu-id="cd2a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd2a5-114">-DefaultProfile</span></span>
<span data-ttu-id="cd2a5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd2a5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd2a5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd2a5-116">-InputObject</span></span>
<span data-ttu-id="cd2a5-117">Eine Batchkonfiguration für ein Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="cd2a5-117">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd2a5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cd2a5-118">-Name</span></span>
<span data-ttu-id="cd2a5-119">Der Name der Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="cd2a5-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd2a5-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="cd2a5-120">-ParentName</span></span>
<span data-ttu-id="cd2a5-121">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="cd2a5-121">The integration account name.</span></span>

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

### <span data-ttu-id="cd2a5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd2a5-122">-PassThru</span></span>
<span data-ttu-id="cd2a5-123">Gibt zurück, ob der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="cd2a5-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="cd2a5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd2a5-124">-ResourceGroupName</span></span>
<span data-ttu-id="cd2a5-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cd2a5-125">The resource group name.</span></span>

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

### <span data-ttu-id="cd2a5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd2a5-126">-ResourceId</span></span>
<span data-ttu-id="cd2a5-127">Die Konfigurationsressourcen-ID des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="cd2a5-127">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="cd2a5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd2a5-128">-Confirm</span></span>
<span data-ttu-id="cd2a5-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd2a5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd2a5-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cd2a5-130">-WhatIf</span></span>
<span data-ttu-id="cd2a5-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd2a5-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd2a5-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd2a5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd2a5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd2a5-133">CommonParameters</span></span>
<span data-ttu-id="cd2a5-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd2a5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd2a5-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd2a5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd2a5-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cd2a5-136">INPUTS</span></span>

### <span data-ttu-id="cd2a5-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd2a5-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="cd2a5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cd2a5-138">System.String</span></span>

## <span data-ttu-id="cd2a5-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cd2a5-139">OUTPUTS</span></span>

### <span data-ttu-id="cd2a5-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cd2a5-140">System.Boolean</span></span>

## <span data-ttu-id="cd2a5-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cd2a5-141">NOTES</span></span>

## <span data-ttu-id="cd2a5-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cd2a5-142">RELATED LINKS</span></span>
