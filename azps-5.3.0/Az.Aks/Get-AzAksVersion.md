---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471565"
---
# <span data-ttu-id="38397-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="38397-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="38397-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38397-102">SYNOPSIS</span></span>
<span data-ttu-id="38397-103">Listet die verfügbaren Versionen zum Erstellen eines verwalteten Kubernetes-Cluster auf.</span><span class="sxs-lookup"><span data-stu-id="38397-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="38397-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38397-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38397-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38397-105">DESCRIPTION</span></span>
<span data-ttu-id="38397-106">Listet die verfügbaren Versionen zum Erstellen eines verwalteten Kubernetes-Cluster auf.</span><span class="sxs-lookup"><span data-stu-id="38397-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="38397-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38397-107">EXAMPLES</span></span>

### <span data-ttu-id="38397-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="38397-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="38397-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38397-109">PARAMETERS</span></span>

### <span data-ttu-id="38397-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38397-110">-DefaultProfile</span></span>
<span data-ttu-id="38397-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38397-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38397-112">-Location</span><span class="sxs-lookup"><span data-stu-id="38397-112">-Location</span></span>
<span data-ttu-id="38397-113">Azure-Standort für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="38397-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="38397-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38397-114">CommonParameters</span></span>
<span data-ttu-id="38397-115">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38397-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38397-116">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38397-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38397-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38397-117">INPUTS</span></span>

### <span data-ttu-id="38397-118">Keine</span><span class="sxs-lookup"><span data-stu-id="38397-118">None</span></span>

## <span data-ttu-id="38397-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38397-119">OUTPUTS</span></span>

### <span data-ttu-id="38397-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="38397-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="38397-121">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="38397-121">NOTES</span></span>

## <span data-ttu-id="38397-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="38397-122">RELATED LINKS</span></span>
