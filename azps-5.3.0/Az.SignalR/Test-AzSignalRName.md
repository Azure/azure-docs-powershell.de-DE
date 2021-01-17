---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468524"
---
# <span data-ttu-id="39302-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="39302-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="39302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39302-102">SYNOPSIS</span></span>
<span data-ttu-id="39302-103">Überprüfen Sie die Verfügbarkeit eines Namens.</span><span class="sxs-lookup"><span data-stu-id="39302-103">Check the availability of a name.</span></span> <span data-ttu-id="39302-104">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="39302-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="39302-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39302-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39302-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39302-106">DESCRIPTION</span></span>
<span data-ttu-id="39302-107">Überprüfen Sie die Verfügbarkeit eines Namens.</span><span class="sxs-lookup"><span data-stu-id="39302-107">Check the availability of a name.</span></span> <span data-ttu-id="39302-108">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="39302-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="39302-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39302-109">EXAMPLES</span></span>

### <span data-ttu-id="39302-110">Überprüfen Sie einen vorhandenen Namen.</span><span class="sxs-lookup"><span data-stu-id="39302-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="39302-111">Überprüfen Sie einen nicht vorhandenen Namen.</span><span class="sxs-lookup"><span data-stu-id="39302-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="39302-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39302-112">PARAMETERS</span></span>

### <span data-ttu-id="39302-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39302-113">-DefaultProfile</span></span>
<span data-ttu-id="39302-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39302-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39302-115">-Location</span><span class="sxs-lookup"><span data-stu-id="39302-115">-Location</span></span>
<span data-ttu-id="39302-116">Der Standort des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="39302-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="39302-117">-Name</span><span class="sxs-lookup"><span data-stu-id="39302-117">-Name</span></span>
<span data-ttu-id="39302-118">Der Name des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="39302-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="39302-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39302-119">CommonParameters</span></span>
<span data-ttu-id="39302-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39302-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39302-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39302-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39302-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39302-122">INPUTS</span></span>

### <span data-ttu-id="39302-123">System.String</span><span class="sxs-lookup"><span data-stu-id="39302-123">System.String</span></span>

## <span data-ttu-id="39302-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39302-124">OUTPUTS</span></span>

### <span data-ttu-id="39302-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39302-125">System.Boolean</span></span>

## <span data-ttu-id="39302-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="39302-126">NOTES</span></span>

## <span data-ttu-id="39302-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="39302-127">RELATED LINKS</span></span>
