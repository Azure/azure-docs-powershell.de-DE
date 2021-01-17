---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468535"
---
# <span data-ttu-id="ee506-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="ee506-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="ee506-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee506-102">SYNOPSIS</span></span>
<span data-ttu-id="ee506-103">Holen Sie sich das Nutzungskontingent eines Abonnements.</span><span class="sxs-lookup"><span data-stu-id="ee506-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="ee506-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee506-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee506-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee506-105">DESCRIPTION</span></span>
<span data-ttu-id="ee506-106">Holen Sie sich das Nutzungskontingent eines Abonnements.</span><span class="sxs-lookup"><span data-stu-id="ee506-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="ee506-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ee506-107">EXAMPLES</span></span>

### <span data-ttu-id="ee506-108">Verwenden des Nutzungskontingents durch Eingabe des Standorts</span><span class="sxs-lookup"><span data-stu-id="ee506-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="ee506-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee506-109">PARAMETERS</span></span>

### <span data-ttu-id="ee506-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee506-110">-DefaultProfile</span></span>
<span data-ttu-id="ee506-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ee506-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee506-112">-Location</span><span class="sxs-lookup"><span data-stu-id="ee506-112">-Location</span></span>
<span data-ttu-id="ee506-113">Der Standort des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="ee506-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="ee506-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee506-114">CommonParameters</span></span>
<span data-ttu-id="ee506-115">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee506-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee506-116">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee506-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee506-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ee506-117">INPUTS</span></span>

### <span data-ttu-id="ee506-118">Keine</span><span class="sxs-lookup"><span data-stu-id="ee506-118">None</span></span>

## <span data-ttu-id="ee506-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ee506-119">OUTPUTS</span></span>

### <span data-ttu-id="ee506-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="ee506-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="ee506-121">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ee506-121">NOTES</span></span>

## <span data-ttu-id="ee506-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ee506-122">RELATED LINKS</span></span>
