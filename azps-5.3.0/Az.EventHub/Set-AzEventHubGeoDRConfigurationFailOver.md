---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 4ee96fbe20fca3f0af1f0bb9604f178b912d0ea2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458672"
---
# <span data-ttu-id="25042-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="25042-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="25042-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25042-102">SYNOPSIS</span></span>
<span data-ttu-id="25042-103">Ruft geo-DR-Failover auf und konfiguriert den Alias so neu, dass er auf den sekundären Namespace verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="25042-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="25042-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25042-104">SYNTAX</span></span>

### <span data-ttu-id="25042-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="25042-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25042-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="25042-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25042-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25042-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25042-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25042-108">DESCRIPTION</span></span>
<span data-ttu-id="25042-109">Das **Cmdlet "Set-AzEventHubGeoDRConfigurationFailOver"** ruft geo-DR-Failover auf und konfiguriert den Alias neu, um auf den sekundären Namespace zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="25042-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="25042-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="25042-110">EXAMPLES</span></span>

### <span data-ttu-id="25042-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="25042-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="25042-112">Ruft den Failover über den Alias "SampleDRConfigName" auf, konfiguriert ihn neu und zeigt auf den sekundären Namespace "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="25042-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="25042-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25042-113">PARAMETERS</span></span>

### <span data-ttu-id="25042-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25042-114">-DefaultProfile</span></span>
<span data-ttu-id="25042-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25042-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25042-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25042-116">-InputObject</span></span>
<span data-ttu-id="25042-117">Eventhub GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="25042-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="25042-118">-Name</span><span class="sxs-lookup"><span data-stu-id="25042-118">-Name</span></span>
<span data-ttu-id="25042-119">Name der DR-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="25042-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="25042-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="25042-120">-Namespace</span></span>
<span data-ttu-id="25042-121">Namespacename – Sekundärer Namespace</span><span class="sxs-lookup"><span data-stu-id="25042-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="25042-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25042-122">-PassThru</span></span>
<span data-ttu-id="25042-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="25042-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="25042-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="25042-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="25042-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25042-125">-ResourceGroupName</span></span>
<span data-ttu-id="25042-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="25042-126">Resource Group Name</span></span>

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

### <span data-ttu-id="25042-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25042-127">-ResourceId</span></span>
<span data-ttu-id="25042-128">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="25042-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="25042-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25042-129">-Confirm</span></span>
<span data-ttu-id="25042-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25042-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25042-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="25042-131">-WhatIf</span></span>
<span data-ttu-id="25042-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25042-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25042-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25042-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25042-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25042-134">CommonParameters</span></span>
<span data-ttu-id="25042-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25042-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25042-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25042-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25042-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="25042-137">INPUTS</span></span>

### <span data-ttu-id="25042-138">System.String</span><span class="sxs-lookup"><span data-stu-id="25042-138">System.String</span></span>

### <span data-ttu-id="25042-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="25042-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="25042-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="25042-140">OUTPUTS</span></span>

### <span data-ttu-id="25042-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25042-141">System.Boolean</span></span>

## <span data-ttu-id="25042-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="25042-142">NOTES</span></span>

## <span data-ttu-id="25042-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="25042-143">RELATED LINKS</span></span>
