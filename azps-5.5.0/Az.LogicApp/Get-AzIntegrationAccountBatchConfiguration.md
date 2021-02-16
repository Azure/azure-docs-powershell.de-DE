---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 26a2e414f05fc0aeb209afa946ae168c59ea4ff8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170406"
---
# <span data-ttu-id="1fbf0-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fbf0-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="1fbf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fbf0-102">SYNOPSIS</span></span>
<span data-ttu-id="1fbf0-103">Ruft die Batchkonfiguration eines Integrationskontos ab.</span><span class="sxs-lookup"><span data-stu-id="1fbf0-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="1fbf0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fbf0-104">SYNTAX</span></span>

### <span data-ttu-id="1fbf0-105">ByIntegrationAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="1fbf0-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fbf0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1fbf0-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fbf0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1fbf0-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fbf0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1fbf0-108">DESCRIPTION</span></span>
<span data-ttu-id="1fbf0-109">Das **Cmdlet "Get-AzIntegrationAccountBatchConfiguration"** ruft eine Batchkonfiguration aus einem Integrationskonto ab.</span><span class="sxs-lookup"><span data-stu-id="1fbf0-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="1fbf0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1fbf0-110">EXAMPLES</span></span>

### <span data-ttu-id="1fbf0-111">Beispiel 1: Erhalten einer Batchkonfiguration nach Parametern</span><span class="sxs-lookup"><span data-stu-id="1fbf0-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="1fbf0-112">Erhalten Sie eine Batchkonfiguration namens "sampleBatchConfig" im Integrationskonto "sampleIntegrationAccount", das in der Ressourcengruppe "sampleResourceGroup" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1fbf0-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="1fbf0-113">Beispiel 2: Auflisten aller Batchkonfigurationen in einem Integrationskonto nach Parametern</span><span class="sxs-lookup"><span data-stu-id="1fbf0-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
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

<span data-ttu-id="1fbf0-114">Erhalten Sie alle Batchkonfigurationen im Integrationskonto "sampleIntegrationAccount", das in der Ressourcengruppe "sampleResourceGroup" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1fbf0-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="1fbf0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fbf0-115">PARAMETERS</span></span>

### <span data-ttu-id="1fbf0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fbf0-116">-DefaultProfile</span></span>
<span data-ttu-id="1fbf0-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1fbf0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fbf0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1fbf0-118">-Name</span></span>
<span data-ttu-id="1fbf0-119">Der Name der Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="1fbf0-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="1fbf0-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="1fbf0-120">-ParentName</span></span>
<span data-ttu-id="1fbf0-121">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="1fbf0-121">The integration account name.</span></span>

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

### <span data-ttu-id="1fbf0-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1fbf0-122">-ParentObject</span></span>
<span data-ttu-id="1fbf0-123">Ein Integrationskontoobjekt.</span><span class="sxs-lookup"><span data-stu-id="1fbf0-123">An integration account object.</span></span>

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

### <span data-ttu-id="1fbf0-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1fbf0-124">-ParentResourceId</span></span>
<span data-ttu-id="1fbf0-125">Die Ressourcen-ID des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="1fbf0-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="1fbf0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fbf0-126">-ResourceGroupName</span></span>
<span data-ttu-id="1fbf0-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1fbf0-127">The resource group name.</span></span>

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

### <span data-ttu-id="1fbf0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fbf0-128">CommonParameters</span></span>
<span data-ttu-id="1fbf0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fbf0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fbf0-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fbf0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fbf0-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1fbf0-131">INPUTS</span></span>

### <span data-ttu-id="1fbf0-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1fbf0-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="1fbf0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1fbf0-133">System.String</span></span>

## <span data-ttu-id="1fbf0-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1fbf0-134">OUTPUTS</span></span>

### <span data-ttu-id="1fbf0-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fbf0-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="1fbf0-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1fbf0-136">NOTES</span></span>

## <span data-ttu-id="1fbf0-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1fbf0-137">RELATED LINKS</span></span>
