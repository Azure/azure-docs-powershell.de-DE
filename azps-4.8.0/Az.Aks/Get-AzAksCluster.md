---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173620"
---
# <span data-ttu-id="6977f-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="6977f-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="6977f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6977f-102">SYNOPSIS</span></span>
<span data-ttu-id="6977f-103">Liste Kubernetes verwalteter Cluster</span><span class="sxs-lookup"><span data-stu-id="6977f-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="6977f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6977f-104">SYNTAX</span></span>

### <span data-ttu-id="6977f-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6977f-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6977f-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6977f-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6977f-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6977f-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6977f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6977f-108">DESCRIPTION</span></span>
<span data-ttu-id="6977f-109">Liste Kubernetes verwalteter Cluster</span><span class="sxs-lookup"><span data-stu-id="6977f-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="6977f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6977f-110">EXAMPLES</span></span>

### <span data-ttu-id="6977f-111">Auflisten aller Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="6977f-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="6977f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6977f-112">PARAMETERS</span></span>

### <span data-ttu-id="6977f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6977f-113">-DefaultProfile</span></span>
<span data-ttu-id="6977f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6977f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6977f-115">-ID</span><span class="sxs-lookup"><span data-stu-id="6977f-115">-Id</span></span>
<span data-ttu-id="6977f-116">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="6977f-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="6977f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6977f-117">-Name</span></span>
<span data-ttu-id="6977f-118">Name Ihres verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="6977f-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="6977f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6977f-119">-ResourceGroupName</span></span>
<span data-ttu-id="6977f-120">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="6977f-120">Resource group name</span></span>

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

### <span data-ttu-id="6977f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6977f-121">CommonParameters</span></span>
<span data-ttu-id="6977f-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6977f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6977f-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6977f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6977f-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6977f-124">INPUTS</span></span>

### <span data-ttu-id="6977f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6977f-125">System.String</span></span>

## <span data-ttu-id="6977f-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6977f-126">OUTPUTS</span></span>

### <span data-ttu-id="6977f-127">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="6977f-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="6977f-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="6977f-128">NOTES</span></span>

## <span data-ttu-id="6977f-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6977f-129">RELATED LINKS</span></span>
