---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 26a2e414f05fc0aeb209afa946ae168c59ea4ff8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846011"
---
# <span data-ttu-id="d1bd5-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1bd5-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="d1bd5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="d1bd5-103">Ruft eine batchkonfiguration für das Integrations Konto ab.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="d1bd5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1bd5-104">SYNTAX</span></span>

### <span data-ttu-id="d1bd5-105">ByIntegrationAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1bd5-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1bd5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d1bd5-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1bd5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1bd5-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1bd5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1bd5-108">DESCRIPTION</span></span>
<span data-ttu-id="d1bd5-109">Das Cmdlet " **Get-AzIntegrationAccountBatchConfiguration** " Ruft eine batchkonfiguration von einem Integrations Konto ab.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="d1bd5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1bd5-110">EXAMPLES</span></span>

### <span data-ttu-id="d1bd5-111">Beispiel 1: Abrufen einer batchkonfiguration nach Parametern</span><span class="sxs-lookup"><span data-stu-id="d1bd5-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="d1bd5-112">Rufen Sie eine batchkonfiguration mit dem Namen "sampleBatchConfig" ab, die sich im Integrations Konto "sampleIntegrationAccount" befindet, das in der Ressourcengruppe "sampleResourceGroup" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="d1bd5-113">Beispiel 2: Auflisten aller Batch Konfigurationen in einem Integrations Konto nach Parametern</span><span class="sxs-lookup"><span data-stu-id="d1bd5-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
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

<span data-ttu-id="d1bd5-114">Rufen Sie alle Batch Konfigurationen ab, die sich im Integrations Konto "sampleIntegrationAccount" befinden, das in der Ressourcengruppe "sampleResourceGroup" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="d1bd5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1bd5-115">PARAMETERS</span></span>

### <span data-ttu-id="d1bd5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1bd5-116">-DefaultProfile</span></span>
<span data-ttu-id="d1bd5-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1bd5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d1bd5-118">-Name</span></span>
<span data-ttu-id="d1bd5-119">Der Konfigurationsname des Integrations Konto-Batches.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="d1bd5-120">-Übergeordneter</span><span class="sxs-lookup"><span data-stu-id="d1bd5-120">-ParentName</span></span>
<span data-ttu-id="d1bd5-121">Der Name des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-121">The integration account name.</span></span>

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

### <span data-ttu-id="d1bd5-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d1bd5-122">-ParentObject</span></span>
<span data-ttu-id="d1bd5-123">Ein Integrations Kontoobjekt.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-123">An integration account object.</span></span>

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

### <span data-ttu-id="d1bd5-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d1bd5-124">-ParentResourceId</span></span>
<span data-ttu-id="d1bd5-125">Die Ressourcen-ID des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="d1bd5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1bd5-126">-ResourceGroupName</span></span>
<span data-ttu-id="d1bd5-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-127">The resource group name.</span></span>

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

### <span data-ttu-id="d1bd5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1bd5-128">CommonParameters</span></span>
<span data-ttu-id="d1bd5-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1bd5-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1bd5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1bd5-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1bd5-131">INPUTS</span></span>

### <span data-ttu-id="d1bd5-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d1bd5-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="d1bd5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d1bd5-133">System.String</span></span>

## <span data-ttu-id="d1bd5-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1bd5-134">OUTPUTS</span></span>

### <span data-ttu-id="d1bd5-135">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1bd5-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="d1bd5-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1bd5-136">NOTES</span></span>

## <span data-ttu-id="d1bd5-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1bd5-137">RELATED LINKS</span></span>
