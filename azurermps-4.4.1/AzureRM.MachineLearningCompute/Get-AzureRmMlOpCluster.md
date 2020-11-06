---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: e37aff4f6f79a3aa0420c98811bc47b951bb4d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500830"
---
# <span data-ttu-id="c1de3-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="c1de3-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="c1de3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1de3-102">SYNOPSIS</span></span>
<span data-ttu-id="c1de3-103">Ruft ein Clusterobjekt für die Operation ab.</span><span class="sxs-lookup"><span data-stu-id="c1de3-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1de3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1de3-104">SYNTAX</span></span>

```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1de3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1de3-105">DESCRIPTION</span></span>
<span data-ttu-id="c1de3-106">Ruft ein Clusterobjekt für die Operation nach Namen oder nach Ressourcengruppe oder nach Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="c1de3-106">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="c1de3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1de3-107">EXAMPLES</span></span>

### <span data-ttu-id="c1de3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c1de3-108">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="c1de3-109">Ruft einen bestimmten Zuordnungs Cluster nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="c1de3-109">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="c1de3-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c1de3-110">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="c1de3-111">Ruft alle Operations Cluster in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="c1de3-111">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="c1de3-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c1de3-112">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="c1de3-113">Ruft alle Operations Cluster in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="c1de3-113">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="c1de3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1de3-114">PARAMETERS</span></span>

### <span data-ttu-id="c1de3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1de3-115">-DefaultProfile</span></span>
<span data-ttu-id="c1de3-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c1de3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1de3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c1de3-117">-Name</span></span>
<span data-ttu-id="c1de3-118">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="c1de3-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get an operationalization cluster by its name.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1de3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1de3-119">-ResourceGroupName</span></span>
<span data-ttu-id="c1de3-120">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="c1de3-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1de3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1de3-121">CommonParameters</span></span>
<span data-ttu-id="c1de3-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1de3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1de3-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1de3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1de3-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1de3-124">INPUTS</span></span>

### <span data-ttu-id="c1de3-125">Keine</span><span class="sxs-lookup"><span data-stu-id="c1de3-125">None</span></span>

## <span data-ttu-id="c1de3-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1de3-126">OUTPUTS</span></span>

### <span data-ttu-id="c1de3-127">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="c1de3-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="c1de3-128">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster, Microsoft. Azure. Commands. MachineLearningCompute, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c1de3-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c1de3-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1de3-129">NOTES</span></span>

## <span data-ttu-id="c1de3-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1de3-130">RELATED LINKS</span></span>

