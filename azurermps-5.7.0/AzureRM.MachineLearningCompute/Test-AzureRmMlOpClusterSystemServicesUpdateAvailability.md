---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/test-azurermmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 9f531b67d2dc3cc6010a7677c96dc4ecf10fb5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496498"
---
# <span data-ttu-id="53ef8-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="53ef8-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="53ef8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53ef8-102">SYNOPSIS</span></span>
<span data-ttu-id="53ef8-103">Überprüft, ob Updates für die Systemdienste verfügbar sind, die mit einem Operations Cluster verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="53ef8-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53ef8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53ef8-104">SYNTAX</span></span>

### <span data-ttu-id="53ef8-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="53ef8-105">TestByNameAndResourceGroup</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53ef8-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="53ef8-106">TestByInputObject</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53ef8-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="53ef8-107">TestByResourceId</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53ef8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53ef8-108">DESCRIPTION</span></span>
<span data-ttu-id="53ef8-109">System Dienste erhalten Updates unabhängig vom Operations Cluster.</span><span class="sxs-lookup"><span data-stu-id="53ef8-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="53ef8-110">Wenn Sie dieses Cmdlet verwenden, kann der Benutzer wissen, ob Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="53ef8-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="53ef8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53ef8-111">EXAMPLES</span></span>

### <span data-ttu-id="53ef8-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53ef8-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="53ef8-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="53ef8-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="53ef8-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="53ef8-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="53ef8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="53ef8-115">PARAMETERS</span></span>

### <span data-ttu-id="53ef8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53ef8-116">-DefaultProfile</span></span>
<span data-ttu-id="53ef8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="53ef8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53ef8-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="53ef8-118">-InputObject</span></span>
<span data-ttu-id="53ef8-119">Das Clusterobjekt für die Operation</span><span class="sxs-lookup"><span data-stu-id="53ef8-119">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: TestByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53ef8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="53ef8-120">-Name</span></span>
<span data-ttu-id="53ef8-121">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="53ef8-121">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: TestByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53ef8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53ef8-122">-ResourceGroupName</span></span>
<span data-ttu-id="53ef8-123">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="53ef8-123">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: TestByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53ef8-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="53ef8-124">-ResourceId</span></span>
<span data-ttu-id="53ef8-125">Die Azure-Ressourcen-ID für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="53ef8-125">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ef8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53ef8-126">CommonParameters</span></span>
<span data-ttu-id="53ef8-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53ef8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53ef8-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53ef8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53ef8-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53ef8-129">INPUTS</span></span>

### <span data-ttu-id="53ef8-130">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="53ef8-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="53ef8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="53ef8-131">System.String</span></span>

## <span data-ttu-id="53ef8-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53ef8-132">OUTPUTS</span></span>

### <span data-ttu-id="53ef8-133">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="53ef8-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="53ef8-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="53ef8-134">NOTES</span></span>

## <span data-ttu-id="53ef8-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53ef8-135">RELATED LINKS</span></span>

