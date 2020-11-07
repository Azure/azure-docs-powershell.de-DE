---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/test-azmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: d05f8b746dbd212c834e3554639340fa6075c216
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650658"
---
# <span data-ttu-id="73c2d-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="73c2d-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="73c2d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="73c2d-103">Überprüft, ob Updates für die Systemdienste verfügbar sind, die mit einem Operations Cluster verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="73c2d-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

## <span data-ttu-id="73c2d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="73c2d-104">SYNTAX</span></span>

### <span data-ttu-id="73c2d-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="73c2d-105">TestByNameAndResourceGroup</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73c2d-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="73c2d-106">TestByInputObject</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73c2d-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="73c2d-107">TestByResourceId</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73c2d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73c2d-108">DESCRIPTION</span></span>
<span data-ttu-id="73c2d-109">System Dienste erhalten Updates unabhängig vom Operations Cluster.</span><span class="sxs-lookup"><span data-stu-id="73c2d-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="73c2d-110">Wenn Sie dieses Cmdlet verwenden, kann der Benutzer wissen, ob Invoke-AzMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="73c2d-110">Using this cmdlet will let the user know if Invoke-AzMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="73c2d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73c2d-111">EXAMPLES</span></span>

### <span data-ttu-id="73c2d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="73c2d-112">Example 1</span></span>
```
PS C:\> Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="73c2d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="73c2d-113">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="73c2d-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="73c2d-114">Example 3</span></span>
```
PS C:\> Find-AzResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="73c2d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="73c2d-115">PARAMETERS</span></span>

### <span data-ttu-id="73c2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73c2d-116">-DefaultProfile</span></span>
<span data-ttu-id="73c2d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="73c2d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73c2d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="73c2d-118">-InputObject</span></span>
<span data-ttu-id="73c2d-119">Das Clusterobjekt für die Operation</span><span class="sxs-lookup"><span data-stu-id="73c2d-119">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: TestByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73c2d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="73c2d-120">-Name</span></span>
<span data-ttu-id="73c2d-121">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="73c2d-121">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c2d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73c2d-122">-ResourceGroupName</span></span>
<span data-ttu-id="73c2d-123">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="73c2d-123">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c2d-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="73c2d-124">-ResourceId</span></span>
<span data-ttu-id="73c2d-125">Die Azure-Ressourcen-ID für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="73c2d-125">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73c2d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c2d-126">CommonParameters</span></span>
<span data-ttu-id="73c2d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73c2d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c2d-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73c2d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c2d-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73c2d-129">INPUTS</span></span>

### <span data-ttu-id="73c2d-130">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="73c2d-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="73c2d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="73c2d-131">System.String</span></span>

## <span data-ttu-id="73c2d-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73c2d-132">OUTPUTS</span></span>

### <span data-ttu-id="73c2d-133">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="73c2d-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="73c2d-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="73c2d-134">NOTES</span></span>

## <span data-ttu-id="73c2d-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73c2d-135">RELATED LINKS</span></span>
