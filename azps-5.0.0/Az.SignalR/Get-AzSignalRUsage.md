---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296740"
---
# <span data-ttu-id="1676f-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="1676f-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="1676f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1676f-102">SYNOPSIS</span></span>
<span data-ttu-id="1676f-103">Abrufen des Nutzungs Kontingents eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="1676f-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="1676f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1676f-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1676f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1676f-105">DESCRIPTION</span></span>
<span data-ttu-id="1676f-106">Abrufen des Nutzungs Kontingents eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="1676f-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="1676f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1676f-107">EXAMPLES</span></span>

### <span data-ttu-id="1676f-108">Abrufen des Nutzungs Kontingents durch Eingabe des Speicherorts</span><span class="sxs-lookup"><span data-stu-id="1676f-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="1676f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1676f-109">PARAMETERS</span></span>

### <span data-ttu-id="1676f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1676f-110">-DefaultProfile</span></span>
<span data-ttu-id="1676f-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1676f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1676f-112">-Standort</span><span class="sxs-lookup"><span data-stu-id="1676f-112">-Location</span></span>
<span data-ttu-id="1676f-113">Der Signalisierungs Dienststandort.</span><span class="sxs-lookup"><span data-stu-id="1676f-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="1676f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1676f-114">CommonParameters</span></span>
<span data-ttu-id="1676f-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1676f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1676f-116">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1676f-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1676f-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1676f-117">INPUTS</span></span>

### <span data-ttu-id="1676f-118">Keine</span><span class="sxs-lookup"><span data-stu-id="1676f-118">None</span></span>

## <span data-ttu-id="1676f-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1676f-119">OUTPUTS</span></span>

### <span data-ttu-id="1676f-120">Microsoft. Azure. Commands. signalr. Models. PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="1676f-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="1676f-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="1676f-121">NOTES</span></span>

## <span data-ttu-id="1676f-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1676f-122">RELATED LINKS</span></span>
