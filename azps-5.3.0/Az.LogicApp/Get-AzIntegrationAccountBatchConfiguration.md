---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 26a2e414f05fc0aeb209afa946ae168c59ea4ff8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472323"
---
# <span data-ttu-id="5170c-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5170c-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="5170c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5170c-102">SYNOPSIS</span></span>
<span data-ttu-id="5170c-103">Ruft die Batchkonfiguration eines Integrationskontos ab.</span><span class="sxs-lookup"><span data-stu-id="5170c-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="5170c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5170c-104">SYNTAX</span></span>

### <span data-ttu-id="5170c-105">ByIntegrationAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="5170c-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5170c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5170c-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5170c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5170c-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5170c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5170c-108">DESCRIPTION</span></span>
<span data-ttu-id="5170c-109">Das **Cmdlet "Get-AzIntegrationAccountBatchConfiguration"** ruft eine Batchkonfiguration aus einem Integrationskonto ab.</span><span class="sxs-lookup"><span data-stu-id="5170c-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="5170c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5170c-110">EXAMPLES</span></span>

### <span data-ttu-id="5170c-111">Beispiel 1: Erhalten einer Batchkonfiguration nach Parametern</span><span class="sxs-lookup"><span data-stu-id="5170c-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="5170c-112">Erhalten Sie eine Batchkonfiguration namens "sampleBatchConfig" im Integrationskonto "sampleIntegrationAccount", das in der Ressourcengruppe "sampleResourceGroup" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5170c-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="5170c-113">Beispiel 2: Auflisten aller Batchkonfigurationen in einem Integrationskonto nach Parametern</span><span class="sxs-lookup"><span data-stu-id="5170c-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig2
Name       : sampleBatchConfig2
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="5170c-114">Erhalten Sie alle Batchkonfigurationen im Integrationskonto "sampleIntegrationAccount", das in der Ressourcengruppe "sampleResourceGroup" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5170c-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="5170c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5170c-115">PARAMETERS</span></span>

### <span data-ttu-id="5170c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5170c-116">-DefaultProfile</span></span>
<span data-ttu-id="5170c-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5170c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5170c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5170c-118">-Name</span></span>
<span data-ttu-id="5170c-119">Der Name der Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="5170c-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5170c-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="5170c-120">-ParentName</span></span>
<span data-ttu-id="5170c-121">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="5170c-121">The integration account name.</span></span>

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

### <span data-ttu-id="5170c-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5170c-122">-ParentObject</span></span>
<span data-ttu-id="5170c-123">Ein Integrationskontoobjekt.</span><span class="sxs-lookup"><span data-stu-id="5170c-123">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5170c-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5170c-124">-ParentResourceId</span></span>
<span data-ttu-id="5170c-125">Die Ressourcen-ID des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="5170c-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="5170c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5170c-126">-ResourceGroupName</span></span>
<span data-ttu-id="5170c-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5170c-127">The resource group name.</span></span>

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

### <span data-ttu-id="5170c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5170c-128">CommonParameters</span></span>
<span data-ttu-id="5170c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5170c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5170c-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5170c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5170c-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5170c-131">INPUTS</span></span>

### <span data-ttu-id="5170c-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="5170c-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="5170c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5170c-133">System.String</span></span>

## <span data-ttu-id="5170c-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5170c-134">OUTPUTS</span></span>

### <span data-ttu-id="5170c-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5170c-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="5170c-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5170c-136">NOTES</span></span>

## <span data-ttu-id="5170c-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5170c-137">RELATED LINKS</span></span>
