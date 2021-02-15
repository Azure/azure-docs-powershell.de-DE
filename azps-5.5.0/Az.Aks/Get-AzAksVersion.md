---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167097"
---
# <span data-ttu-id="ef61c-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="ef61c-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="ef61c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef61c-102">SYNOPSIS</span></span>
<span data-ttu-id="ef61c-103">Listet die verfügbaren Versionen zum Erstellen eines verwalteten Kubernetes-Cluster auf.</span><span class="sxs-lookup"><span data-stu-id="ef61c-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="ef61c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef61c-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef61c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef61c-105">DESCRIPTION</span></span>
<span data-ttu-id="ef61c-106">Listet die verfügbaren Versionen zum Erstellen eines verwalteten Kubernetes-Cluster auf.</span><span class="sxs-lookup"><span data-stu-id="ef61c-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="ef61c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ef61c-107">EXAMPLES</span></span>

### <span data-ttu-id="ef61c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ef61c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="ef61c-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef61c-109">PARAMETERS</span></span>

### <span data-ttu-id="ef61c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef61c-110">-DefaultProfile</span></span>
<span data-ttu-id="ef61c-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef61c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef61c-112">-Location</span><span class="sxs-lookup"><span data-stu-id="ef61c-112">-Location</span></span>
<span data-ttu-id="ef61c-113">Azure-Standort für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="ef61c-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="ef61c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef61c-114">CommonParameters</span></span>
<span data-ttu-id="ef61c-115">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef61c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef61c-116">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef61c-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef61c-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ef61c-117">INPUTS</span></span>

### <span data-ttu-id="ef61c-118">Keine</span><span class="sxs-lookup"><span data-stu-id="ef61c-118">None</span></span>

## <span data-ttu-id="ef61c-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ef61c-119">OUTPUTS</span></span>

### <span data-ttu-id="ef61c-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="ef61c-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="ef61c-121">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ef61c-121">NOTES</span></span>

## <span data-ttu-id="ef61c-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ef61c-122">RELATED LINKS</span></span>
