---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995489"
---
# <span data-ttu-id="e66d8-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="e66d8-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="e66d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e66d8-102">SYNOPSIS</span></span>
<span data-ttu-id="e66d8-103">Abrufen des Nutzungs Kontingents eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="e66d8-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="e66d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e66d8-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e66d8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e66d8-105">DESCRIPTION</span></span>
<span data-ttu-id="e66d8-106">Abrufen des Nutzungs Kontingents eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="e66d8-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="e66d8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e66d8-107">EXAMPLES</span></span>

### <span data-ttu-id="e66d8-108">Abrufen des Nutzungs Kontingents durch Eingabe des Speicherorts</span><span class="sxs-lookup"><span data-stu-id="e66d8-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="e66d8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e66d8-109">PARAMETERS</span></span>

### <span data-ttu-id="e66d8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e66d8-110">-DefaultProfile</span></span>
<span data-ttu-id="e66d8-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e66d8-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e66d8-112">-Standort</span><span class="sxs-lookup"><span data-stu-id="e66d8-112">-Location</span></span>
<span data-ttu-id="e66d8-113">Der Signalisierungs Dienststandort.</span><span class="sxs-lookup"><span data-stu-id="e66d8-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="e66d8-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e66d8-114">CommonParameters</span></span>
<span data-ttu-id="e66d8-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e66d8-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e66d8-116">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e66d8-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e66d8-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e66d8-117">INPUTS</span></span>

### <span data-ttu-id="e66d8-118">Keine</span><span class="sxs-lookup"><span data-stu-id="e66d8-118">None</span></span>

## <span data-ttu-id="e66d8-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e66d8-119">OUTPUTS</span></span>

### <span data-ttu-id="e66d8-120">Microsoft. Azure. Commands. signalr. Models. PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="e66d8-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="e66d8-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="e66d8-121">NOTES</span></span>

## <span data-ttu-id="e66d8-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e66d8-122">RELATED LINKS</span></span>
