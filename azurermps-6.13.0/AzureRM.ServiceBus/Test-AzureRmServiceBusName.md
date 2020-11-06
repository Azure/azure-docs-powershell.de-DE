---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: e7fafeeee8a377cc9bb7eb9ce514c0a0d7b89c9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482026"
---
# <span data-ttu-id="aaef5-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="aaef5-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="aaef5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aaef5-102">SYNOPSIS</span></span>
<span data-ttu-id="aaef5-103">Überprüft die Verfügbarkeit des angegebenen Namespace namens oder-Alias (Dr-Konfigurationsname).</span><span class="sxs-lookup"><span data-stu-id="aaef5-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaef5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aaef5-104">SYNTAX</span></span>

### <span data-ttu-id="aaef5-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="aaef5-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaef5-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="aaef5-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aaef5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aaef5-107">DESCRIPTION</span></span>
<span data-ttu-id="aaef5-108">Das Cmdlet " **Test-AzureRmServiceBusName** " überprüft die Verfügbarkeit des Namespace namens oder-Alias (Dr-Konfigurations Name).</span><span class="sxs-lookup"><span data-stu-id="aaef5-108">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="aaef5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aaef5-109">EXAMPLES</span></span>

### <span data-ttu-id="aaef5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aaef5-110">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="aaef5-111">Gibt den Status der Verfügbarkeit des Namespacenamens "MyNameSapceName" als wahr zurück.</span><span class="sxs-lookup"><span data-stu-id="aaef5-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="aaef5-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="aaef5-112">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="aaef5-113">Gibt den Status der Verfügbarkeit des Namespacenamens "MyNameSapceName" als "falsch" mit "Reason" zurück.</span><span class="sxs-lookup"><span data-stu-id="aaef5-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="aaef5-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="aaef5-114">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="aaef5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="aaef5-115">PARAMETERS</span></span>

### <span data-ttu-id="aaef5-116">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="aaef5-116">-AliasName</span></span>
<span data-ttu-id="aaef5-117">Dr-Konfigurationsname – Alias Name</span><span class="sxs-lookup"><span data-stu-id="aaef5-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="aaef5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaef5-118">-DefaultProfile</span></span>
<span data-ttu-id="aaef5-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aaef5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaef5-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="aaef5-120">-Namespace</span></span>
<span data-ttu-id="aaef5-121">ServiceBus-Namespace Name</span><span class="sxs-lookup"><span data-stu-id="aaef5-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="aaef5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaef5-122">-ResourceGroupName</span></span>
<span data-ttu-id="aaef5-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="aaef5-123">Resource Group Name</span></span>

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

### <span data-ttu-id="aaef5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaef5-124">CommonParameters</span></span>
<span data-ttu-id="aaef5-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaef5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaef5-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaef5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaef5-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aaef5-127">INPUTS</span></span>

### <span data-ttu-id="aaef5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="aaef5-128">System.String</span></span>

## <span data-ttu-id="aaef5-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aaef5-129">OUTPUTS</span></span>

### <span data-ttu-id="aaef5-130">Microsoft. Azure. Commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="aaef5-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="aaef5-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="aaef5-131">NOTES</span></span>

## <span data-ttu-id="aaef5-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aaef5-132">RELATED LINKS</span></span>
