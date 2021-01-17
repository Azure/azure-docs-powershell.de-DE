---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 43e2ae9426d80b7762fb8afe7b9c57a53a232f8a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303003"
---
# <span data-ttu-id="20940-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="20940-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="20940-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20940-102">SYNOPSIS</span></span>
<span data-ttu-id="20940-103">Erhalten Sie die Details der Clusterressourcen.</span><span class="sxs-lookup"><span data-stu-id="20940-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="20940-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20940-104">SYNTAX</span></span>

### <span data-ttu-id="20940-105">BySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="20940-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20940-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="20940-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20940-107">ByName</span><span class="sxs-lookup"><span data-stu-id="20940-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20940-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20940-108">DESCRIPTION</span></span>
<span data-ttu-id="20940-109">Vom **Get-AzServiceFabricCluster** werden die Clusterressourcendetails angezeigt.</span><span class="sxs-lookup"><span data-stu-id="20940-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="20940-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="20940-110">EXAMPLES</span></span>

### <span data-ttu-id="20940-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20940-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="20940-112">Mit diesem Befehl werden die Clusterressourcendetails für den Cluster "myCluster" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="20940-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="20940-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20940-113">PARAMETERS</span></span>

### <span data-ttu-id="20940-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20940-114">-DefaultProfile</span></span>
<span data-ttu-id="20940-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20940-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20940-116">-Name</span><span class="sxs-lookup"><span data-stu-id="20940-116">-Name</span></span>
<span data-ttu-id="20940-117">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="20940-117">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20940-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20940-118">-ResourceGroupName</span></span>
<span data-ttu-id="20940-119">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="20940-119">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20940-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20940-120">CommonParameters</span></span>
<span data-ttu-id="20940-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20940-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20940-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20940-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20940-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="20940-123">INPUTS</span></span>

### <span data-ttu-id="20940-124">System.String</span><span class="sxs-lookup"><span data-stu-id="20940-124">System.String</span></span>

## <span data-ttu-id="20940-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="20940-125">OUTPUTS</span></span>

### <span data-ttu-id="20940-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="20940-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="20940-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="20940-127">NOTES</span></span>

## <span data-ttu-id="20940-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="20940-128">RELATED LINKS</span></span>
