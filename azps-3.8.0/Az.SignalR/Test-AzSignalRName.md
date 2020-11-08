---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995985"
---
# <span data-ttu-id="12a02-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="12a02-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="12a02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12a02-102">SYNOPSIS</span></span>
<span data-ttu-id="12a02-103">Überprüfen Sie die Verfügbarkeit eines Namens.</span><span class="sxs-lookup"><span data-stu-id="12a02-103">Check the availability of a name.</span></span> <span data-ttu-id="12a02-104">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="12a02-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="12a02-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="12a02-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12a02-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12a02-106">DESCRIPTION</span></span>
<span data-ttu-id="12a02-107">Überprüfen Sie die Verfügbarkeit eines Namens.</span><span class="sxs-lookup"><span data-stu-id="12a02-107">Check the availability of a name.</span></span> <span data-ttu-id="12a02-108">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="12a02-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="12a02-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12a02-109">EXAMPLES</span></span>

### <span data-ttu-id="12a02-110">Überprüfen Sie einen vorhandenen Namen.</span><span class="sxs-lookup"><span data-stu-id="12a02-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="12a02-111">Überprüfen Sie einen nicht vorhandenen Namen.</span><span class="sxs-lookup"><span data-stu-id="12a02-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="12a02-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="12a02-112">PARAMETERS</span></span>

### <span data-ttu-id="12a02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a02-113">-DefaultProfile</span></span>
<span data-ttu-id="12a02-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12a02-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12a02-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="12a02-115">-Location</span></span>
<span data-ttu-id="12a02-116">Der Signalisierungs Dienststandort.</span><span class="sxs-lookup"><span data-stu-id="12a02-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="12a02-117">-Name</span><span class="sxs-lookup"><span data-stu-id="12a02-117">-Name</span></span>
<span data-ttu-id="12a02-118">Der Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="12a02-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="12a02-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a02-119">CommonParameters</span></span>
<span data-ttu-id="12a02-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a02-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a02-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12a02-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a02-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12a02-122">INPUTS</span></span>

### <span data-ttu-id="12a02-123">System. String</span><span class="sxs-lookup"><span data-stu-id="12a02-123">System.String</span></span>

## <span data-ttu-id="12a02-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12a02-124">OUTPUTS</span></span>

### <span data-ttu-id="12a02-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12a02-125">System.Boolean</span></span>

## <span data-ttu-id="12a02-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="12a02-126">NOTES</span></span>

## <span data-ttu-id="12a02-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12a02-127">RELATED LINKS</span></span>
