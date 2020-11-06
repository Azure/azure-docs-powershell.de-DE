---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: 396243e366f6a21e2ac94d105473b348c6a8198d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501085"
---
# <span data-ttu-id="d90e3-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="d90e3-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="d90e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d90e3-102">SYNOPSIS</span></span>
<span data-ttu-id="d90e3-103">Überprüft die Verfügbarkeit des angegebenen Namespace namens.</span><span class="sxs-lookup"><span data-stu-id="d90e3-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d90e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d90e3-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d90e3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d90e3-105">DESCRIPTION</span></span>
<span data-ttu-id="d90e3-106">Das Cmdlet " **Test-AzureRmRelayName** " Überprüfen der Verfügbarkeit des Namespace namens</span><span class="sxs-lookup"><span data-stu-id="d90e3-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="d90e3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d90e3-107">EXAMPLES</span></span>

### <span data-ttu-id="d90e3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d90e3-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="d90e3-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d90e3-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="d90e3-110">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d90e3-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="d90e3-111">Gibt den Status der Verfügbarkeit des Namespacenamens zurück</span><span class="sxs-lookup"><span data-stu-id="d90e3-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="d90e3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d90e3-112">PARAMETERS</span></span>

### <span data-ttu-id="d90e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d90e3-113">-DefaultProfile</span></span>
<span data-ttu-id="d90e3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d90e3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d90e3-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d90e3-115">-Namespace</span></span>
<span data-ttu-id="d90e3-116">Name des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="d90e3-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="d90e3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d90e3-117">CommonParameters</span></span>
<span data-ttu-id="d90e3-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d90e3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d90e3-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d90e3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d90e3-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d90e3-120">INPUTS</span></span>

### <span data-ttu-id="d90e3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d90e3-121">System.String</span></span>


## <span data-ttu-id="d90e3-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d90e3-122">OUTPUTS</span></span>

### <span data-ttu-id="d90e3-123">Microsoft. Azure. Commands. Relay. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="d90e3-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="d90e3-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="d90e3-124">NOTES</span></span>

## <span data-ttu-id="d90e3-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d90e3-125">RELATED LINKS</span></span>
