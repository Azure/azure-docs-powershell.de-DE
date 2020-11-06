---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: 24041c299f2f242126f265ad232db3e0c5d526b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503202"
---
# <span data-ttu-id="714ea-101">Get-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="714ea-101">Get-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="714ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="714ea-102">SYNOPSIS</span></span>
<span data-ttu-id="714ea-103">Ruft die primären und sekundären Verbindungszeichenfolgen für das ServiceBus-Thema ab.</span><span class="sxs-lookup"><span data-stu-id="714ea-103">Gets the primary and secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="714ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="714ea-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="714ea-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="714ea-105">DESCRIPTION</span></span>
<span data-ttu-id="714ea-106">Das Cmdlet " **Get-AzureRmServiceBusTopicKey** " gibt die primären und sekundären Verbindungszeichenfolgen für das angegebene ServiceBus-Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="714ea-106">The **Get-AzureRmServiceBusTopicKey** cmdlet returns the primary and secondary connection strings for the given Service Bus topic.</span></span>

## <span data-ttu-id="714ea-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="714ea-107">EXAMPLES</span></span>

### <span data-ttu-id="714ea-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="714ea-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="714ea-109">Gibt die primären und sekundären Verbindungszeichenfolgen für das angegebene ServiceBus-Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="714ea-109">Returns the primary and secondary connection strings for the specified Service Bus topic.</span></span>

## <span data-ttu-id="714ea-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="714ea-110">PARAMETERS</span></span>

### <span data-ttu-id="714ea-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="714ea-111">-ResourceGroup</span></span>
<span data-ttu-id="714ea-112">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="714ea-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="714ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="714ea-113">-DefaultProfile</span></span>
<span data-ttu-id="714ea-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="714ea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="714ea-115">-Name</span><span class="sxs-lookup"><span data-stu-id="714ea-115">-Name</span></span>
<span data-ttu-id="714ea-116">Thema-AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="714ea-116">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="714ea-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="714ea-117">-Namespace</span></span>
<span data-ttu-id="714ea-118">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="714ea-118">Namespace Name.</span></span>

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

### <span data-ttu-id="714ea-119">-Topic</span><span class="sxs-lookup"><span data-stu-id="714ea-119">-Topic</span></span>
<span data-ttu-id="714ea-120">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="714ea-120">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="714ea-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="714ea-121">CommonParameters</span></span>
<span data-ttu-id="714ea-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="714ea-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="714ea-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="714ea-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="714ea-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="714ea-124">INPUTS</span></span>

### <span data-ttu-id="714ea-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="714ea-125">-ResourceGroup</span></span>
 <span data-ttu-id="714ea-126">System. String</span><span class="sxs-lookup"><span data-stu-id="714ea-126">System.String</span></span>
 

### <span data-ttu-id="714ea-127">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="714ea-127">-NamespaceName</span></span>
 <span data-ttu-id="714ea-128">System. String</span><span class="sxs-lookup"><span data-stu-id="714ea-128">System.String</span></span>
 

### <span data-ttu-id="714ea-129">-Topicname</span><span class="sxs-lookup"><span data-stu-id="714ea-129">-TopicName</span></span>
 <span data-ttu-id="714ea-130">System. String</span><span class="sxs-lookup"><span data-stu-id="714ea-130">System.String</span></span>
 

### <span data-ttu-id="714ea-131">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="714ea-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="714ea-132">System. String</span><span class="sxs-lookup"><span data-stu-id="714ea-132">System.String</span></span>

## <span data-ttu-id="714ea-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="714ea-133">OUTPUTS</span></span>

### <span data-ttu-id="714ea-134">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="714ea-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="714ea-135">PrimaryConnectionString: Endpunkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Wert}; EntityPath = SB-zu pic_exampl1 SecondaryConnectionString: Endpunkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Wert}; EntityPath = SB-zu pic_exampl1 Primär Primär: {Primärwert} SecondaryKey: {SecondaryKey Wert} keyName: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="714ea-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="714ea-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="714ea-136">NOTES</span></span>

## <span data-ttu-id="714ea-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="714ea-137">RELATED LINKS</span></span>

