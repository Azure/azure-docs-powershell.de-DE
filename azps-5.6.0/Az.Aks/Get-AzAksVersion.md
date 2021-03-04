---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 3a46f28ad0f169f4f4f280922dff675b5e749fed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926064"
---
# <span data-ttu-id="54199-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="54199-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="54199-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54199-102">SYNOPSIS</span></span>
<span data-ttu-id="54199-103">Liste der verfügbaren Version zum Erstellen eines verwalteten Kubernetes-Clusters auf.</span><span class="sxs-lookup"><span data-stu-id="54199-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="54199-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54199-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54199-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54199-105">DESCRIPTION</span></span>
<span data-ttu-id="54199-106">Liste der verfügbaren Version zum Erstellen eines verwalteten Kubernetes-Clusters auf.</span><span class="sxs-lookup"><span data-stu-id="54199-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="54199-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54199-107">EXAMPLES</span></span>

### <span data-ttu-id="54199-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54199-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="54199-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="54199-109">PARAMETERS</span></span>

### <span data-ttu-id="54199-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54199-110">-DefaultProfile</span></span>
<span data-ttu-id="54199-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54199-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54199-112">-Location</span><span class="sxs-lookup"><span data-stu-id="54199-112">-Location</span></span>
<span data-ttu-id="54199-113">Azure-Speicherort für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="54199-113">Azure location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54199-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54199-114">CommonParameters</span></span>
<span data-ttu-id="54199-115">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54199-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54199-116">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54199-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54199-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54199-117">INPUTS</span></span>

### <span data-ttu-id="54199-118">Keine</span><span class="sxs-lookup"><span data-stu-id="54199-118">None</span></span>

## <span data-ttu-id="54199-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54199-119">OUTPUTS</span></span>

### <span data-ttu-id="54199-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="54199-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="54199-121">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="54199-121">NOTES</span></span>

## <span data-ttu-id="54199-122">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="54199-122">RELATED LINKS</span></span>
