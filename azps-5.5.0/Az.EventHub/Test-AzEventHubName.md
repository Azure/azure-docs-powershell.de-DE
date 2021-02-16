---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8eb43982db0eddeb9127006e0cfa3336698eb7e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170622"
---
# <span data-ttu-id="2bc6d-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="2bc6d-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="2bc6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bc6d-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc6d-103">Überprüft die Verfügbarkeit des angegebenen NameSpacenamens oder Alias (DR-Konfigurationsname)</span><span class="sxs-lookup"><span data-stu-id="2bc6d-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="2bc6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bc6d-104">SYNTAX</span></span>

### <span data-ttu-id="2bc6d-105">NamespaceCheckNameAvailabilitySet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2bc6d-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bc6d-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2bc6d-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bc6d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2bc6d-107">DESCRIPTION</span></span>
<span data-ttu-id="2bc6d-108">Das **Test-AzEventhubName-Cmdlet** überprüft die Verfügbarkeit des NameSpacenamens oder Alias (DR-Konfigurationsname)</span><span class="sxs-lookup"><span data-stu-id="2bc6d-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="2bc6d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2bc6d-109">EXAMPLES</span></span>

### <span data-ttu-id="2bc6d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2bc6d-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="2bc6d-111">Gibt den Status bei Verfügbarkeit des Namespacenamens 'MyNameSapceName' als True (falls verfügbar) zurück.</span><span class="sxs-lookup"><span data-stu-id="2bc6d-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="2bc6d-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2bc6d-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="2bc6d-113">Gibt den Status bei Verfügbarkeit des Namespacenamens "MyNameSapceName" als "False" mit "Reason" zurück.</span><span class="sxs-lookup"><span data-stu-id="2bc6d-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="2bc6d-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2bc6d-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="2bc6d-115">Gibt den Verfügbarkeitsstatus des Aliasnamens 'myAliasName' für den Namespace 'MyNameSapceName' als True (falls verfügbar) zurück.</span><span class="sxs-lookup"><span data-stu-id="2bc6d-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="2bc6d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2bc6d-116">PARAMETERS</span></span>

### <span data-ttu-id="2bc6d-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="2bc6d-117">-AliasName</span></span>
<span data-ttu-id="2bc6d-118">DR Configuration Name - Alias Name</span><span class="sxs-lookup"><span data-stu-id="2bc6d-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="2bc6d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc6d-119">-DefaultProfile</span></span>
<span data-ttu-id="2bc6d-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2bc6d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bc6d-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2bc6d-121">-Namespace</span></span>
<span data-ttu-id="2bc6d-122">Namespacename von Eventhub</span><span class="sxs-lookup"><span data-stu-id="2bc6d-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="2bc6d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bc6d-123">-ResourceGroupName</span></span>
<span data-ttu-id="2bc6d-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="2bc6d-124">Resource Group Name</span></span>

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

### <span data-ttu-id="2bc6d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc6d-125">CommonParameters</span></span>
<span data-ttu-id="2bc6d-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bc6d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc6d-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bc6d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc6d-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2bc6d-128">INPUTS</span></span>

### <span data-ttu-id="2bc6d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2bc6d-129">System.String</span></span>

## <span data-ttu-id="2bc6d-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2bc6d-130">OUTPUTS</span></span>

### <span data-ttu-id="2bc6d-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="2bc6d-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="2bc6d-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2bc6d-132">NOTES</span></span>

## <span data-ttu-id="2bc6d-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2bc6d-133">RELATED LINKS</span></span>
