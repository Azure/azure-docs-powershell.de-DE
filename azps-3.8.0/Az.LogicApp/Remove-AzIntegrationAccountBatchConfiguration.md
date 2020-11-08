---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 848ce0e0c5608271f1f8facb955aad2df95b6a0a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996086"
---
# <span data-ttu-id="0c23b-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c23b-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="0c23b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c23b-102">SYNOPSIS</span></span>
<span data-ttu-id="0c23b-103">Entfernt eine Integration Account-batchkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0c23b-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="0c23b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c23b-104">SYNTAX</span></span>

### <span data-ttu-id="0c23b-105">ByIntegrationAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="0c23b-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c23b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0c23b-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c23b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0c23b-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c23b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c23b-108">DESCRIPTION</span></span>
<span data-ttu-id="0c23b-109">Das Cmdlet **Remove-AzIntegrationAccountBatchConfiguration** entfernt eine batchkonfiguration aus einem Integrations Konto.</span><span class="sxs-lookup"><span data-stu-id="0c23b-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="0c23b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c23b-110">EXAMPLES</span></span>

### <span data-ttu-id="0c23b-111">Beispiel 1: Entfernen einer batchkonfiguration nach Parametern</span><span class="sxs-lookup"><span data-stu-id="0c23b-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="0c23b-112">Entfernt die batchkonfiguration mit dem Namen "sampleBatchConfig", die sich im Integrations Konto "sampleIntegrationAccount" befindet.</span><span class="sxs-lookup"><span data-stu-id="0c23b-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="0c23b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c23b-113">PARAMETERS</span></span>

### <span data-ttu-id="0c23b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c23b-114">-DefaultProfile</span></span>
<span data-ttu-id="0c23b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0c23b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c23b-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0c23b-116">-InputObject</span></span>
<span data-ttu-id="0c23b-117">Eine batchkonfiguration für das Integrations Konto.</span><span class="sxs-lookup"><span data-stu-id="0c23b-117">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="0c23b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0c23b-118">-Name</span></span>
<span data-ttu-id="0c23b-119">Der Konfigurationsname des Integrations Konto-Batches.</span><span class="sxs-lookup"><span data-stu-id="0c23b-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="0c23b-120">-Übergeordneter</span><span class="sxs-lookup"><span data-stu-id="0c23b-120">-ParentName</span></span>
<span data-ttu-id="0c23b-121">Der Name des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="0c23b-121">The integration account name.</span></span>

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

### <span data-ttu-id="0c23b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c23b-122">-PassThru</span></span>
<span data-ttu-id="0c23b-123">Gibt zurück, ob der Befehl erfolgreich war oder nicht.</span><span class="sxs-lookup"><span data-stu-id="0c23b-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="0c23b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c23b-124">-ResourceGroupName</span></span>
<span data-ttu-id="0c23b-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0c23b-125">The resource group name.</span></span>

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

### <span data-ttu-id="0c23b-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0c23b-126">-ResourceId</span></span>
<span data-ttu-id="0c23b-127">Die Ressourcen-ID der Integrations Konto-batchkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0c23b-127">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="0c23b-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0c23b-128">-Confirm</span></span>
<span data-ttu-id="0c23b-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0c23b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c23b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c23b-130">-WhatIf</span></span>
<span data-ttu-id="0c23b-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c23b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c23b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c23b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c23b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c23b-133">CommonParameters</span></span>
<span data-ttu-id="0c23b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c23b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c23b-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c23b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c23b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c23b-136">INPUTS</span></span>

### <span data-ttu-id="0c23b-137">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c23b-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="0c23b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0c23b-138">System.String</span></span>

## <span data-ttu-id="0c23b-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c23b-139">OUTPUTS</span></span>

### <span data-ttu-id="0c23b-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c23b-140">System.Boolean</span></span>

## <span data-ttu-id="0c23b-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c23b-141">NOTES</span></span>

## <span data-ttu-id="0c23b-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c23b-142">RELATED LINKS</span></span>
