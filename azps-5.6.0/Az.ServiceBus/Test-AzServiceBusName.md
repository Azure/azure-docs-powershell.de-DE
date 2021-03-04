---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: b2bca900be878e6f89f52b1f6096e82f79ec7863
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923408"
---
# <span data-ttu-id="5b5a3-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="5b5a3-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="5b5a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b5a3-102">SYNOPSIS</span></span>
<span data-ttu-id="5b5a3-103">Überprüft die Verfügbarkeit des angegebenen NameSpace-Namens oder Alias (DR-Konfigurationsname)</span><span class="sxs-lookup"><span data-stu-id="5b5a3-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="5b5a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b5a3-104">SYNTAX</span></span>

### <span data-ttu-id="5b5a3-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5b5a3-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b5a3-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5b5a3-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b5a3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b5a3-107">DESCRIPTION</span></span>
<span data-ttu-id="5b5a3-108">Das **Test-AzServiceBusName-Cmdlet** Überprüfen der Verfügbarkeit des NameSpace-Namens oder Alias (DR-Konfigurationsname)</span><span class="sxs-lookup"><span data-stu-id="5b5a3-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="5b5a3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5b5a3-109">EXAMPLES</span></span>

### <span data-ttu-id="5b5a3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b5a3-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="5b5a3-111">Gibt den Status für die Verfügbarkeit des Namespacenamens "MyNameSapceName" als "True" zurück.</span><span class="sxs-lookup"><span data-stu-id="5b5a3-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="5b5a3-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5b5a3-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="5b5a3-113">Gibt den Status für die Verfügbarkeit des Namespacenamens "MyNameSapceName" als Falsch mit Grund zurück.</span><span class="sxs-lookup"><span data-stu-id="5b5a3-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="5b5a3-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5b5a3-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="5b5a3-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5b5a3-115">PARAMETERS</span></span>

### <span data-ttu-id="5b5a3-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="5b5a3-116">-AliasName</span></span>
<span data-ttu-id="5b5a3-117">DR-Konfigurationsname – Aliasname</span><span class="sxs-lookup"><span data-stu-id="5b5a3-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="5b5a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b5a3-118">-DefaultProfile</span></span>
<span data-ttu-id="5b5a3-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b5a3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b5a3-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5b5a3-120">-Namespace</span></span>
<span data-ttu-id="5b5a3-121">Namespacename von Servicebus</span><span class="sxs-lookup"><span data-stu-id="5b5a3-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="5b5a3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b5a3-122">-ResourceGroupName</span></span>
<span data-ttu-id="5b5a3-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="5b5a3-123">Resource Group Name</span></span>

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

### <span data-ttu-id="5b5a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b5a3-124">CommonParameters</span></span>
<span data-ttu-id="5b5a3-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b5a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b5a3-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b5a3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b5a3-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5b5a3-127">INPUTS</span></span>

### <span data-ttu-id="5b5a3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5b5a3-128">System.String</span></span>

## <span data-ttu-id="5b5a3-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5b5a3-129">OUTPUTS</span></span>

### <span data-ttu-id="5b5a3-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="5b5a3-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="5b5a3-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5b5a3-131">NOTES</span></span>

## <span data-ttu-id="5b5a3-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5b5a3-132">RELATED LINKS</span></span>
