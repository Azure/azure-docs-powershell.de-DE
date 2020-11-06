---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: cdf8c04a3d3b3b9fc50e571642bc14352d976b84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500545"
---
# <span data-ttu-id="973bc-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="973bc-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="973bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="973bc-102">SYNOPSIS</span></span>
<span data-ttu-id="973bc-103">Ruft die Zugriffstasten ab, die einem Operations Cluster zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="973bc-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="973bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="973bc-104">SYNTAX</span></span>

### <span data-ttu-id="973bc-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="973bc-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="973bc-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="973bc-106">GetByInputObject</span></span>
```
Get-AzureRmMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="973bc-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="973bc-107">GetByResourceId</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="973bc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="973bc-108">DESCRIPTION</span></span>
<span data-ttu-id="973bc-109">Die Schlüssel für das Speicherkonto, die Container Registrierung und andere Dienste, die dem Zuordnungs Cluster zugeordnet sind, werden beim Abrufen der Clustereigenschaften nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="973bc-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="973bc-110">Ein bestimmter Aufruf zum Abrufen der Schlüssel muss vorgenommen werden, da es sich um vertrauliche Informationen handelt.</span><span class="sxs-lookup"><span data-stu-id="973bc-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="973bc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="973bc-111">EXAMPLES</span></span>

### <span data-ttu-id="973bc-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="973bc-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="973bc-113">Gibt die geheimen Schlüssel für die Dienste zurück, die dem Cluster für die Operation zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="973bc-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="973bc-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="973bc-114">PARAMETERS</span></span>

### <span data-ttu-id="973bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="973bc-115">-DefaultProfile</span></span>
<span data-ttu-id="973bc-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="973bc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="973bc-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="973bc-117">-InputObject</span></span>
<span data-ttu-id="973bc-118">Das Clusterobjekt für die Operation</span><span class="sxs-lookup"><span data-stu-id="973bc-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: GetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="973bc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="973bc-119">-Name</span></span>
<span data-ttu-id="973bc-120">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="973bc-120">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="973bc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="973bc-121">-ResourceGroupName</span></span>
<span data-ttu-id="973bc-122">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="973bc-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="973bc-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="973bc-123">-ResourceId</span></span>
<span data-ttu-id="973bc-124">Die Azure-Ressourcen-ID für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="973bc-124">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="973bc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="973bc-125">CommonParameters</span></span>
<span data-ttu-id="973bc-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="973bc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="973bc-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="973bc-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="973bc-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="973bc-128">INPUTS</span></span>

### <span data-ttu-id="973bc-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="973bc-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="973bc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="973bc-130">System.String</span></span>

## <span data-ttu-id="973bc-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="973bc-131">OUTPUTS</span></span>

### <span data-ttu-id="973bc-132">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="973bc-132">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="973bc-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="973bc-133">NOTES</span></span>

## <span data-ttu-id="973bc-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="973bc-134">RELATED LINKS</span></span>

