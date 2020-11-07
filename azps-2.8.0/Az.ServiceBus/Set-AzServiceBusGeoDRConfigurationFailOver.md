---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 4e6426b00a05568cff5b0fe1c153dcc41b36ed6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824752"
---
# <span data-ttu-id="37e16-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="37e16-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="37e16-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37e16-102">SYNOPSIS</span></span>
<span data-ttu-id="37e16-103">Ruft Geo Dr-Failover auf und konfiguriert den Alias so, dass er auf den sekundären Namespace verweist.</span><span class="sxs-lookup"><span data-stu-id="37e16-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="37e16-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37e16-104">SYNTAX</span></span>

### <span data-ttu-id="37e16-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="37e16-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37e16-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="37e16-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37e16-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37e16-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37e16-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37e16-108">DESCRIPTION</span></span>
<span data-ttu-id="37e16-109">Das Cmdlet " **Satz-AzServiceBusGeoDRConfigurationFailOver** " ruft Geo Dr-Failover auf und konfiguriert den Alias so, dass er auf den sekundären Namespace verweist.</span><span class="sxs-lookup"><span data-stu-id="37e16-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="37e16-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37e16-110">EXAMPLES</span></span>

### <span data-ttu-id="37e16-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37e16-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="37e16-112">Ruft das Failover für den Alias "SampleDRConfigName" auf, konfiguriert und verweist auf den sekundären Namespace "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="37e16-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="37e16-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="37e16-113">PARAMETERS</span></span>

### <span data-ttu-id="37e16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e16-114">-DefaultProfile</span></span>
<span data-ttu-id="37e16-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37e16-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37e16-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="37e16-116">-InputObject</span></span>
<span data-ttu-id="37e16-117">ServiceBus-GeoDR-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="37e16-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="37e16-118">-Name</span><span class="sxs-lookup"><span data-stu-id="37e16-118">-Name</span></span>
<span data-ttu-id="37e16-119">Dr-Konfigurations Name-Alias</span><span class="sxs-lookup"><span data-stu-id="37e16-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="37e16-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="37e16-120">-Namespace</span></span>
<span data-ttu-id="37e16-121">Namespace Name – sekundärer Namespace</span><span class="sxs-lookup"><span data-stu-id="37e16-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="37e16-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37e16-122">-PassThru</span></span>
<span data-ttu-id="37e16-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="37e16-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="37e16-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="37e16-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="37e16-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37e16-125">-ResourceGroupName</span></span>
<span data-ttu-id="37e16-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="37e16-126">Resource Group Name</span></span>

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

### <span data-ttu-id="37e16-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="37e16-127">-ResourceId</span></span>
<span data-ttu-id="37e16-128">GeoDRConfiguration-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="37e16-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="37e16-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37e16-129">-Confirm</span></span>
<span data-ttu-id="37e16-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37e16-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37e16-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37e16-131">-WhatIf</span></span>
<span data-ttu-id="37e16-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37e16-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37e16-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37e16-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37e16-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e16-134">CommonParameters</span></span>
<span data-ttu-id="37e16-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37e16-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e16-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37e16-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e16-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37e16-137">INPUTS</span></span>

### <span data-ttu-id="37e16-138">System. String</span><span class="sxs-lookup"><span data-stu-id="37e16-138">System.String</span></span>

### <span data-ttu-id="37e16-139">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="37e16-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="37e16-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37e16-140">OUTPUTS</span></span>

### <span data-ttu-id="37e16-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="37e16-141">System.Boolean</span></span>

## <span data-ttu-id="37e16-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="37e16-142">NOTES</span></span>

## <span data-ttu-id="37e16-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37e16-143">RELATED LINKS</span></span>
