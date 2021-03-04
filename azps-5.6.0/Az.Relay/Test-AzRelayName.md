---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: be0b0f2aa9aa45fa69b3d57051a5671a76186abc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943714"
---
# <span data-ttu-id="6d62d-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="6d62d-101">Test-AzRelayName</span></span>

## <span data-ttu-id="6d62d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d62d-102">SYNOPSIS</span></span>
<span data-ttu-id="6d62d-103">Überprüft die Verfügbarkeit des angegebenen NameSpace-Namens</span><span class="sxs-lookup"><span data-stu-id="6d62d-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="6d62d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d62d-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d62d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d62d-105">DESCRIPTION</span></span>
<span data-ttu-id="6d62d-106">Das **Test-AzRelayName-Cmdlet** "Verfügbarkeit des NameSpace-Namens überprüfen"</span><span class="sxs-lookup"><span data-stu-id="6d62d-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="6d62d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6d62d-107">EXAMPLES</span></span>

### <span data-ttu-id="6d62d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6d62d-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="6d62d-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6d62d-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="6d62d-110">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="6d62d-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="6d62d-111">Gibt den Status für die Verfügbarkeit des Namespacenamens zurück.</span><span class="sxs-lookup"><span data-stu-id="6d62d-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="6d62d-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6d62d-112">PARAMETERS</span></span>

### <span data-ttu-id="6d62d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d62d-113">-DefaultProfile</span></span>
<span data-ttu-id="6d62d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d62d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d62d-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6d62d-115">-Namespace</span></span>
<span data-ttu-id="6d62d-116">Name des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="6d62d-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="6d62d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d62d-117">CommonParameters</span></span>
<span data-ttu-id="6d62d-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d62d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d62d-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d62d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d62d-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6d62d-120">INPUTS</span></span>

### <span data-ttu-id="6d62d-121">System.String</span><span class="sxs-lookup"><span data-stu-id="6d62d-121">System.String</span></span>

## <span data-ttu-id="6d62d-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6d62d-122">OUTPUTS</span></span>

### <span data-ttu-id="6d62d-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="6d62d-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="6d62d-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6d62d-124">NOTES</span></span>

## <span data-ttu-id="6d62d-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6d62d-125">RELATED LINKS</span></span>
