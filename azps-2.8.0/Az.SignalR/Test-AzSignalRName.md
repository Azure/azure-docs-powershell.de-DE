---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: 21fbee422b898b5e5cf448f4a8f1913777268964
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823127"
---
# <span data-ttu-id="6c683-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="6c683-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="6c683-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c683-102">SYNOPSIS</span></span>
<span data-ttu-id="6c683-103">Überprüfen Sie die Verfügbarkeit eines Namens.</span><span class="sxs-lookup"><span data-stu-id="6c683-103">Check the availability of a name.</span></span> <span data-ttu-id="6c683-104">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="6c683-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="6c683-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c683-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c683-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c683-106">DESCRIPTION</span></span>
<span data-ttu-id="6c683-107">Überprüfen Sie die Verfügbarkeit eines Namens.</span><span class="sxs-lookup"><span data-stu-id="6c683-107">Check the availability of a name.</span></span> <span data-ttu-id="6c683-108">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="6c683-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="6c683-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c683-109">EXAMPLES</span></span>

### <span data-ttu-id="6c683-110">Überprüfen Sie einen vorhandenen Namen.</span><span class="sxs-lookup"><span data-stu-id="6c683-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="6c683-111">Überprüfen Sie einen nicht vorhandenen Namen.</span><span class="sxs-lookup"><span data-stu-id="6c683-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="6c683-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c683-112">PARAMETERS</span></span>

### <span data-ttu-id="6c683-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c683-113">-DefaultProfile</span></span>
<span data-ttu-id="6c683-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c683-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c683-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="6c683-115">-Location</span></span>
<span data-ttu-id="6c683-116">Der Signalisierungs Dienststandort.</span><span class="sxs-lookup"><span data-stu-id="6c683-116">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c683-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6c683-117">-Name</span></span>
<span data-ttu-id="6c683-118">Der Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="6c683-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="6c683-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c683-119">CommonParameters</span></span>
<span data-ttu-id="6c683-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c683-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c683-121">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c683-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c683-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c683-122">INPUTS</span></span>

### <span data-ttu-id="6c683-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6c683-123">System.String</span></span>

## <span data-ttu-id="6c683-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c683-124">OUTPUTS</span></span>

### <span data-ttu-id="6c683-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c683-125">System.Boolean</span></span>

## <span data-ttu-id="6c683-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c683-126">NOTES</span></span>

## <span data-ttu-id="6c683-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c683-127">RELATED LINKS</span></span>
