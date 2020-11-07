---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c4c23b877ae42703ade4b163c8c09d9156725e77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659379"
---
# <span data-ttu-id="614a8-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="614a8-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="614a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="614a8-102">SYNOPSIS</span></span>
<span data-ttu-id="614a8-103">Löscht einen Alias (Disaster Recovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="614a8-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="614a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="614a8-104">SYNTAX</span></span>

### <span data-ttu-id="614a8-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="614a8-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="614a8-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="614a8-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="614a8-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="614a8-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="614a8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="614a8-108">DESCRIPTION</span></span>
<span data-ttu-id="614a8-109">Das Cmdlet **Remove-AzServiceBusGeoDRConfiguration** löscht einen Alias (Disaster Recovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="614a8-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="614a8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="614a8-110">EXAMPLES</span></span>

### <span data-ttu-id="614a8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="614a8-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="614a8-112">Löscht einen Alias (Disaster Recovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="614a8-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="614a8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="614a8-113">PARAMETERS</span></span>

### <span data-ttu-id="614a8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="614a8-114">-AsJob</span></span>
<span data-ttu-id="614a8-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="614a8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="614a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="614a8-116">-DefaultProfile</span></span>
<span data-ttu-id="614a8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="614a8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="614a8-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="614a8-118">-InputObject</span></span>
<span data-ttu-id="614a8-119">ServiceBus-GeoDR-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="614a8-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="614a8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="614a8-120">-Name</span></span>
<span data-ttu-id="614a8-121">Alias Namen (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="614a8-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="614a8-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="614a8-122">-Namespace</span></span>
<span data-ttu-id="614a8-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="614a8-123">Namespace Name</span></span>

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

### <span data-ttu-id="614a8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="614a8-124">-PassThru</span></span>
<span data-ttu-id="614a8-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="614a8-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="614a8-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="614a8-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="614a8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="614a8-127">-ResourceGroupName</span></span>
<span data-ttu-id="614a8-128">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="614a8-128">Resource Group Name</span></span>

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

### <span data-ttu-id="614a8-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="614a8-129">-ResourceId</span></span>
<span data-ttu-id="614a8-130">GeoDRConfiguration-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="614a8-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="614a8-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="614a8-131">-Confirm</span></span>
<span data-ttu-id="614a8-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="614a8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="614a8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="614a8-133">-WhatIf</span></span>
<span data-ttu-id="614a8-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="614a8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="614a8-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="614a8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="614a8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="614a8-136">CommonParameters</span></span>
<span data-ttu-id="614a8-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="614a8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="614a8-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="614a8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="614a8-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="614a8-139">INPUTS</span></span>

### <span data-ttu-id="614a8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="614a8-140">System.String</span></span>

### <span data-ttu-id="614a8-141">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="614a8-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="614a8-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="614a8-142">OUTPUTS</span></span>

### <span data-ttu-id="614a8-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="614a8-143">System.Boolean</span></span>

## <span data-ttu-id="614a8-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="614a8-144">NOTES</span></span>

## <span data-ttu-id="614a8-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="614a8-145">RELATED LINKS</span></span>
