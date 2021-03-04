---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 6620579ad49143dc715fc62f23d305e2efd3d5ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946560"
---
# <span data-ttu-id="e9d14-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="e9d14-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="e9d14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9d14-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d14-103">Überprüft die Verfügbarkeit des angegebenen NameSpace-Namens oder Alias (DR-Konfigurationsname)</span><span class="sxs-lookup"><span data-stu-id="e9d14-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="e9d14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9d14-104">SYNTAX</span></span>

### <span data-ttu-id="e9d14-105">NamespaceCheckNameAvailabilitySet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9d14-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9d14-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e9d14-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9d14-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9d14-107">DESCRIPTION</span></span>
<span data-ttu-id="e9d14-108">Das **Test-AzEventhubName-Cmdlet** überprüft die Verfügbarkeit des NameSpace-Namens oder Alias (DR-Konfigurationsname)</span><span class="sxs-lookup"><span data-stu-id="e9d14-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="e9d14-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e9d14-109">EXAMPLES</span></span>

### <span data-ttu-id="e9d14-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e9d14-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="e9d14-111">Gibt den Status für die Verfügbarkeit des Namespacenamens "MyNameSapceName" als "True" zurück, wenn verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9d14-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="e9d14-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e9d14-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="e9d14-113">Gibt den Status für die Verfügbarkeit des Namespacenamens "MyNameSapceName" als Falsch mit Grund zurück.</span><span class="sxs-lookup"><span data-stu-id="e9d14-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="e9d14-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e9d14-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="e9d14-115">Gibt den Status für die Verfügbarkeit des Aliasnamens "myAliasName" für namespace 'MyNameSapceName' als True zurück, wenn verfügbar</span><span class="sxs-lookup"><span data-stu-id="e9d14-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="e9d14-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e9d14-116">PARAMETERS</span></span>

### <span data-ttu-id="e9d14-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="e9d14-117">-AliasName</span></span>
<span data-ttu-id="e9d14-118">DR-Konfigurationsname – Aliasname</span><span class="sxs-lookup"><span data-stu-id="e9d14-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="e9d14-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d14-119">-DefaultProfile</span></span>
<span data-ttu-id="e9d14-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9d14-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9d14-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e9d14-121">-Namespace</span></span>
<span data-ttu-id="e9d14-122">Name des Eventhub-Namespaces</span><span class="sxs-lookup"><span data-stu-id="e9d14-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="e9d14-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9d14-123">-ResourceGroupName</span></span>
<span data-ttu-id="e9d14-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="e9d14-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e9d14-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d14-125">CommonParameters</span></span>
<span data-ttu-id="e9d14-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9d14-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d14-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9d14-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d14-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e9d14-128">INPUTS</span></span>

### <span data-ttu-id="e9d14-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e9d14-129">System.String</span></span>

## <span data-ttu-id="e9d14-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e9d14-130">OUTPUTS</span></span>

### <span data-ttu-id="e9d14-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="e9d14-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="e9d14-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e9d14-132">NOTES</span></span>

## <span data-ttu-id="e9d14-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e9d14-133">RELATED LINKS</span></span>
