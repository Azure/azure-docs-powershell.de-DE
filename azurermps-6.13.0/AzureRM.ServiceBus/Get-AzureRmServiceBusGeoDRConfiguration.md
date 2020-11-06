---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 7d3635b33e96052c42ca77384d2f138af5cc0d5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501066"
---
# <span data-ttu-id="5336f-101">Get-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="5336f-101">Get-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="5336f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5336f-102">SYNOPSIS</span></span>
<span data-ttu-id="5336f-103">Ruft Alias (Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab</span><span class="sxs-lookup"><span data-stu-id="5336f-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5336f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5336f-104">SYNTAX</span></span>

### <span data-ttu-id="5336f-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5336f-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5336f-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5336f-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5336f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5336f-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5336f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5336f-108">DESCRIPTION</span></span>
<span data-ttu-id="5336f-109">Der **Get-AzureRmServiceBusGeoDRConfiguration** ruft Alias (Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="5336f-109">The **Get-AzureRmServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="5336f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5336f-110">EXAMPLES</span></span>

### <span data-ttu-id="5336f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5336f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="5336f-112">Ruft Alias "SampleDRCongifName"-Konfiguration für den primären Namespace "SampleNamespace_Primary" ab</span><span class="sxs-lookup"><span data-stu-id="5336f-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="5336f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5336f-113">PARAMETERS</span></span>

### <span data-ttu-id="5336f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5336f-114">-DefaultProfile</span></span>
<span data-ttu-id="5336f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5336f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5336f-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5336f-116">-InputObject</span></span>
<span data-ttu-id="5336f-117">Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="5336f-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5336f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5336f-118">-Name</span></span>
<span data-ttu-id="5336f-119">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="5336f-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5336f-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5336f-120">-Namespace</span></span>
<span data-ttu-id="5336f-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="5336f-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5336f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5336f-122">-ResourceGroupName</span></span>
<span data-ttu-id="5336f-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="5336f-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5336f-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5336f-124">-ResourceId</span></span>
<span data-ttu-id="5336f-125">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="5336f-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5336f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5336f-126">CommonParameters</span></span>
<span data-ttu-id="5336f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5336f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5336f-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5336f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5336f-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5336f-129">INPUTS</span></span>

### <span data-ttu-id="5336f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5336f-130">System.String</span></span>

### <span data-ttu-id="5336f-131">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5336f-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="5336f-132">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5336f-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="5336f-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5336f-133">OUTPUTS</span></span>

### <span data-ttu-id="5336f-134">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="5336f-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="5336f-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="5336f-135">NOTES</span></span>

## <span data-ttu-id="5336f-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5336f-136">RELATED LINKS</span></span>
