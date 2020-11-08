---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f45899b1c2d397245461a10a6e2648f92dc9da40
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010493"
---
# <span data-ttu-id="67714-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="67714-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="67714-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67714-102">SYNOPSIS</span></span>
<span data-ttu-id="67714-103">Dieser Vorgang deaktiviert die Disaster Recovery und beendet die Replikation von Änderungen von primären zu sekundären Namespaces.</span><span class="sxs-lookup"><span data-stu-id="67714-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="67714-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67714-104">SYNTAX</span></span>

### <span data-ttu-id="67714-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="67714-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67714-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="67714-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67714-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67714-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67714-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67714-108">DESCRIPTION</span></span>
<span data-ttu-id="67714-109">Das Cmdlet " **festlegen-AzServiceBusGeoDRConfigurationBreakPair** " deaktiviert die Disaster Recovery und beendet die Replikation von Änderungen von primären zu sekundären Namespaces.</span><span class="sxs-lookup"><span data-stu-id="67714-109">The **Set-AzServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="67714-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67714-110">EXAMPLES</span></span>

### <span data-ttu-id="67714-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="67714-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="67714-112">Dieser Vorgang deaktiviert die Disaster Recovery und beendet die Replikation von Änderungen von primären zu sekundären Namespaces.</span><span class="sxs-lookup"><span data-stu-id="67714-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="67714-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="67714-113">PARAMETERS</span></span>

### <span data-ttu-id="67714-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67714-114">-DefaultProfile</span></span>
<span data-ttu-id="67714-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67714-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67714-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="67714-116">-InputObject</span></span>
<span data-ttu-id="67714-117">ServiceBus-GeoDR-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="67714-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="67714-118">-Name</span><span class="sxs-lookup"><span data-stu-id="67714-118">-Name</span></span>
<span data-ttu-id="67714-119">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="67714-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="67714-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="67714-120">-Namespace</span></span>
<span data-ttu-id="67714-121">Namespace Name – primärer Namespace</span><span class="sxs-lookup"><span data-stu-id="67714-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="67714-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67714-122">-PassThru</span></span>
<span data-ttu-id="67714-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="67714-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="67714-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="67714-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="67714-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67714-125">-ResourceGroupName</span></span>
<span data-ttu-id="67714-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="67714-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67714-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="67714-127">-ResourceId</span></span>
<span data-ttu-id="67714-128">GeoDRConfiguration-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="67714-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="67714-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="67714-129">-Confirm</span></span>
<span data-ttu-id="67714-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="67714-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67714-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67714-131">-WhatIf</span></span>
<span data-ttu-id="67714-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67714-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67714-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67714-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67714-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67714-134">CommonParameters</span></span>
<span data-ttu-id="67714-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67714-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67714-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67714-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67714-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67714-137">INPUTS</span></span>

### <span data-ttu-id="67714-138">System. String</span><span class="sxs-lookup"><span data-stu-id="67714-138">System.String</span></span>

### <span data-ttu-id="67714-139">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="67714-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="67714-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67714-140">OUTPUTS</span></span>

### <span data-ttu-id="67714-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="67714-141">System.Boolean</span></span>

## <span data-ttu-id="67714-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="67714-142">NOTES</span></span>

## <span data-ttu-id="67714-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67714-143">RELATED LINKS</span></span>
