---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 9c5fe091e5e218c4e70ef1486f1211bc0be7894b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498814"
---
# <span data-ttu-id="5e99f-101">Remove-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e99f-101">Remove-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="5e99f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e99f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e99f-103">Löscht einen Alias (Disaster Recovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="5e99f-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e99f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e99f-104">SYNTAX</span></span>

### <span data-ttu-id="5e99f-105">GeoDRBreakPairFailOverPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e99f-105">GeoDRBreakPairFailOverPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e99f-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5e99f-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e99f-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e99f-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e99f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e99f-108">DESCRIPTION</span></span>
<span data-ttu-id="5e99f-109">Das Cmdlet **Remove-AzureRmServiceBusGeoDRConfiguration** löscht einen Alias (Disaster Recovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="5e99f-109">The **Remove-AzureRmServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5e99f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e99f-110">EXAMPLES</span></span>

### <span data-ttu-id="5e99f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e99f-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="5e99f-112">Löscht einen Alias (Disaster Recovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="5e99f-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5e99f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e99f-113">PARAMETERS</span></span>

### <span data-ttu-id="5e99f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e99f-114">-AsJob</span></span>
<span data-ttu-id="5e99f-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5e99f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e99f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e99f-116">-DefaultProfile</span></span>
<span data-ttu-id="5e99f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e99f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e99f-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5e99f-118">-InputObject</span></span>
<span data-ttu-id="5e99f-119">ServiceBus-GeoDR-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="5e99f-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="5e99f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5e99f-120">-Name</span></span>
<span data-ttu-id="5e99f-121">Alias Namen (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="5e99f-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="5e99f-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5e99f-122">-Namespace</span></span>
<span data-ttu-id="5e99f-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="5e99f-123">Namespace Name</span></span>

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

### <span data-ttu-id="5e99f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e99f-124">-PassThru</span></span>
<span data-ttu-id="5e99f-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="5e99f-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5e99f-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="5e99f-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5e99f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e99f-127">-ResourceGroupName</span></span>
<span data-ttu-id="5e99f-128">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="5e99f-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e99f-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5e99f-129">-ResourceId</span></span>
<span data-ttu-id="5e99f-130">GeoDRConfiguration-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="5e99f-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="5e99f-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e99f-131">-Confirm</span></span>
<span data-ttu-id="5e99f-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e99f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e99f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e99f-133">-WhatIf</span></span>
<span data-ttu-id="5e99f-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e99f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e99f-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e99f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e99f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e99f-136">CommonParameters</span></span>
<span data-ttu-id="5e99f-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e99f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5e99f-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e99f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e99f-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e99f-139">INPUTS</span></span>

### <span data-ttu-id="5e99f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5e99f-140">System.String</span></span>
<span data-ttu-id="5e99f-141">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="5e99f-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="5e99f-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e99f-142">OUTPUTS</span></span>

### <span data-ttu-id="5e99f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e99f-143">System.Boolean</span></span>


## <span data-ttu-id="5e99f-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e99f-144">NOTES</span></span>

## <span data-ttu-id="5e99f-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e99f-145">RELATED LINKS</span></span>
