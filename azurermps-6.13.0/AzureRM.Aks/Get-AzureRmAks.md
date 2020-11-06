---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/get-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
ms.openlocfilehash: d30d9858a3050864f5cc86601adf6b598be8c54d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501270"
---
# <span data-ttu-id="bea07-101">Get-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="bea07-101">Get-AzureRmAks</span></span>

## <span data-ttu-id="bea07-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bea07-102">SYNOPSIS</span></span>
<span data-ttu-id="bea07-103">Liste Kubernetes verwalteter Cluster</span><span class="sxs-lookup"><span data-stu-id="bea07-103">List Kubernetes managed clusters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bea07-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bea07-104">SYNTAX</span></span>

### <span data-ttu-id="bea07-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bea07-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bea07-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bea07-106">IdParameterSet</span></span>
```
Get-AzureRmAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bea07-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bea07-107">NameParameterSet</span></span>
```
Get-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bea07-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bea07-108">DESCRIPTION</span></span>
<span data-ttu-id="bea07-109">Liste Kubernetes verwalteter Cluster</span><span class="sxs-lookup"><span data-stu-id="bea07-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="bea07-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bea07-110">EXAMPLES</span></span>

### <span data-ttu-id="bea07-111">Auflisten aller Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="bea07-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzureRmAks
```

## <span data-ttu-id="bea07-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bea07-112">PARAMETERS</span></span>

### <span data-ttu-id="bea07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea07-113">-DefaultProfile</span></span>
<span data-ttu-id="bea07-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bea07-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea07-115">-ID</span><span class="sxs-lookup"><span data-stu-id="bea07-115">-Id</span></span>
<span data-ttu-id="bea07-116">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="bea07-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="bea07-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bea07-117">-Name</span></span>
<span data-ttu-id="bea07-118">Name Ihres verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="bea07-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="bea07-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea07-119">-ResourceGroupName</span></span>
<span data-ttu-id="bea07-120">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="bea07-120">Resource group name</span></span>

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

### <span data-ttu-id="bea07-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea07-121">CommonParameters</span></span>
<span data-ttu-id="bea07-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bea07-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea07-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bea07-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea07-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bea07-124">INPUTS</span></span>

### <span data-ttu-id="bea07-125">System. String</span><span class="sxs-lookup"><span data-stu-id="bea07-125">System.String</span></span>

## <span data-ttu-id="bea07-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bea07-126">OUTPUTS</span></span>

### <span data-ttu-id="bea07-127">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="bea07-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="bea07-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="bea07-128">NOTES</span></span>

## <span data-ttu-id="bea07-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bea07-129">RELATED LINKS</span></span>
