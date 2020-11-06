---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 274563165beefdc8a5d7575bd32328f68bf40efa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501970"
---
# <span data-ttu-id="cc31d-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="cc31d-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="cc31d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc31d-102">SYNOPSIS</span></span>
<span data-ttu-id="cc31d-103">Ruft Geo Dr-Failover auf und konfiguriert den Alias so, dass er auf den sekundären Namespace verweist.</span><span class="sxs-lookup"><span data-stu-id="cc31d-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc31d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc31d-104">SYNTAX</span></span>

### <span data-ttu-id="cc31d-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cc31d-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc31d-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cc31d-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc31d-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc31d-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc31d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc31d-108">DESCRIPTION</span></span>
<span data-ttu-id="cc31d-109">Das Cmdlet " **Satz-AzureRmServiceBusGeoDRConfigurationFailOver** " envokes Geo Dr-Failover, und konfigurieren Sie den Alias so, dass er auf den sekundären Namespace verweist.</span><span class="sxs-lookup"><span data-stu-id="cc31d-109">The **Set-AzureRmServiceBusGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="cc31d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc31d-110">EXAMPLES</span></span>

### <span data-ttu-id="cc31d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc31d-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="cc31d-112">Ruft das Failover für den Alias "SampleDRCongifName" auf, konfiguriert und verweist auf den sekundären Namespace "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="cc31d-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="cc31d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc31d-113">PARAMETERS</span></span>

### <span data-ttu-id="cc31d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc31d-114">-DefaultProfile</span></span>
<span data-ttu-id="cc31d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc31d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc31d-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cc31d-116">-InputObject</span></span>
<span data-ttu-id="cc31d-117">ServiceBus-GeoDR-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="cc31d-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc31d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cc31d-118">-Name</span></span>
<span data-ttu-id="cc31d-119">Dr-Konfigurations Name-Alias</span><span class="sxs-lookup"><span data-stu-id="cc31d-119">DR Configuration Name - Alias</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc31d-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cc31d-120">-Namespace</span></span>
<span data-ttu-id="cc31d-121">Namespace Name – sekundärer Namespace</span><span class="sxs-lookup"><span data-stu-id="cc31d-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="cc31d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc31d-122">-PassThru</span></span>
<span data-ttu-id="cc31d-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="cc31d-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cc31d-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="cc31d-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc31d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc31d-125">-ResourceGroupName</span></span>
<span data-ttu-id="cc31d-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="cc31d-126">Resource Group Name</span></span>

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

### <span data-ttu-id="cc31d-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cc31d-127">-ResourceId</span></span>
<span data-ttu-id="cc31d-128">GeoDRConfiguration-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="cc31d-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc31d-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cc31d-129">-Confirm</span></span>
<span data-ttu-id="cc31d-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc31d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc31d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc31d-131">-WhatIf</span></span>
<span data-ttu-id="cc31d-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc31d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc31d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc31d-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc31d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc31d-134">CommonParameters</span></span>
<span data-ttu-id="cc31d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc31d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc31d-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc31d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc31d-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc31d-137">INPUTS</span></span>

### <span data-ttu-id="cc31d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cc31d-138">System.String</span></span>

### <span data-ttu-id="cc31d-139">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="cc31d-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="cc31d-140">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cc31d-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="cc31d-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc31d-141">OUTPUTS</span></span>

### <span data-ttu-id="cc31d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cc31d-142">System.Boolean</span></span>

## <span data-ttu-id="cc31d-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc31d-143">NOTES</span></span>

## <span data-ttu-id="cc31d-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc31d-144">RELATED LINKS</span></span>
