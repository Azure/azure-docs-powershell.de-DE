---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e5623ed840b9b1d2a7f75150fa686d6f488dc2ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480905"
---
# <span data-ttu-id="c2577-101">Get-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2577-101">Get-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="c2577-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2577-102">SYNOPSIS</span></span>
<span data-ttu-id="c2577-103">Ruft Alias (Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab</span><span class="sxs-lookup"><span data-stu-id="c2577-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2577-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2577-104">SYNTAX</span></span>

### <span data-ttu-id="c2577-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2577-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2577-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c2577-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2577-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2577-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2577-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2577-108">DESCRIPTION</span></span>
<span data-ttu-id="c2577-109">Der **Get-AzureRmServiceBusGeoDRConfiguration** ruft Alias (Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="c2577-109">The **Get-AzureRmServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="c2577-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2577-110">EXAMPLES</span></span>

### <span data-ttu-id="c2577-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c2577-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="c2577-112">Ruft Alias "SampleDRCongifName"-Konfiguration für den primären Namespace "SampleNamespace_Primary" ab</span><span class="sxs-lookup"><span data-stu-id="c2577-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="c2577-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2577-113">PARAMETERS</span></span>

### <span data-ttu-id="c2577-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2577-114">-DefaultProfile</span></span>
<span data-ttu-id="c2577-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2577-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2577-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c2577-116">-InputObject</span></span>
<span data-ttu-id="c2577-117">Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="c2577-117">Namespace Object</span></span>

```yaml
Type: PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2577-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c2577-118">-Name</span></span>
<span data-ttu-id="c2577-119">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="c2577-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2577-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c2577-120">-Namespace</span></span>
<span data-ttu-id="c2577-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="c2577-121">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2577-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2577-122">-ResourceGroupName</span></span>
<span data-ttu-id="c2577-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="c2577-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2577-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c2577-124">-ResourceId</span></span>
<span data-ttu-id="c2577-125">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c2577-125">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2577-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2577-126">CommonParameters</span></span>
<span data-ttu-id="c2577-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2577-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c2577-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2577-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2577-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2577-129">INPUTS</span></span>

### <span data-ttu-id="c2577-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c2577-130">System.String</span></span>
<span data-ttu-id="c2577-131">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c2577-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="c2577-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2577-132">OUTPUTS</span></span>

### <span data-ttu-id="c2577-133">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c2577-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="c2577-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2577-134">NOTES</span></span>

## <span data-ttu-id="c2577-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2577-135">RELATED LINKS</span></span>
