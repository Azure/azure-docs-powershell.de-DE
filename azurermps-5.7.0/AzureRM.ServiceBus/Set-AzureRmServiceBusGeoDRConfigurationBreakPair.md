---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: da4df1206035e5ecae1a21d70e67091e852b1c51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663042"
---
# <span data-ttu-id="87d1c-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="87d1c-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="87d1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="87d1c-103">Dieser Vorgang deaktiviert die Disaster Recovery und beendet die Replikation von Änderungen von primären zu sekundären Namespaces.</span><span class="sxs-lookup"><span data-stu-id="87d1c-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87d1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87d1c-104">SYNTAX</span></span>

### <span data-ttu-id="87d1c-105">GeoDRBreakPairFailOverPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="87d1c-105">GeoDRBreakPairFailOverPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87d1c-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="87d1c-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87d1c-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87d1c-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87d1c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87d1c-108">DESCRIPTION</span></span>
<span data-ttu-id="87d1c-109">Das Cmdlet " **festlegen-AzureRmServiceBusGeoDRConfigurationBreakPair** " deaktiviert die Disaster Recovery und beendet die Replikation von Änderungen von primären zu sekundären Namespaces.</span><span class="sxs-lookup"><span data-stu-id="87d1c-109">The **Set-AzureRmServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="87d1c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87d1c-110">EXAMPLES</span></span>

### <span data-ttu-id="87d1c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="87d1c-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="87d1c-112">Dieser Vorgang deaktiviert die Disaster Recovery und beendet die Replikation von Änderungen von primären zu sekundären Namespaces.</span><span class="sxs-lookup"><span data-stu-id="87d1c-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="87d1c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="87d1c-113">PARAMETERS</span></span>

### <span data-ttu-id="87d1c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d1c-114">-DefaultProfile</span></span>
<span data-ttu-id="87d1c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="87d1c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87d1c-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="87d1c-116">-InputObject</span></span>
<span data-ttu-id="87d1c-117">ServiceBus-GeoDR-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="87d1c-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87d1c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="87d1c-118">-Name</span></span>
<span data-ttu-id="87d1c-119">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="87d1c-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d1c-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="87d1c-120">-Namespace</span></span>
<span data-ttu-id="87d1c-121">Namespace Name – primärer Namespace</span><span class="sxs-lookup"><span data-stu-id="87d1c-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d1c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87d1c-122">-PassThru</span></span>
<span data-ttu-id="87d1c-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="87d1c-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="87d1c-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="87d1c-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d1c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87d1c-125">-ResourceGroupName</span></span>
<span data-ttu-id="87d1c-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="87d1c-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d1c-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="87d1c-127">-ResourceId</span></span>
<span data-ttu-id="87d1c-128">GeoDRConfiguration-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="87d1c-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d1c-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87d1c-129">-Confirm</span></span>
<span data-ttu-id="87d1c-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87d1c-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d1c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87d1c-131">-WhatIf</span></span>
<span data-ttu-id="87d1c-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87d1c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87d1c-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87d1c-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d1c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d1c-134">CommonParameters</span></span>
<span data-ttu-id="87d1c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87d1c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="87d1c-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87d1c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d1c-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87d1c-137">INPUTS</span></span>

### <span data-ttu-id="87d1c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="87d1c-138">System.String</span></span>
<span data-ttu-id="87d1c-139">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="87d1c-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="87d1c-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87d1c-140">OUTPUTS</span></span>

### <span data-ttu-id="87d1c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="87d1c-141">System.Boolean</span></span>


## <span data-ttu-id="87d1c-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="87d1c-142">NOTES</span></span>

## <span data-ttu-id="87d1c-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87d1c-143">RELATED LINKS</span></span>
