---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: 0c094fbc294ac6ca5370f8d82c8ebfceac74af0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659336"
---
# <span data-ttu-id="beb0b-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="beb0b-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="beb0b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="beb0b-102">SYNOPSIS</span></span>
<span data-ttu-id="beb0b-103">Überprüft die Verfügbarkeit des angegebenen Namespace namens oder-Alias (Dr-Konfigurationsname).</span><span class="sxs-lookup"><span data-stu-id="beb0b-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="beb0b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="beb0b-104">SYNTAX</span></span>

### <span data-ttu-id="beb0b-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="beb0b-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="beb0b-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="beb0b-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="beb0b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="beb0b-107">DESCRIPTION</span></span>
<span data-ttu-id="beb0b-108">Das Cmdlet " **Test-AzServiceBusName** " überprüft die Verfügbarkeit des Namespace namens oder-Alias (Dr-Konfigurations Name).</span><span class="sxs-lookup"><span data-stu-id="beb0b-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="beb0b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="beb0b-109">EXAMPLES</span></span>

### <span data-ttu-id="beb0b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="beb0b-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="beb0b-111">Gibt den Status der Verfügbarkeit des Namespacenamens "MyNameSapceName" als wahr zurück.</span><span class="sxs-lookup"><span data-stu-id="beb0b-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="beb0b-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="beb0b-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="beb0b-113">Gibt den Status der Verfügbarkeit des Namespacenamens "MyNameSapceName" als "falsch" mit "Reason" zurück.</span><span class="sxs-lookup"><span data-stu-id="beb0b-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="beb0b-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="beb0b-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="beb0b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="beb0b-115">PARAMETERS</span></span>

### <span data-ttu-id="beb0b-116">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="beb0b-116">-AliasName</span></span>
<span data-ttu-id="beb0b-117">Dr-Konfigurationsname – Alias Name</span><span class="sxs-lookup"><span data-stu-id="beb0b-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="beb0b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beb0b-118">-DefaultProfile</span></span>
<span data-ttu-id="beb0b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="beb0b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="beb0b-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="beb0b-120">-Namespace</span></span>
<span data-ttu-id="beb0b-121">ServiceBus-Namespace Name</span><span class="sxs-lookup"><span data-stu-id="beb0b-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="beb0b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beb0b-122">-ResourceGroupName</span></span>
<span data-ttu-id="beb0b-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="beb0b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="beb0b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beb0b-124">CommonParameters</span></span>
<span data-ttu-id="beb0b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beb0b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beb0b-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beb0b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beb0b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="beb0b-127">INPUTS</span></span>

### <span data-ttu-id="beb0b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="beb0b-128">System.String</span></span>

## <span data-ttu-id="beb0b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="beb0b-129">OUTPUTS</span></span>

### <span data-ttu-id="beb0b-130">Microsoft. Azure. Commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="beb0b-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="beb0b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="beb0b-131">NOTES</span></span>

## <span data-ttu-id="beb0b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="beb0b-132">RELATED LINKS</span></span>
