---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664431"
---
# <span data-ttu-id="e30d5-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="e30d5-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="e30d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e30d5-102">SYNOPSIS</span></span>
<span data-ttu-id="e30d5-103">Überprüft die Verfügbarkeit des angegebenen Namespace namens.</span><span class="sxs-lookup"><span data-stu-id="e30d5-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e30d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e30d5-104">SYNTAX</span></span>

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## <span data-ttu-id="e30d5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e30d5-105">DESCRIPTION</span></span>
<span data-ttu-id="e30d5-106">Das Cmdlet " **Test-AzureRmServiceBusName** " Überprüfen der Verfügbarkeit des Namespace namens</span><span class="sxs-lookup"><span data-stu-id="e30d5-106">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="e30d5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e30d5-107">EXAMPLES</span></span>

### <span data-ttu-id="e30d5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e30d5-108">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### <span data-ttu-id="e30d5-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e30d5-109">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### <span data-ttu-id="e30d5-110">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e30d5-110">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

<span data-ttu-id="e30d5-111">Gibt den Status der Verfügbarkeit des Namespacenamens zurück</span><span class="sxs-lookup"><span data-stu-id="e30d5-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="e30d5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e30d5-112">PARAMETERS</span></span>

### <span data-ttu-id="e30d5-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e30d5-113">-Namespace</span></span>
<span data-ttu-id="e30d5-114">Name des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="e30d5-114">ServiceBus Namespace Name.</span></span>

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
### <span data-ttu-id="e30d5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e30d5-115">CommonParameters</span></span>
<span data-ttu-id="e30d5-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e30d5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e30d5-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e30d5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e30d5-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e30d5-118">INPUTS</span></span>

### <span data-ttu-id="e30d5-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e30d5-119">-Namespace</span></span>
 <span data-ttu-id="e30d5-120">System. String</span><span class="sxs-lookup"><span data-stu-id="e30d5-120">System.String</span></span>

## <span data-ttu-id="e30d5-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e30d5-121">OUTPUTS</span></span>

### <span data-ttu-id="e30d5-122">[Microsoft. Azure. Commands. ServiceBus. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="e30d5-122">[Microsoft.Azure.Commands.ServiceBus.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="e30d5-123">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e30d5-123">Example 1</span></span>
<span data-ttu-id="e30d5-124">NameAvailable-Grund Nachricht</span><span class="sxs-lookup"><span data-stu-id="e30d5-124">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="e30d5-125">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e30d5-125">Example 2</span></span>
<span data-ttu-id="e30d5-126">NameAvailable-Grund Nachricht</span><span class="sxs-lookup"><span data-stu-id="e30d5-126">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="e30d5-127">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e30d5-127">Example 3</span></span>
<span data-ttu-id="e30d5-128">NameAvailable-Grund Nachricht</span><span class="sxs-lookup"><span data-stu-id="e30d5-128">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="e30d5-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="e30d5-129">NOTES</span></span>

## <span data-ttu-id="e30d5-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e30d5-130">RELATED LINKS</span></span>
