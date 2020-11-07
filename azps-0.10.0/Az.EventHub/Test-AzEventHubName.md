---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 49b47e637d009eabac106679e81ec763b0898160
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843995"
---
# <span data-ttu-id="32858-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="32858-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="32858-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="32858-102">SYNOPSIS</span></span>
<span data-ttu-id="32858-103">Überprüft die Verfügbarkeit des angegebenen Namespace namens oder-Alias (Dr-Konfigurationsname).</span><span class="sxs-lookup"><span data-stu-id="32858-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="32858-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32858-104">SYNTAX</span></span>

### <span data-ttu-id="32858-105">NamespaceCheckNameAvailabilitySet (Standard)</span><span class="sxs-lookup"><span data-stu-id="32858-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32858-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="32858-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32858-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32858-107">DESCRIPTION</span></span>
<span data-ttu-id="32858-108">Das Cmdlet " **Test-AzEventhubName** " überprüft die Verfügbarkeit des Namespace namens oder-Alias (Dr-Konfigurations Name).</span><span class="sxs-lookup"><span data-stu-id="32858-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="32858-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32858-109">EXAMPLES</span></span>

### <span data-ttu-id="32858-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="32858-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="32858-111">Gibt den Status der Verfügbarkeit des Namespacenamens "MyNameSapceName" als "wahr" zurück, falls verfügbar</span><span class="sxs-lookup"><span data-stu-id="32858-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="32858-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="32858-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="32858-113">Gibt den Status der Verfügbarkeit des Namespacenamens "MyNameSapceName" als "falsch" mit "Reason" zurück.</span><span class="sxs-lookup"><span data-stu-id="32858-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="32858-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="32858-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="32858-115">Gibt den Status der Verfügbarkeit des Aliasnamens "myaliasname" für den Namespace "MyNameSapceName" als "true" zurück, falls verfügbar</span><span class="sxs-lookup"><span data-stu-id="32858-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="32858-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="32858-116">PARAMETERS</span></span>

### <span data-ttu-id="32858-117">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="32858-117">-AliasName</span></span>
<span data-ttu-id="32858-118">Dr-Konfigurationsname – Alias Name</span><span class="sxs-lookup"><span data-stu-id="32858-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="32858-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32858-119">-DefaultProfile</span></span>
<span data-ttu-id="32858-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="32858-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32858-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="32858-121">-Namespace</span></span>
<span data-ttu-id="32858-122">Eventhub-Namespace Name</span><span class="sxs-lookup"><span data-stu-id="32858-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="32858-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32858-123">-ResourceGroupName</span></span>
<span data-ttu-id="32858-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="32858-124">Resource Group Name</span></span>

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

### <span data-ttu-id="32858-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32858-125">CommonParameters</span></span>
<span data-ttu-id="32858-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32858-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32858-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32858-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32858-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="32858-128">INPUTS</span></span>

### <span data-ttu-id="32858-129">System. String</span><span class="sxs-lookup"><span data-stu-id="32858-129">System.String</span></span>

## <span data-ttu-id="32858-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="32858-130">OUTPUTS</span></span>

### <span data-ttu-id="32858-131">Microsoft. Azure. Commands. EventHub. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="32858-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="32858-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="32858-132">NOTES</span></span>

## <span data-ttu-id="32858-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="32858-133">RELATED LINKS</span></span>
