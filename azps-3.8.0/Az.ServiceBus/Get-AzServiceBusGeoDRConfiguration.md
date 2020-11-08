---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 5a2f3a3310675324fde3ff262cf88325224193c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003959"
---
# <span data-ttu-id="29735-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="29735-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="29735-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29735-102">SYNOPSIS</span></span>
<span data-ttu-id="29735-103">Ruft Alias (Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab</span><span class="sxs-lookup"><span data-stu-id="29735-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="29735-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29735-104">SYNTAX</span></span>

### <span data-ttu-id="29735-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="29735-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29735-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="29735-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29735-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29735-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29735-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29735-108">DESCRIPTION</span></span>
<span data-ttu-id="29735-109">Der **Get-AzServiceBusGeoDRConfiguration** ruft Alias (Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="29735-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="29735-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29735-110">EXAMPLES</span></span>

### <span data-ttu-id="29735-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="29735-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="29735-112">Ruft Alias "SampleDRConfigName"-Konfiguration für den primären Namespace "SampleNamespace_Primary" ab</span><span class="sxs-lookup"><span data-stu-id="29735-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="29735-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="29735-113">PARAMETERS</span></span>

### <span data-ttu-id="29735-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29735-114">-DefaultProfile</span></span>
<span data-ttu-id="29735-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29735-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29735-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="29735-116">-InputObject</span></span>
<span data-ttu-id="29735-117">Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="29735-117">Namespace Object</span></span>

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

### <span data-ttu-id="29735-118">-Name</span><span class="sxs-lookup"><span data-stu-id="29735-118">-Name</span></span>
<span data-ttu-id="29735-119">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="29735-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="29735-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="29735-120">-Namespace</span></span>
<span data-ttu-id="29735-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="29735-121">Namespace Name</span></span>

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

### <span data-ttu-id="29735-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29735-122">-ResourceGroupName</span></span>
<span data-ttu-id="29735-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="29735-123">Resource Group Name</span></span>

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

### <span data-ttu-id="29735-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="29735-124">-ResourceId</span></span>
<span data-ttu-id="29735-125">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="29735-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="29735-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29735-126">CommonParameters</span></span>
<span data-ttu-id="29735-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29735-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29735-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29735-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29735-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29735-129">INPUTS</span></span>

### <span data-ttu-id="29735-130">System. String</span><span class="sxs-lookup"><span data-stu-id="29735-130">System.String</span></span>

### <span data-ttu-id="29735-131">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="29735-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="29735-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29735-132">OUTPUTS</span></span>

### <span data-ttu-id="29735-133">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="29735-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="29735-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="29735-134">NOTES</span></span>

## <span data-ttu-id="29735-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29735-135">RELATED LINKS</span></span>
