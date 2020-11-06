---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 4faca15a0c348ee1011789db5acd227c06ee1b85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501606"
---
# <span data-ttu-id="7f3b8-101">Get-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="7f3b8-101">Get-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="7f3b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f3b8-102">SYNOPSIS</span></span>
<span data-ttu-id="7f3b8-103">Ruft die primären und sekundären Verbindungszeichenfolgen für die angegebene ServiceBus-Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="7f3b8-103">Gets the primary and secondary connection strings for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f3b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f3b8-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueKey [-ResourceGroup] <String> -Namespace <String> -Queue <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f3b8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f3b8-105">DESCRIPTION</span></span>
<span data-ttu-id="7f3b8-106">Das Cmdlet " **Get-AzureRmServiceBusQueueKey** " gibt die primären und sekundären Verbindungszeichenfolgen für die angegebene ServiceBus-Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="7f3b8-106">The **Get-AzureRmServiceBusQueueKey** cmdlet returns the primary and secondary connection strings for the given Service Bus queue.</span></span> 

## <span data-ttu-id="7f3b8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f3b8-107">EXAMPLES</span></span>

### <span data-ttu-id="7f3b8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f3b8-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="7f3b8-109">Gibt die primären und sekundären Verbindungszeichenfolgen für die angegebene ServiceBus-Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="7f3b8-109">Returns the primary and secondary connection strings for the specified Service Bus queue.</span></span>

## <span data-ttu-id="7f3b8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f3b8-110">PARAMETERS</span></span>

### <span data-ttu-id="7f3b8-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7f3b8-111">-ResourceGroup</span></span>
<span data-ttu-id="7f3b8-112">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7f3b8-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="7f3b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f3b8-113">-DefaultProfile</span></span>
<span data-ttu-id="7f3b8-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f3b8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f3b8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7f3b8-115">-Name</span></span>
<span data-ttu-id="7f3b8-116">AuthorizationRule-Name der ServiceBus-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="7f3b8-116">ServiceBus Queue AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3b8-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7f3b8-117">-Namespace</span></span>
<span data-ttu-id="7f3b8-118">Name des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="7f3b8-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3b8-119">-Queue</span><span class="sxs-lookup"><span data-stu-id="7f3b8-119">-Queue</span></span>
<span data-ttu-id="7f3b8-120">Name der ServiceBus-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="7f3b8-120">ServiceBus Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3b8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f3b8-121">CommonParameters</span></span>
<span data-ttu-id="7f3b8-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f3b8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f3b8-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f3b8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f3b8-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f3b8-124">INPUTS</span></span>

### <span data-ttu-id="7f3b8-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7f3b8-125">-ResourceGroup</span></span>
 <span data-ttu-id="7f3b8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7f3b8-126">System.String</span></span>
 

### <span data-ttu-id="7f3b8-127">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="7f3b8-127">-NamespaceName</span></span>
 <span data-ttu-id="7f3b8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7f3b8-128">System.String</span></span>
 

### <span data-ttu-id="7f3b8-129">-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="7f3b8-129">-QueueName</span></span>
 <span data-ttu-id="7f3b8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7f3b8-130">System.String</span></span>
 

### <span data-ttu-id="7f3b8-131">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="7f3b8-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="7f3b8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7f3b8-132">System.String</span></span>

## <span data-ttu-id="7f3b8-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f3b8-133">OUTPUTS</span></span>

### <span data-ttu-id="7f3b8-134">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="7f3b8-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="7f3b8-135">PrimaryConnectionString: Endpunkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Wert}; EntityPath = SB-Queue_e xampl1 SecondaryConnectionString: Endpunkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Wert}; EntityPath = SB-Queue_e xampl1 Primary: {Primärwert} SecondaryKey: {SecondaryKey Wert} keyName: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="7f3b8-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="7f3b8-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f3b8-136">NOTES</span></span>

## <span data-ttu-id="7f3b8-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f3b8-137">RELATED LINKS</span></span>

