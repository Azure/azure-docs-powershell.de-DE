---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 4434802f1025e24bb249ee503ed2267e9187a2c2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846895"
---
# <span data-ttu-id="458f1-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="458f1-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="458f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="458f1-102">SYNOPSIS</span></span>
<span data-ttu-id="458f1-103">Ruft die primären und sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten ab (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="458f1-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="458f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="458f1-104">SYNTAX</span></span>

### <span data-ttu-id="458f1-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="458f1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="458f1-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="458f1-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="458f1-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="458f1-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="458f1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="458f1-108">DESCRIPTION</span></span>
<span data-ttu-id="458f1-109">Das Cmdlet " **Get-AzRelayKey** " gibt die primären und sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten zurück (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="458f1-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="458f1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="458f1-110">EXAMPLES</span></span>

### <span data-ttu-id="458f1-111">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="458f1-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="458f1-112">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="458f1-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="458f1-113">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="458f1-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="458f1-114">Primäre und sekundäre Verbindungszeichenfolge zu den angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="458f1-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="458f1-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="458f1-115">PARAMETERS</span></span>

### <span data-ttu-id="458f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="458f1-116">-DefaultProfile</span></span>
<span data-ttu-id="458f1-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="458f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="458f1-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="458f1-118">-HybridConnection</span></span>
<span data-ttu-id="458f1-119">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="458f1-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="458f1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="458f1-120">-Name</span></span>
<span data-ttu-id="458f1-121">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="458f1-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="458f1-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="458f1-122">-Namespace</span></span>
<span data-ttu-id="458f1-123">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="458f1-123">Namespace Name.</span></span>

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

### <span data-ttu-id="458f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="458f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="458f1-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="458f1-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="458f1-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="458f1-126">-WcfRelay</span></span>
<span data-ttu-id="458f1-127">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="458f1-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="458f1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="458f1-128">CommonParameters</span></span>
<span data-ttu-id="458f1-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="458f1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="458f1-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="458f1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="458f1-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="458f1-131">INPUTS</span></span>

### <span data-ttu-id="458f1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="458f1-132">System.String</span></span>

## <span data-ttu-id="458f1-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="458f1-133">OUTPUTS</span></span>

### <span data-ttu-id="458f1-134">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="458f1-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="458f1-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="458f1-135">NOTES</span></span>

## <span data-ttu-id="458f1-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="458f1-136">RELATED LINKS</span></span>
