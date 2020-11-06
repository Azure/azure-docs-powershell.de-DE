---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: 746dde8dd3460add5eb6a20e4a9b771873dac0e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495998"
---
# <span data-ttu-id="54915-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="54915-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="54915-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54915-102">SYNOPSIS</span></span>
<span data-ttu-id="54915-103">Ruft ein Clusterobjekt für die Operation ab.</span><span class="sxs-lookup"><span data-stu-id="54915-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54915-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54915-104">SYNTAX</span></span>

### <span data-ttu-id="54915-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="54915-105">GetByName</span></span>
```
Get-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54915-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="54915-106">GetByResourceGroup</span></span>
```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54915-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54915-107">DESCRIPTION</span></span>
<span data-ttu-id="54915-108">Ruft ein Clusterobjekt für die Operation nach Namen oder nach Ressourcengruppe oder nach Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="54915-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="54915-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54915-109">EXAMPLES</span></span>

### <span data-ttu-id="54915-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54915-110">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="54915-111">Ruft einen bestimmten Zuordnungs Cluster nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="54915-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="54915-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="54915-112">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="54915-113">Ruft alle Operations Cluster in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="54915-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="54915-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="54915-114">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="54915-115">Ruft alle Operations Cluster in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="54915-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="54915-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="54915-116">PARAMETERS</span></span>

### <span data-ttu-id="54915-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54915-117">-DefaultProfile</span></span>
<span data-ttu-id="54915-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="54915-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54915-119">-Name</span><span class="sxs-lookup"><span data-stu-id="54915-119">-Name</span></span>
<span data-ttu-id="54915-120">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="54915-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54915-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54915-121">-ResourceGroupName</span></span>
<span data-ttu-id="54915-122">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="54915-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54915-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54915-123">CommonParameters</span></span>
<span data-ttu-id="54915-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54915-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54915-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54915-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54915-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54915-126">INPUTS</span></span>

### <span data-ttu-id="54915-127">Keine</span><span class="sxs-lookup"><span data-stu-id="54915-127">None</span></span>

## <span data-ttu-id="54915-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54915-128">OUTPUTS</span></span>

### <span data-ttu-id="54915-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="54915-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="54915-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="54915-130">NOTES</span></span>

## <span data-ttu-id="54915-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54915-131">RELATED LINKS</span></span>
