---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
ms.openlocfilehash: 34db847ba7a4051efab32a62c667d3d79ad4ac30
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658416"
---
# <span data-ttu-id="36823-101">Get-AzAks</span><span class="sxs-lookup"><span data-stu-id="36823-101">Get-AzAks</span></span>

## <span data-ttu-id="36823-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36823-102">SYNOPSIS</span></span>
<span data-ttu-id="36823-103">Liste Kubernetes verwalteter Cluster</span><span class="sxs-lookup"><span data-stu-id="36823-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="36823-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36823-104">SYNTAX</span></span>

### <span data-ttu-id="36823-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="36823-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36823-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36823-106">IdParameterSet</span></span>
```
Get-AzAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36823-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="36823-107">NameParameterSet</span></span>
```
Get-AzAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36823-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36823-108">DESCRIPTION</span></span>
<span data-ttu-id="36823-109">Liste Kubernetes verwalteter Cluster</span><span class="sxs-lookup"><span data-stu-id="36823-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="36823-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36823-110">EXAMPLES</span></span>

### <span data-ttu-id="36823-111">Auflisten aller Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="36823-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzAks
```

## <span data-ttu-id="36823-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="36823-112">PARAMETERS</span></span>

### <span data-ttu-id="36823-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36823-113">-DefaultProfile</span></span>
<span data-ttu-id="36823-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36823-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36823-115">-ID</span><span class="sxs-lookup"><span data-stu-id="36823-115">-Id</span></span>
<span data-ttu-id="36823-116">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="36823-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="36823-117">-Name</span><span class="sxs-lookup"><span data-stu-id="36823-117">-Name</span></span>
<span data-ttu-id="36823-118">Name Ihres verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="36823-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="36823-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36823-119">-ResourceGroupName</span></span>
<span data-ttu-id="36823-120">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="36823-120">Resource group name</span></span>

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

### <span data-ttu-id="36823-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36823-121">CommonParameters</span></span>
<span data-ttu-id="36823-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36823-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36823-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36823-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36823-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36823-124">INPUTS</span></span>

### <span data-ttu-id="36823-125">System. String</span><span class="sxs-lookup"><span data-stu-id="36823-125">System.String</span></span>

## <span data-ttu-id="36823-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36823-126">OUTPUTS</span></span>

### <span data-ttu-id="36823-127">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="36823-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="36823-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="36823-128">NOTES</span></span>

## <span data-ttu-id="36823-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36823-129">RELATED LINKS</span></span>
