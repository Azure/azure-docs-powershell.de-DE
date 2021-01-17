---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 45c3e0a4271a5eb2527ff25b5858a3f5aa35dc0a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372055"
---
# <span data-ttu-id="eb7ed-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="eb7ed-101">Test-AzRelayName</span></span>

## <span data-ttu-id="eb7ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb7ed-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7ed-103">Überprüft die Verfügbarkeit des angegebenen NameSpacenamens.</span><span class="sxs-lookup"><span data-stu-id="eb7ed-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="eb7ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb7ed-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb7ed-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb7ed-105">DESCRIPTION</span></span>
<span data-ttu-id="eb7ed-106">Mit **dem Cmdlet "Test-AzRelayName"** wird die Verfügbarkeit des NameSpacenamens überprüft.</span><span class="sxs-lookup"><span data-stu-id="eb7ed-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="eb7ed-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eb7ed-107">EXAMPLES</span></span>

### <span data-ttu-id="eb7ed-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eb7ed-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="eb7ed-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="eb7ed-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="eb7ed-110">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="eb7ed-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="eb7ed-111">Gibt den Status der Verfügbarkeit des Namespacenamens zurück.</span><span class="sxs-lookup"><span data-stu-id="eb7ed-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="eb7ed-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb7ed-112">PARAMETERS</span></span>

### <span data-ttu-id="eb7ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb7ed-113">-DefaultProfile</span></span>
<span data-ttu-id="eb7ed-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb7ed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb7ed-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eb7ed-115">-Namespace</span></span>
<span data-ttu-id="eb7ed-116">Namespacename des Relays.</span><span class="sxs-lookup"><span data-stu-id="eb7ed-116">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7ed-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7ed-117">CommonParameters</span></span>
<span data-ttu-id="eb7ed-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb7ed-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7ed-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb7ed-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7ed-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eb7ed-120">INPUTS</span></span>

### <span data-ttu-id="eb7ed-121">System.String</span><span class="sxs-lookup"><span data-stu-id="eb7ed-121">System.String</span></span>

## <span data-ttu-id="eb7ed-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eb7ed-122">OUTPUTS</span></span>

### <span data-ttu-id="eb7ed-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="eb7ed-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="eb7ed-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="eb7ed-124">NOTES</span></span>

## <span data-ttu-id="eb7ed-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="eb7ed-125">RELATED LINKS</span></span>
