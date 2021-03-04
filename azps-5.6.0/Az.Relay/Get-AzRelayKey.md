---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: ca477e278ef28cd2fce17578d55782f3ab610954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943822"
---
# <span data-ttu-id="a54bb-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="a54bb-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="a54bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a54bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a54bb-103">Ruft die primären und sekundären Verbindungszeichenfolgen für die angegebenen Relayentitäten ab (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="a54bb-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="a54bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a54bb-104">SYNTAX</span></span>

### <span data-ttu-id="a54bb-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a54bb-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a54bb-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a54bb-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a54bb-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a54bb-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a54bb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a54bb-108">DESCRIPTION</span></span>
<span data-ttu-id="a54bb-109">Das **Get-AzRelayKey-Cmdlet** gibt die primären und sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten zurück (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="a54bb-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="a54bb-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a54bb-110">EXAMPLES</span></span>

### <span data-ttu-id="a54bb-111">Beispiel 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="a54bb-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="a54bb-112">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="a54bb-112">Example 2: WcfRelay</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="a54bb-113">Beispiel 3: HybridVerbinden</span><span class="sxs-lookup"><span data-stu-id="a54bb-113">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="a54bb-114">Primäre und sekundäre Verbindungszeichenfolge zu den angegebenen Relayentitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="a54bb-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="a54bb-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a54bb-115">PARAMETERS</span></span>

### <span data-ttu-id="a54bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a54bb-116">-DefaultProfile</span></span>
<span data-ttu-id="a54bb-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a54bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a54bb-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="a54bb-118">-HybridConnection</span></span>
<span data-ttu-id="a54bb-119">HybridVerbindeungsname.</span><span class="sxs-lookup"><span data-stu-id="a54bb-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="a54bb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a54bb-120">-Name</span></span>
<span data-ttu-id="a54bb-121">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="a54bb-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="a54bb-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a54bb-122">-Namespace</span></span>
<span data-ttu-id="a54bb-123">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="a54bb-123">Namespace Name.</span></span>

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

### <span data-ttu-id="a54bb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a54bb-124">-ResourceGroupName</span></span>
<span data-ttu-id="a54bb-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="a54bb-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a54bb-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="a54bb-126">-WcfRelay</span></span>
<span data-ttu-id="a54bb-127">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="a54bb-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="a54bb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a54bb-128">CommonParameters</span></span>
<span data-ttu-id="a54bb-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a54bb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a54bb-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a54bb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a54bb-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a54bb-131">INPUTS</span></span>

### <span data-ttu-id="a54bb-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a54bb-132">System.String</span></span>

## <span data-ttu-id="a54bb-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a54bb-133">OUTPUTS</span></span>

### <span data-ttu-id="a54bb-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="a54bb-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="a54bb-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a54bb-135">NOTES</span></span>

## <span data-ttu-id="a54bb-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a54bb-136">RELATED LINKS</span></span>
