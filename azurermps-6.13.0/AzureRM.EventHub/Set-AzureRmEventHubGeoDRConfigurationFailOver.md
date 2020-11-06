---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 84a101a427fc5541d4888a0b4deb4c5e3880b1d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496185"
---
# <span data-ttu-id="53df6-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="53df6-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="53df6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53df6-102">SYNOPSIS</span></span>
<span data-ttu-id="53df6-103">Ruft Geo Dr-Failover auf und konfiguriert den Alias so, dass er auf den sekundären Namespace verweist.</span><span class="sxs-lookup"><span data-stu-id="53df6-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53df6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53df6-104">SYNTAX</span></span>

### <span data-ttu-id="53df6-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="53df6-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53df6-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="53df6-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53df6-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53df6-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53df6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53df6-108">DESCRIPTION</span></span>
<span data-ttu-id="53df6-109">Das Cmdlet " **Satz-AzureRmEventHubGeoDRConfigurationFailOver** " envokes Geo Dr-Failover, und konfigurieren Sie den Alias so, dass er auf den sekundären Namespace verweist.</span><span class="sxs-lookup"><span data-stu-id="53df6-109">The **Set-AzureRmEventHubGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="53df6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53df6-110">EXAMPLES</span></span>

### <span data-ttu-id="53df6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53df6-111">Example 1</span></span>
```
PS C:\>Set-AzureRmEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="53df6-112">Ruft das Failover für den Alias "SampleDRCongifName" auf, konfiguriert und verweist auf den sekundären Namespace "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="53df6-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="53df6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="53df6-113">PARAMETERS</span></span>

### <span data-ttu-id="53df6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53df6-114">-DefaultProfile</span></span>
<span data-ttu-id="53df6-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="53df6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53df6-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="53df6-116">-InputObject</span></span>
<span data-ttu-id="53df6-117">Eventhub GeoDR-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="53df6-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53df6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="53df6-118">-Name</span></span>
<span data-ttu-id="53df6-119">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="53df6-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53df6-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="53df6-120">-Namespace</span></span>
<span data-ttu-id="53df6-121">Namespace Name – sekundärer Namespace</span><span class="sxs-lookup"><span data-stu-id="53df6-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="53df6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53df6-122">-PassThru</span></span>
<span data-ttu-id="53df6-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="53df6-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="53df6-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="53df6-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="53df6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53df6-125">-ResourceGroupName</span></span>
<span data-ttu-id="53df6-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="53df6-126">Resource Group Name</span></span>

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

### <span data-ttu-id="53df6-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="53df6-127">-ResourceId</span></span>
<span data-ttu-id="53df6-128">GeoDRConfiguration-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="53df6-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="53df6-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="53df6-129">-Confirm</span></span>
<span data-ttu-id="53df6-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="53df6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53df6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53df6-131">-WhatIf</span></span>
<span data-ttu-id="53df6-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="53df6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53df6-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="53df6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53df6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53df6-134">CommonParameters</span></span>
<span data-ttu-id="53df6-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53df6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53df6-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53df6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53df6-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53df6-137">INPUTS</span></span>

### <span data-ttu-id="53df6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="53df6-138">System.String</span></span>

### <span data-ttu-id="53df6-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="53df6-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>
<span data-ttu-id="53df6-140">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="53df6-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="53df6-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53df6-141">OUTPUTS</span></span>

### <span data-ttu-id="53df6-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53df6-142">System.Boolean</span></span>

## <span data-ttu-id="53df6-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="53df6-143">NOTES</span></span>

## <span data-ttu-id="53df6-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53df6-144">RELATED LINKS</span></span>
