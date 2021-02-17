---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156268"
---
# <span data-ttu-id="260ff-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="260ff-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="260ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="260ff-102">SYNOPSIS</span></span>
<span data-ttu-id="260ff-103">Holen Sie sich das Nutzungskontingent eines Abonnements.</span><span class="sxs-lookup"><span data-stu-id="260ff-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="260ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="260ff-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="260ff-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="260ff-105">DESCRIPTION</span></span>
<span data-ttu-id="260ff-106">Holen Sie sich das Nutzungskontingent eines Abonnements.</span><span class="sxs-lookup"><span data-stu-id="260ff-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="260ff-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="260ff-107">EXAMPLES</span></span>

### <span data-ttu-id="260ff-108">Holen Sie sich das Nutzungskontingent, indem Sie den Standort eingeben.</span><span class="sxs-lookup"><span data-stu-id="260ff-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="260ff-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="260ff-109">PARAMETERS</span></span>

### <span data-ttu-id="260ff-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="260ff-110">-DefaultProfile</span></span>
<span data-ttu-id="260ff-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="260ff-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="260ff-112">-Location</span><span class="sxs-lookup"><span data-stu-id="260ff-112">-Location</span></span>
<span data-ttu-id="260ff-113">Der Standort des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="260ff-113">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260ff-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="260ff-114">CommonParameters</span></span>
<span data-ttu-id="260ff-115">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="260ff-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="260ff-116">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="260ff-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="260ff-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="260ff-117">INPUTS</span></span>

### <span data-ttu-id="260ff-118">Keine</span><span class="sxs-lookup"><span data-stu-id="260ff-118">None</span></span>

## <span data-ttu-id="260ff-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="260ff-119">OUTPUTS</span></span>

### <span data-ttu-id="260ff-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="260ff-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="260ff-121">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="260ff-121">NOTES</span></span>

## <span data-ttu-id="260ff-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="260ff-122">RELATED LINKS</span></span>
