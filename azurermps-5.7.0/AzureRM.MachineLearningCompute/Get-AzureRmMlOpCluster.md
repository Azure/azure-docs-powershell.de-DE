---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: 0e9eecf16a26be5367df5d8ad8b45a40e0050da3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662846"
---
# <span data-ttu-id="34d27-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="34d27-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="34d27-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34d27-102">SYNOPSIS</span></span>
<span data-ttu-id="34d27-103">Ruft ein Clusterobjekt für die Operation ab.</span><span class="sxs-lookup"><span data-stu-id="34d27-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34d27-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34d27-104">SYNTAX</span></span>

### <span data-ttu-id="34d27-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="34d27-105">GetByName</span></span>
```
Get-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="34d27-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="34d27-106">GetByResourceGroup</span></span>
```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34d27-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34d27-107">DESCRIPTION</span></span>
<span data-ttu-id="34d27-108">Ruft ein Clusterobjekt für die Operation nach Namen oder nach Ressourcengruppe oder nach Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="34d27-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="34d27-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34d27-109">EXAMPLES</span></span>

### <span data-ttu-id="34d27-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="34d27-110">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="34d27-111">Ruft einen bestimmten Zuordnungs Cluster nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="34d27-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="34d27-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="34d27-112">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="34d27-113">Ruft alle Operations Cluster in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="34d27-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="34d27-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="34d27-114">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="34d27-115">Ruft alle Operations Cluster in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="34d27-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="34d27-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="34d27-116">PARAMETERS</span></span>

### <span data-ttu-id="34d27-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d27-117">-DefaultProfile</span></span>
<span data-ttu-id="34d27-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34d27-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34d27-119">-Name</span><span class="sxs-lookup"><span data-stu-id="34d27-119">-Name</span></span>
<span data-ttu-id="34d27-120">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="34d27-120">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d27-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34d27-121">-ResourceGroupName</span></span>
<span data-ttu-id="34d27-122">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="34d27-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d27-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d27-123">CommonParameters</span></span>
<span data-ttu-id="34d27-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34d27-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d27-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34d27-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d27-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34d27-126">INPUTS</span></span>

### <span data-ttu-id="34d27-127">Keine</span><span class="sxs-lookup"><span data-stu-id="34d27-127">None</span></span>

## <span data-ttu-id="34d27-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34d27-128">OUTPUTS</span></span>

### <span data-ttu-id="34d27-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="34d27-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="34d27-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster, Microsoft. Azure. Commands. MachineLearningCompute, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="34d27-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="34d27-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="34d27-131">NOTES</span></span>

## <span data-ttu-id="34d27-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34d27-132">RELATED LINKS</span></span>

