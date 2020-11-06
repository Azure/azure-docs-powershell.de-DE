---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 87dc2d1e372bdab6415a78e8c79ed0c3bd5491ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496857"
---
# <span data-ttu-id="9a64f-101">Get-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="9a64f-101">Get-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="9a64f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a64f-102">SYNOPSIS</span></span>
<span data-ttu-id="9a64f-103">Ruft die primären und sekundären Verbindungszeichenfolgen für den Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="9a64f-103">Gets the primary and secondary connection strings for the namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a64f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a64f-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a64f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a64f-105">DESCRIPTION</span></span>
<span data-ttu-id="9a64f-106">Das Cmdlet " **Get-AzureRmServiceBusNamespaceKey** " gibt die primären und sekundären Verbindungszeichenfolgen für den angegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="9a64f-106">The **Get-AzureRmServiceBusNamespaceKey** cmdlet returns the primary and secondary connection strings for the given namespace.</span></span> 

## <span data-ttu-id="9a64f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a64f-107">EXAMPLES</span></span>

### <span data-ttu-id="9a64f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9a64f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="9a64f-109">Primäre und sekundäre Verbindungszeichenfolge für den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="9a64f-109">Primary and secondary connection string to the specified namespace.</span></span>

## <span data-ttu-id="9a64f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a64f-110">PARAMETERS</span></span>

### <span data-ttu-id="9a64f-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9a64f-111">-ResourceGroup</span></span>
<span data-ttu-id="9a64f-112">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9a64f-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="9a64f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a64f-113">-DefaultProfile</span></span>
<span data-ttu-id="9a64f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a64f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a64f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9a64f-115">-Name</span></span>
<span data-ttu-id="9a64f-116">ServiceBus-Namespace-AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="9a64f-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="9a64f-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9a64f-117">-Namespace</span></span>
<span data-ttu-id="9a64f-118">Name des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="9a64f-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="9a64f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a64f-119">CommonParameters</span></span>
<span data-ttu-id="9a64f-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a64f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a64f-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a64f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a64f-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a64f-122">INPUTS</span></span>

### <span data-ttu-id="9a64f-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9a64f-123">-ResourceGroup</span></span>
 <span data-ttu-id="9a64f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9a64f-124">System.String</span></span>
 

### <span data-ttu-id="9a64f-125">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="9a64f-125">-NamespaceName</span></span>
 <span data-ttu-id="9a64f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9a64f-126">System.String</span></span>
 

### <span data-ttu-id="9a64f-127">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="9a64f-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="9a64f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9a64f-128">System.String</span></span>

## <span data-ttu-id="9a64f-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a64f-129">OUTPUTS</span></span>

### <span data-ttu-id="9a64f-130">Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="9a64f-130">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="9a64f-131">PrimaryConnectionString: Endpunkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-Wert} SecondaryConnectionString: Endpunkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey Wert} Primär Primär: {Primärwert} SecondaryKey: {SecondaryKey Wert} keyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="9a64f-131">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="9a64f-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a64f-132">NOTES</span></span>

## <span data-ttu-id="9a64f-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a64f-133">RELATED LINKS</span></span>

