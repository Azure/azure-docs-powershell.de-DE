---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 69f6b1bc50681bafe7a860dcebaa7616c8f14e90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665121"
---
# <span data-ttu-id="b80dd-101">Get-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="b80dd-101">Get-AzureRmRelayKey</span></span>

## <span data-ttu-id="b80dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b80dd-102">SYNOPSIS</span></span>
<span data-ttu-id="b80dd-103">Ruft die primären und sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten ab (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="b80dd-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b80dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b80dd-104">SYNTAX</span></span>

### <span data-ttu-id="b80dd-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b80dd-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b80dd-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b80dd-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b80dd-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b80dd-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b80dd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b80dd-108">DESCRIPTION</span></span>
<span data-ttu-id="b80dd-109">Das Cmdlet " **Get-AzureRmRelayKey** " gibt die primären und sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten zurück (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="b80dd-109">The **Get-AzureRmRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b80dd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b80dd-110">EXAMPLES</span></span>

### <span data-ttu-id="b80dd-111">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="b80dd-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="b80dd-112">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b80dd-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="b80dd-113">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b80dd-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="b80dd-114">Primäre und sekundäre Verbindungszeichenfolge zu den angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="b80dd-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b80dd-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b80dd-115">PARAMETERS</span></span>

### <span data-ttu-id="b80dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b80dd-116">-DefaultProfile</span></span>
<span data-ttu-id="b80dd-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b80dd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b80dd-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b80dd-118">-HybridConnection</span></span>
<span data-ttu-id="b80dd-119">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="b80dd-119">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b80dd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b80dd-120">-Name</span></span>
<span data-ttu-id="b80dd-121">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="b80dd-121">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b80dd-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b80dd-122">-Namespace</span></span>
<span data-ttu-id="b80dd-123">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="b80dd-123">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b80dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b80dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="b80dd-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b80dd-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b80dd-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b80dd-126">-WcfRelay</span></span>
<span data-ttu-id="b80dd-127">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="b80dd-127">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b80dd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b80dd-128">CommonParameters</span></span>
<span data-ttu-id="b80dd-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b80dd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b80dd-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b80dd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b80dd-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b80dd-131">INPUTS</span></span>

### <span data-ttu-id="b80dd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b80dd-132">System.String</span></span>


## <span data-ttu-id="b80dd-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b80dd-133">OUTPUTS</span></span>

### <span data-ttu-id="b80dd-134">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="b80dd-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>


## <span data-ttu-id="b80dd-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b80dd-135">NOTES</span></span>

## <span data-ttu-id="b80dd-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b80dd-136">RELATED LINKS</span></span>
