---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 8c48e6dc8fb095258953a57498b76219dec4ef42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502586"
---
# <span data-ttu-id="4753e-101">Get-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="4753e-101">Get-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="4753e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4753e-102">SYNOPSIS</span></span>
<span data-ttu-id="4753e-103">Ruft Alias (Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab</span><span class="sxs-lookup"><span data-stu-id="4753e-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4753e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4753e-104">SYNTAX</span></span>

### <span data-ttu-id="4753e-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4753e-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4753e-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4753e-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4753e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4753e-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4753e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4753e-108">DESCRIPTION</span></span>
<span data-ttu-id="4753e-109">Der **Get-AzureRmEventHubGeoDRConfiguration** ruft Alias (Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="4753e-109">The **Get-AzureRmEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="4753e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4753e-110">EXAMPLES</span></span>

### <span data-ttu-id="4753e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4753e-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="4753e-112">Ruft Alias "SampleDRCongifName"-Konfiguration für den primären Namespace "SampleNamespace_Primary" ab</span><span class="sxs-lookup"><span data-stu-id="4753e-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="4753e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4753e-113">PARAMETERS</span></span>

### <span data-ttu-id="4753e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4753e-114">-DefaultProfile</span></span>
<span data-ttu-id="4753e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4753e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4753e-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4753e-116">-InputObject</span></span>
<span data-ttu-id="4753e-117">Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="4753e-117">Namespace Object</span></span>

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

### <span data-ttu-id="4753e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4753e-118">-Name</span></span>
<span data-ttu-id="4753e-119">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="4753e-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4753e-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4753e-120">-Namespace</span></span>
<span data-ttu-id="4753e-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="4753e-121">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4753e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4753e-122">-ResourceGroupName</span></span>
<span data-ttu-id="4753e-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="4753e-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4753e-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4753e-124">-ResourceId</span></span>
<span data-ttu-id="4753e-125">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4753e-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="4753e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4753e-126">CommonParameters</span></span>
<span data-ttu-id="4753e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4753e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4753e-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4753e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4753e-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4753e-129">INPUTS</span></span>

### <span data-ttu-id="4753e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4753e-130">System.String</span></span>
<span data-ttu-id="4753e-131">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="4753e-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="4753e-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4753e-132">OUTPUTS</span></span>

### <span data-ttu-id="4753e-133">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4753e-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4753e-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="4753e-134">NOTES</span></span>

## <span data-ttu-id="4753e-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4753e-135">RELATED LINKS</span></span>
