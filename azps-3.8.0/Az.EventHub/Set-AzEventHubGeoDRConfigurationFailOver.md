---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 4ee96fbe20fca3f0af1f0bb9604f178b912d0ea2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845576"
---
# <span data-ttu-id="43802-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="43802-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="43802-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43802-102">SYNOPSIS</span></span>
<span data-ttu-id="43802-103">Ruft Geo Dr-Failover auf und konfiguriert den Alias so, dass er auf den sekundären Namespace verweist.</span><span class="sxs-lookup"><span data-stu-id="43802-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="43802-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43802-104">SYNTAX</span></span>

### <span data-ttu-id="43802-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="43802-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43802-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="43802-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43802-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43802-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43802-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43802-108">DESCRIPTION</span></span>
<span data-ttu-id="43802-109">Das Cmdlet " **Satz-AzEventHubGeoDRConfigurationFailOver** " ruft Geo Dr-Failover auf und konfiguriert den Alias so, dass er auf den sekundären Namespace verweist.</span><span class="sxs-lookup"><span data-stu-id="43802-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="43802-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43802-110">EXAMPLES</span></span>

### <span data-ttu-id="43802-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43802-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="43802-112">Ruft das Failover für den Alias "SampleDRConfigName" auf, konfiguriert und verweist auf den sekundären Namespace "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="43802-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="43802-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="43802-113">PARAMETERS</span></span>

### <span data-ttu-id="43802-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43802-114">-DefaultProfile</span></span>
<span data-ttu-id="43802-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43802-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43802-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43802-116">-InputObject</span></span>
<span data-ttu-id="43802-117">Eventhub GeoDR-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="43802-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="43802-118">-Name</span><span class="sxs-lookup"><span data-stu-id="43802-118">-Name</span></span>
<span data-ttu-id="43802-119">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="43802-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="43802-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="43802-120">-Namespace</span></span>
<span data-ttu-id="43802-121">Namespace Name – sekundärer Namespace</span><span class="sxs-lookup"><span data-stu-id="43802-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="43802-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43802-122">-PassThru</span></span>
<span data-ttu-id="43802-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="43802-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="43802-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="43802-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="43802-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43802-125">-ResourceGroupName</span></span>
<span data-ttu-id="43802-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="43802-126">Resource Group Name</span></span>

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

### <span data-ttu-id="43802-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="43802-127">-ResourceId</span></span>
<span data-ttu-id="43802-128">GeoDRConfiguration-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="43802-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="43802-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="43802-129">-Confirm</span></span>
<span data-ttu-id="43802-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="43802-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43802-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43802-131">-WhatIf</span></span>
<span data-ttu-id="43802-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43802-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43802-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43802-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43802-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43802-134">CommonParameters</span></span>
<span data-ttu-id="43802-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43802-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43802-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43802-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43802-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43802-137">INPUTS</span></span>

### <span data-ttu-id="43802-138">System. String</span><span class="sxs-lookup"><span data-stu-id="43802-138">System.String</span></span>

### <span data-ttu-id="43802-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="43802-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="43802-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43802-140">OUTPUTS</span></span>

### <span data-ttu-id="43802-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43802-141">System.Boolean</span></span>

## <span data-ttu-id="43802-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="43802-142">NOTES</span></span>

## <span data-ttu-id="43802-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43802-143">RELATED LINKS</span></span>
