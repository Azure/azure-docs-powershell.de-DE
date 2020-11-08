---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177321"
---
# <span data-ttu-id="9b85f-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="9b85f-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="9b85f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9b85f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b85f-103">Liste der verfügbaren Versionen zum Erstellen eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="9b85f-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="9b85f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b85f-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b85f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b85f-105">DESCRIPTION</span></span>
<span data-ttu-id="9b85f-106">Liste der verfügbaren Versionen zum Erstellen eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="9b85f-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="9b85f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b85f-107">EXAMPLES</span></span>

### <span data-ttu-id="9b85f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9b85f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="9b85f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b85f-109">PARAMETERS</span></span>

### <span data-ttu-id="9b85f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b85f-110">-DefaultProfile</span></span>
<span data-ttu-id="9b85f-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9b85f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b85f-112">-Standort</span><span class="sxs-lookup"><span data-stu-id="9b85f-112">-Location</span></span>
<span data-ttu-id="9b85f-113">Azure-Speicherort für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="9b85f-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="9b85f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b85f-114">CommonParameters</span></span>
<span data-ttu-id="9b85f-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b85f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b85f-116">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b85f-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b85f-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9b85f-117">INPUTS</span></span>

### <span data-ttu-id="9b85f-118">Keine</span><span class="sxs-lookup"><span data-stu-id="9b85f-118">None</span></span>

## <span data-ttu-id="9b85f-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9b85f-119">OUTPUTS</span></span>

### <span data-ttu-id="9b85f-120">Microsoft. Azure. Commands. AKS. Models. PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="9b85f-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="9b85f-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="9b85f-121">NOTES</span></span>

## <span data-ttu-id="9b85f-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9b85f-122">RELATED LINKS</span></span>
