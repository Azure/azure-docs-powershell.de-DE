---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: a52274d44b36f2e0dea220464ba835635ab845f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471843"
---
# <span data-ttu-id="a10c5-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="a10c5-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="a10c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a10c5-102">SYNOPSIS</span></span>
<span data-ttu-id="a10c5-103">Überprüft die Verfügbarkeit des angegebenen NameSpacenamens oder Alias (DR-Konfigurationsname)</span><span class="sxs-lookup"><span data-stu-id="a10c5-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="a10c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a10c5-104">SYNTAX</span></span>

### <span data-ttu-id="a10c5-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a10c5-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a10c5-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a10c5-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a10c5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a10c5-107">DESCRIPTION</span></span>
<span data-ttu-id="a10c5-108">Das **Cmdlet "Test-AzServiceBusName"** überprüft die Verfügbarkeit des NameSpacenamens oder Alias (DR-Konfigurationsname)</span><span class="sxs-lookup"><span data-stu-id="a10c5-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="a10c5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a10c5-109">EXAMPLES</span></span>

### <span data-ttu-id="a10c5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a10c5-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="a10c5-111">Gibt den Status bei Verfügbarkeit des Namespacenamens 'MyNameSapceName' als True zurück.</span><span class="sxs-lookup"><span data-stu-id="a10c5-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="a10c5-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a10c5-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="a10c5-113">Gibt den Status bei Verfügbarkeit des Namespacenamens "MyNameSapceName" als "False" mit "Reason" zurück.</span><span class="sxs-lookup"><span data-stu-id="a10c5-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="a10c5-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a10c5-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="a10c5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a10c5-115">PARAMETERS</span></span>

### <span data-ttu-id="a10c5-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="a10c5-116">-AliasName</span></span>
<span data-ttu-id="a10c5-117">DR Configuration Name - Alias Name</span><span class="sxs-lookup"><span data-stu-id="a10c5-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="a10c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a10c5-118">-DefaultProfile</span></span>
<span data-ttu-id="a10c5-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a10c5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a10c5-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a10c5-120">-Namespace</span></span>
<span data-ttu-id="a10c5-121">Namespacename des Servicebus</span><span class="sxs-lookup"><span data-stu-id="a10c5-121">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a10c5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a10c5-122">-ResourceGroupName</span></span>
<span data-ttu-id="a10c5-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="a10c5-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a10c5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a10c5-124">CommonParameters</span></span>
<span data-ttu-id="a10c5-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a10c5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a10c5-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a10c5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a10c5-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a10c5-127">INPUTS</span></span>

### <span data-ttu-id="a10c5-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a10c5-128">System.String</span></span>

## <span data-ttu-id="a10c5-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a10c5-129">OUTPUTS</span></span>

### <span data-ttu-id="a10c5-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="a10c5-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="a10c5-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a10c5-131">NOTES</span></span>

## <span data-ttu-id="a10c5-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a10c5-132">RELATED LINKS</span></span>
