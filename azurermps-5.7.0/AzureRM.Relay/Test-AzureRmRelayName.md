---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: adf7c4b7f8d80e16b49d9d55b742a55279232a07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498870"
---
# <span data-ttu-id="744a2-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="744a2-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="744a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="744a2-102">SYNOPSIS</span></span>
<span data-ttu-id="744a2-103">Überprüft die Verfügbarkeit des angegebenen Namespace namens.</span><span class="sxs-lookup"><span data-stu-id="744a2-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="744a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="744a2-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="744a2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="744a2-105">DESCRIPTION</span></span>
<span data-ttu-id="744a2-106">Das Cmdlet " **Test-AzureRmRelayName** " Überprüfen der Verfügbarkeit des Namespace namens</span><span class="sxs-lookup"><span data-stu-id="744a2-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="744a2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="744a2-107">EXAMPLES</span></span>

### <span data-ttu-id="744a2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="744a2-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### <span data-ttu-id="744a2-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="744a2-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### <span data-ttu-id="744a2-110">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="744a2-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

<span data-ttu-id="744a2-111">Gibt den Status der Verfügbarkeit des Namespacenamens zurück</span><span class="sxs-lookup"><span data-stu-id="744a2-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="744a2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="744a2-112">PARAMETERS</span></span>

### <span data-ttu-id="744a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="744a2-113">-DefaultProfile</span></span>
<span data-ttu-id="744a2-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="744a2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="744a2-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="744a2-115">-Namespace</span></span>
<span data-ttu-id="744a2-116">Name des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="744a2-116">Relay Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744a2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744a2-117">CommonParameters</span></span>
<span data-ttu-id="744a2-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="744a2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744a2-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="744a2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744a2-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="744a2-120">INPUTS</span></span>

### <span data-ttu-id="744a2-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="744a2-121">-Namespace</span></span>
 <span data-ttu-id="744a2-122">System. String</span><span class="sxs-lookup"><span data-stu-id="744a2-122">System.String</span></span>

## <span data-ttu-id="744a2-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="744a2-123">OUTPUTS</span></span>

### <span data-ttu-id="744a2-124">[Microsoft. Azure. Commands. Relay. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="744a2-124">[Microsoft.Azure.Commands.Relay.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="744a2-125">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="744a2-125">Example 1</span></span>
<span data-ttu-id="744a2-126">NameAvailable-Grund Nachricht</span><span class="sxs-lookup"><span data-stu-id="744a2-126">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="744a2-127">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="744a2-127">Example 2</span></span>
<span data-ttu-id="744a2-128">NameAvailable-Grund Nachricht</span><span class="sxs-lookup"><span data-stu-id="744a2-128">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="744a2-129">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="744a2-129">Example 3</span></span>
<span data-ttu-id="744a2-130">NameAvailable-Grund Nachricht</span><span class="sxs-lookup"><span data-stu-id="744a2-130">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="744a2-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="744a2-131">NOTES</span></span>

## <span data-ttu-id="744a2-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="744a2-132">RELATED LINKS</span></span>

