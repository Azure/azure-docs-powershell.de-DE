---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 40a80a975de56a867f0dcbc34aea0e46d42a155d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482457"
---
# <span data-ttu-id="76702-101">Get-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="76702-101">Get-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="76702-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76702-102">SYNOPSIS</span></span>
<span data-ttu-id="76702-103">Ruft Alias (Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab</span><span class="sxs-lookup"><span data-stu-id="76702-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76702-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="76702-104">SYNTAX</span></span>

### <span data-ttu-id="76702-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="76702-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76702-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="76702-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76702-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76702-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76702-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76702-108">DESCRIPTION</span></span>
<span data-ttu-id="76702-109">Der **Get-AzureRmEventHubGeoDRConfiguration** ruft Alias (Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="76702-109">The **Get-AzureRmEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="76702-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76702-110">EXAMPLES</span></span>

### <span data-ttu-id="76702-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="76702-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="76702-112">Ruft Alias "SampleDRCongifName"-Konfiguration für den primären Namespace "SampleNamespace_Primary" ab</span><span class="sxs-lookup"><span data-stu-id="76702-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="76702-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="76702-113">PARAMETERS</span></span>

### <span data-ttu-id="76702-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76702-114">-DefaultProfile</span></span>
<span data-ttu-id="76702-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76702-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76702-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="76702-116">-InputObject</span></span>
<span data-ttu-id="76702-117">Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="76702-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76702-118">-Name</span><span class="sxs-lookup"><span data-stu-id="76702-118">-Name</span></span>
<span data-ttu-id="76702-119">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="76702-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="76702-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="76702-120">-Namespace</span></span>
<span data-ttu-id="76702-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="76702-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76702-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76702-122">-ResourceGroupName</span></span>
<span data-ttu-id="76702-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="76702-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76702-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="76702-124">-ResourceId</span></span>
<span data-ttu-id="76702-125">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="76702-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="76702-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76702-126">CommonParameters</span></span>
<span data-ttu-id="76702-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76702-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76702-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76702-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76702-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76702-129">INPUTS</span></span>

### <span data-ttu-id="76702-130">System. String</span><span class="sxs-lookup"><span data-stu-id="76702-130">System.String</span></span>

### <span data-ttu-id="76702-131">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="76702-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="76702-132">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="76702-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="76702-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76702-133">OUTPUTS</span></span>

### <span data-ttu-id="76702-134">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="76702-134">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="76702-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="76702-135">NOTES</span></span>

## <span data-ttu-id="76702-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76702-136">RELATED LINKS</span></span>
