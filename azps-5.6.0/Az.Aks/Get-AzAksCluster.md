---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: 50d4dc8531f28ebb50ef562321b3974c7b50a102
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926083"
---
# <span data-ttu-id="f3bc9-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="f3bc9-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="f3bc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="f3bc9-103">Listen Sie verwaltete Kubernetes-Cluster auf.</span><span class="sxs-lookup"><span data-stu-id="f3bc9-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="f3bc9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3bc9-104">SYNTAX</span></span>

### <span data-ttu-id="f3bc9-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f3bc9-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3bc9-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3bc9-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3bc9-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3bc9-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3bc9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3bc9-108">DESCRIPTION</span></span>
<span data-ttu-id="f3bc9-109">Listen Sie verwaltete Kubernetes-Cluster auf.</span><span class="sxs-lookup"><span data-stu-id="f3bc9-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="f3bc9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f3bc9-110">EXAMPLES</span></span>

### <span data-ttu-id="f3bc9-111">Auflisten aller Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="f3bc9-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="f3bc9-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f3bc9-112">PARAMETERS</span></span>

### <span data-ttu-id="f3bc9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3bc9-113">-DefaultProfile</span></span>
<span data-ttu-id="f3bc9-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3bc9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3bc9-115">-ID</span><span class="sxs-lookup"><span data-stu-id="f3bc9-115">-Id</span></span>
<span data-ttu-id="f3bc9-116">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="f3bc9-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3bc9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f3bc9-117">-Name</span></span>
<span data-ttu-id="f3bc9-118">Name Des verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="f3bc9-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bc9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3bc9-119">-ResourceGroupName</span></span>
<span data-ttu-id="f3bc9-120">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f3bc9-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bc9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3bc9-121">CommonParameters</span></span>
<span data-ttu-id="f3bc9-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3bc9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3bc9-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3bc9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3bc9-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f3bc9-124">INPUTS</span></span>

### <span data-ttu-id="f3bc9-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f3bc9-125">System.String</span></span>

## <span data-ttu-id="f3bc9-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f3bc9-126">OUTPUTS</span></span>

### <span data-ttu-id="f3bc9-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="f3bc9-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="f3bc9-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f3bc9-128">NOTES</span></span>

## <span data-ttu-id="f3bc9-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f3bc9-129">RELATED LINKS</span></span>
