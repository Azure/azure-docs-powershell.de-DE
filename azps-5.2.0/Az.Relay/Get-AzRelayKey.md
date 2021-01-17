---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 87682e5aa7b3c6ab5f7cc5ba4200d73f45960001
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359538"
---
# <span data-ttu-id="07758-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="07758-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="07758-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07758-102">SYNOPSIS</span></span>
<span data-ttu-id="07758-103">Ruft die primären und sekundären Verbindungszeichenfolgen für die angegebenen Relayentitäten ab (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="07758-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="07758-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07758-104">SYNTAX</span></span>

### <span data-ttu-id="07758-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="07758-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07758-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="07758-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07758-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="07758-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07758-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07758-108">DESCRIPTION</span></span>
<span data-ttu-id="07758-109">Das **Cmdlet "Get-AzRelayKey"** gibt die primären und sekundären Verbindungszeichenfolgen für die angegebenen Relayentitäten zurück (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="07758-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="07758-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="07758-110">EXAMPLES</span></span>

### <span data-ttu-id="07758-111">Beispiel 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="07758-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="07758-112">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="07758-112">Example 2: WcfRelay</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="07758-113">Beispiel 3: HybridVerbinden</span><span class="sxs-lookup"><span data-stu-id="07758-113">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="07758-114">Primäre und sekundäre Verbindungszeichenfolge zu den angegebenen Relayentitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="07758-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="07758-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07758-115">PARAMETERS</span></span>

### <span data-ttu-id="07758-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07758-116">-DefaultProfile</span></span>
<span data-ttu-id="07758-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07758-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07758-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="07758-118">-HybridConnection</span></span>
<span data-ttu-id="07758-119">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="07758-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="07758-120">-Name</span><span class="sxs-lookup"><span data-stu-id="07758-120">-Name</span></span>
<span data-ttu-id="07758-121">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="07758-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="07758-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="07758-122">-Namespace</span></span>
<span data-ttu-id="07758-123">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="07758-123">Namespace Name.</span></span>

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

### <span data-ttu-id="07758-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07758-124">-ResourceGroupName</span></span>
<span data-ttu-id="07758-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="07758-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="07758-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="07758-126">-WcfRelay</span></span>
<span data-ttu-id="07758-127">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="07758-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="07758-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07758-128">CommonParameters</span></span>
<span data-ttu-id="07758-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07758-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07758-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07758-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07758-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="07758-131">INPUTS</span></span>

### <span data-ttu-id="07758-132">System.String</span><span class="sxs-lookup"><span data-stu-id="07758-132">System.String</span></span>

## <span data-ttu-id="07758-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="07758-133">OUTPUTS</span></span>

### <span data-ttu-id="07758-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="07758-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="07758-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="07758-135">NOTES</span></span>

## <span data-ttu-id="07758-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="07758-136">RELATED LINKS</span></span>
