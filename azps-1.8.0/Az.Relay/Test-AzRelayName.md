---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 796f241ebd554647f22e3c5216807e1644c9d769
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659689"
---
# <span data-ttu-id="cc58a-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="cc58a-101">Test-AzRelayName</span></span>

## <span data-ttu-id="cc58a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc58a-102">SYNOPSIS</span></span>
<span data-ttu-id="cc58a-103">Überprüft die Verfügbarkeit des angegebenen Namespace namens.</span><span class="sxs-lookup"><span data-stu-id="cc58a-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="cc58a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc58a-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc58a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc58a-105">DESCRIPTION</span></span>
<span data-ttu-id="cc58a-106">Das Cmdlet " **Test-AzRelayName** " Überprüfen der Verfügbarkeit des Namespace namens</span><span class="sxs-lookup"><span data-stu-id="cc58a-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="cc58a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc58a-107">EXAMPLES</span></span>

### <span data-ttu-id="cc58a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc58a-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="cc58a-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cc58a-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="cc58a-110">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="cc58a-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="cc58a-111">Gibt den Status der Verfügbarkeit des Namespacenamens zurück</span><span class="sxs-lookup"><span data-stu-id="cc58a-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="cc58a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc58a-112">PARAMETERS</span></span>

### <span data-ttu-id="cc58a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc58a-113">-DefaultProfile</span></span>
<span data-ttu-id="cc58a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc58a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc58a-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cc58a-115">-Namespace</span></span>
<span data-ttu-id="cc58a-116">Name des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="cc58a-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="cc58a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc58a-117">CommonParameters</span></span>
<span data-ttu-id="cc58a-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc58a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc58a-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc58a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc58a-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc58a-120">INPUTS</span></span>

### <span data-ttu-id="cc58a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="cc58a-121">System.String</span></span>

## <span data-ttu-id="cc58a-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc58a-122">OUTPUTS</span></span>

### <span data-ttu-id="cc58a-123">Microsoft. Azure. Commands. Relay. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="cc58a-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="cc58a-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc58a-124">NOTES</span></span>

## <span data-ttu-id="cc58a-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc58a-125">RELATED LINKS</span></span>
