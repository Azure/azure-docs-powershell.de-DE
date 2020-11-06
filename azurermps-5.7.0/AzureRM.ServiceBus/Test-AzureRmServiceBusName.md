---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: a35487b2eb1dae8d8af452fba9a47854ecab6efb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480885"
---
# <span data-ttu-id="a88a9-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="a88a9-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="a88a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a88a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a88a9-103">Überprüft die Verfügbarkeit des angegebenen Namespace namens oder-Alias (Dr-Konfigurationsname).</span><span class="sxs-lookup"><span data-stu-id="a88a9-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a88a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a88a9-104">SYNTAX</span></span>

### <span data-ttu-id="a88a9-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a88a9-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a88a9-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a88a9-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a88a9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a88a9-107">DESCRIPTION</span></span>
<span data-ttu-id="a88a9-108">Das Cmdlet " **Test-AzureRmServiceBusName** " überprüft die Verfügbarkeit des Namespace namens oder-Alias (Dr-Konfigurations Name).</span><span class="sxs-lookup"><span data-stu-id="a88a9-108">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="a88a9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a88a9-109">EXAMPLES</span></span>

### <span data-ttu-id="a88a9-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a88a9-110">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="a88a9-111">Gibt den Status der Verfügbarkeit des Namespacenamens "MyNameSapceName" als wahr zurück.</span><span class="sxs-lookup"><span data-stu-id="a88a9-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="a88a9-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a88a9-112">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="a88a9-113">Gibt den Status der Verfügbarkeit des Namespacenamens "MyNameSapceName" als "falsch" mit "Reason" zurück.</span><span class="sxs-lookup"><span data-stu-id="a88a9-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="a88a9-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a88a9-114">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```


## <span data-ttu-id="a88a9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a88a9-115">PARAMETERS</span></span>

### <span data-ttu-id="a88a9-116">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="a88a9-116">-AliasName</span></span>
<span data-ttu-id="a88a9-117">Dr-Konfigurationsname – Alias Name</span><span class="sxs-lookup"><span data-stu-id="a88a9-117">DR Configuration Name - Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: Alias

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a88a9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a88a9-118">-DefaultProfile</span></span>
<span data-ttu-id="a88a9-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a88a9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a88a9-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a88a9-120">-Namespace</span></span>
<span data-ttu-id="a88a9-121">ServiceBus-Namespace Name</span><span class="sxs-lookup"><span data-stu-id="a88a9-121">Servicebus Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a88a9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a88a9-122">-ResourceGroupName</span></span>
<span data-ttu-id="a88a9-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a88a9-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a88a9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a88a9-124">CommonParameters</span></span>
<span data-ttu-id="a88a9-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a88a9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a88a9-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a88a9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a88a9-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a88a9-127">INPUTS</span></span>

### <span data-ttu-id="a88a9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a88a9-128">System.String</span></span>


## <span data-ttu-id="a88a9-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a88a9-129">OUTPUTS</span></span>

### <span data-ttu-id="a88a9-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a88a9-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="a88a9-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="a88a9-131">NOTES</span></span>

## <span data-ttu-id="a88a9-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a88a9-132">RELATED LINKS</span></span>
