---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
ms.openlocfilehash: 24400b7a2c882cef81d818c5f5b94fca4235ec83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650685"
---
# <span data-ttu-id="abb05-101">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="abb05-101">Get-AzMlOpCluster</span></span>

## <span data-ttu-id="abb05-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="abb05-102">SYNOPSIS</span></span>
<span data-ttu-id="abb05-103">Ruft ein Clusterobjekt für die Operation ab.</span><span class="sxs-lookup"><span data-stu-id="abb05-103">Gets an operationalization cluster object.</span></span>

## <span data-ttu-id="abb05-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="abb05-104">SYNTAX</span></span>

### <span data-ttu-id="abb05-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="abb05-105">GetByName</span></span>
```
Get-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="abb05-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="abb05-106">GetByResourceGroup</span></span>
```
Get-AzMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abb05-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="abb05-107">DESCRIPTION</span></span>
<span data-ttu-id="abb05-108">Ruft ein Clusterobjekt für die Operation nach Namen oder nach Ressourcengruppe oder nach Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="abb05-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="abb05-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="abb05-109">EXAMPLES</span></span>

### <span data-ttu-id="abb05-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="abb05-110">Example 1</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="abb05-111">Ruft einen bestimmten Zuordnungs Cluster nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="abb05-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="abb05-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="abb05-112">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="abb05-113">Ruft alle Operations Cluster in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="abb05-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="abb05-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="abb05-114">Example 3</span></span>
```
PS C:\> Get-AzMlOpCluster
```

<span data-ttu-id="abb05-115">Ruft alle Operations Cluster in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="abb05-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="abb05-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="abb05-116">PARAMETERS</span></span>

### <span data-ttu-id="abb05-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb05-117">-DefaultProfile</span></span>
<span data-ttu-id="abb05-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="abb05-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abb05-119">-Name</span><span class="sxs-lookup"><span data-stu-id="abb05-119">-Name</span></span>
<span data-ttu-id="abb05-120">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="abb05-120">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="abb05-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abb05-121">-ResourceGroupName</span></span>
<span data-ttu-id="abb05-122">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="abb05-122">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="abb05-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb05-123">CommonParameters</span></span>
<span data-ttu-id="abb05-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abb05-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb05-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abb05-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb05-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="abb05-126">INPUTS</span></span>

### <span data-ttu-id="abb05-127">Keine</span><span class="sxs-lookup"><span data-stu-id="abb05-127">None</span></span>

## <span data-ttu-id="abb05-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="abb05-128">OUTPUTS</span></span>

### <span data-ttu-id="abb05-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="abb05-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="abb05-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="abb05-130">NOTES</span></span>

## <span data-ttu-id="abb05-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="abb05-131">RELATED LINKS</span></span>
