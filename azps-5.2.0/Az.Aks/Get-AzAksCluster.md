---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299443"
---
# <span data-ttu-id="e95fe-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="e95fe-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="e95fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e95fe-102">SYNOPSIS</span></span>
<span data-ttu-id="e95fe-103">Von Kubernetes verwaltete Cluster auflisten.</span><span class="sxs-lookup"><span data-stu-id="e95fe-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="e95fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e95fe-104">SYNTAX</span></span>

### <span data-ttu-id="e95fe-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e95fe-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e95fe-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95fe-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95fe-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95fe-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e95fe-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e95fe-108">DESCRIPTION</span></span>
<span data-ttu-id="e95fe-109">Von Kubernetes verwaltete Cluster auflisten.</span><span class="sxs-lookup"><span data-stu-id="e95fe-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="e95fe-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e95fe-110">EXAMPLES</span></span>

### <span data-ttu-id="e95fe-111">Alle Kubernetes-Cluster auflisten</span><span class="sxs-lookup"><span data-stu-id="e95fe-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="e95fe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e95fe-112">PARAMETERS</span></span>

### <span data-ttu-id="e95fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95fe-113">-DefaultProfile</span></span>
<span data-ttu-id="e95fe-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e95fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e95fe-115">-ID</span><span class="sxs-lookup"><span data-stu-id="e95fe-115">-Id</span></span>
<span data-ttu-id="e95fe-116">ID eines verwalteten Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="e95fe-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="e95fe-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e95fe-117">-Name</span></span>
<span data-ttu-id="e95fe-118">Name des verwalteten Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="e95fe-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="e95fe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e95fe-119">-ResourceGroupName</span></span>
<span data-ttu-id="e95fe-120">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="e95fe-120">Resource group name</span></span>

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

### <span data-ttu-id="e95fe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95fe-121">CommonParameters</span></span>
<span data-ttu-id="e95fe-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e95fe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95fe-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e95fe-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95fe-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e95fe-124">INPUTS</span></span>

### <span data-ttu-id="e95fe-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e95fe-125">System.String</span></span>

## <span data-ttu-id="e95fe-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e95fe-126">OUTPUTS</span></span>

### <span data-ttu-id="e95fe-127">Microsoft.Azure.Commands.Aks.Models.PSAkiernetesCluster</span><span class="sxs-lookup"><span data-stu-id="e95fe-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="e95fe-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e95fe-128">NOTES</span></span>

## <span data-ttu-id="e95fe-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e95fe-129">RELATED LINKS</span></span>
