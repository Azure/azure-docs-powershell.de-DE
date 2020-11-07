---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8717019982175b30e0db84e7433147008e40803e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661016"
---
# <span data-ttu-id="979d6-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="979d6-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="979d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="979d6-102">SYNOPSIS</span></span>
<span data-ttu-id="979d6-103">Überprüft die Verfügbarkeit des angegebenen Namespace namens oder-Alias (Dr-Konfigurationsname).</span><span class="sxs-lookup"><span data-stu-id="979d6-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="979d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="979d6-104">SYNTAX</span></span>

### <span data-ttu-id="979d6-105">NamespaceCheckNameAvailabilitySet (Standard)</span><span class="sxs-lookup"><span data-stu-id="979d6-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="979d6-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="979d6-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="979d6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="979d6-107">DESCRIPTION</span></span>
<span data-ttu-id="979d6-108">Das Cmdlet " **Test-AzEventhubName** " überprüft die Verfügbarkeit des Namespace namens oder-Alias (Dr-Konfigurations Name).</span><span class="sxs-lookup"><span data-stu-id="979d6-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="979d6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="979d6-109">EXAMPLES</span></span>

### <span data-ttu-id="979d6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="979d6-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="979d6-111">Gibt den Status der Verfügbarkeit des Namespacenamens "MyNameSapceName" als "wahr" zurück, falls verfügbar</span><span class="sxs-lookup"><span data-stu-id="979d6-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="979d6-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="979d6-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="979d6-113">Gibt den Status der Verfügbarkeit des Namespacenamens "MyNameSapceName" als "falsch" mit "Reason" zurück.</span><span class="sxs-lookup"><span data-stu-id="979d6-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="979d6-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="979d6-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="979d6-115">Gibt den Status der Verfügbarkeit des Aliasnamens "myaliasname" für den Namespace "MyNameSapceName" als "true" zurück, falls verfügbar</span><span class="sxs-lookup"><span data-stu-id="979d6-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="979d6-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="979d6-116">PARAMETERS</span></span>

### <span data-ttu-id="979d6-117">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="979d6-117">-AliasName</span></span>
<span data-ttu-id="979d6-118">Dr-Konfigurationsname – Alias Name</span><span class="sxs-lookup"><span data-stu-id="979d6-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="979d6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="979d6-119">-DefaultProfile</span></span>
<span data-ttu-id="979d6-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="979d6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="979d6-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="979d6-121">-Namespace</span></span>
<span data-ttu-id="979d6-122">Eventhub-Namespace Name</span><span class="sxs-lookup"><span data-stu-id="979d6-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="979d6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="979d6-123">-ResourceGroupName</span></span>
<span data-ttu-id="979d6-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="979d6-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="979d6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="979d6-125">CommonParameters</span></span>
<span data-ttu-id="979d6-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="979d6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="979d6-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="979d6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="979d6-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="979d6-128">INPUTS</span></span>

### <span data-ttu-id="979d6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="979d6-129">System.String</span></span>

## <span data-ttu-id="979d6-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="979d6-130">OUTPUTS</span></span>

### <span data-ttu-id="979d6-131">Microsoft. Azure. Commands. EventHub. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="979d6-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="979d6-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="979d6-132">NOTES</span></span>

## <span data-ttu-id="979d6-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="979d6-133">RELATED LINKS</span></span>
